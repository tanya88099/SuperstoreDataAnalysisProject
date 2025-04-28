# SuperstoreDataAnalysisProject
This superstore Data analysis project we'll do it in AWS cloud. We'll explore many things on AWS. 

### Step-by-Step Guide of AWS Project

#### **1. IAM User Setup**
- Create a user in AWS Identity and Access Management (IAM) with a unique name and password.
- Attach **AdministratorAccess** policy directly to grant full admin privileges.
- Note down your account ID and IAM user credentials for login.
- Login as the IAM user for all subsequent steps.

#### **2. Create an S3 Bucket**
- Navigate to S3 in the AWS Management Console.
- Provide a bucket name and select a region (ensure it aligns with your AWS Glue setup later).
- Use default settings and create the bucket.
- Within the bucket:
  - Create a folder named `Orders`.
  - Under `Orders`, create another folder named `snapshot_day=2017-01-01`.
- Download the superstore dataset from Kaggle, clean and format the data, and save it as a `.csv` file named `orders.csv`.
- Upload `orders.csv` to the appropriate folders in S3.

#### **3. AWS Glue: Data Catalog Creation**
- Confirm that the AWS Region matches your S3 bucket setup.
- Navigate to AWS Glue and create a database named `SuperStoreDB`.
- Set up a crawler to extract, transform, and load (ETL) the data into tables:
  - Choose `Add a Data Source`, select the S3 path of `Orders`.
  - Assign a role for AWS Glue (e.g., `glue-role`) and schedule the crawler.
  - Run the crawler to populate the database with tables.

#### **4. AWS Athena: Query Data**
- Access Athena to query the structured data from S3.
- Save the query results in a dedicated folder within S3.
- Test your queries to verify the data catalog created by AWS Glue.

#### **5. Visualize Data with Amazon QuickSight**
- Sign up for Amazon QuickSight and configure your account.
- Import data into SPICE for faster analysis.
- Create datasets using the tables from your database and generate visualizations.
- Explore and share insights from your visualizations.

---
## 🧠 Author

**Tanya Singh**  
Data Modeler | SQL Enthusiast | Azure Certified  
📬 https://www.linkedin.com/in/tanya88099/
