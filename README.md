Title: Serverless ETL Pipeline with AWS Glue and Lambda

Description: This repository demonstrates a serverless architecture to automate an ETL pipeline using AWS services. The architecture is built for processing raw data in S3, performing schema discovery with AWS Glue Crawlers, and transforming the data with AWS Glue ETL jobs. Notifications are sent via Amazon SNS upon completion.

Architecture Workflow:
Trigger: Raw data is uploaded to the S3 bucket, invoking a Lambda function.
Schema Discovery: The Lambda function triggers an AWS Glue Crawler to identify the schema.
Data Processing: Based on a CloudWatch rule, an AWS Glue ETL job processes and writes the data to a processed S3 bucket.
Notifications: Amazon SNS sends email alerts once the ETL job completes.
Services Used:
Amazon S3: For raw and processed data storage.
AWS Glue Crawler: For schema discovery and catalog creation.
AWS Glue ETL: For data transformation.
AWS Lambda: To orchestrate workflows.
Amazon CloudWatch: For rule-based triggers.
Amazon SNS: For notifications.
Repository Contents:
CloudFormation templates for resource creation.
Python scripts for Lambda functions.
Sample Glue ETL script for transforming data.
Instructions to set up and deploy the pipeline.
