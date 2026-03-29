# ✅ Method 1: Create DynamoDB Table from AWS Console
## Step 1️⃣ – Login to AWS

Go to aws.amazon.com

Sign in to your AWS account

Open the AWS Management Console

## Step 2️⃣ – Search for DynamoDB

In the top search bar, type DynamoDB

Click on Amazon DynamoDB

## Step 3️⃣ – Create a Table

Click Create table

You will see a form. Fill it like this:

### 🔹 Table name

Example:

Users
### 🔹 Partition key (Primary Key)

Example:

UserID

Data type:

String (or Number if needed)

You can leave other settings as default for now.

## 4️⃣ – Choose Table Settings

You’ll see two capacity modes:

Option A: On-demand (Recommended for beginners)

Automatically scales

Pay only for what you use

👉 Select On-demand

## Step 5️⃣ – Click Create

Click Create table

Wait a few seconds

🎉 Your DynamoDB table is ready!

## Step 6️⃣ – Add Data to Table

Open your table

Go to Explore table items

Click Create item

Add values like:

UserID: 101
Name: John
Email: john@email.com

Click Save

Done ✅

# ✅ Method 2: Create DynamoDB Using AWS CLI

If you have AWS CLI installed:

aws dynamodb create-table \
    --table-name Users \
    --attribute-definitions AttributeName=UserID,AttributeType=S \
    --key-schema AttributeName=UserID,KeyType=HASH \
    --billing-mode PAY_PER_REQUEST

This creates the same table using command line.
