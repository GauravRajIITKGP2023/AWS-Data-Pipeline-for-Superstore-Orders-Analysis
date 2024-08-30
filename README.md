# AWS-Data-Pipeline-for-Superstore-Orders-Analysis

## Project Overview  
This project demonstrates the end-to-end creation of an automated data pipeline using various Amazon Web Services (AWS), including Identity and Access Management (IAM), Simple Storage Service (S3), AWS Glue, Amazon Athena, and Amazon QuickSight. The pipeline is designed to analyze incremental order data from a fictional Superstore dataset.

## Objectives  
- Showcase proficiency in AWS services for data storage, Extract, Transform, Load (ETL), and analytics.  
- Automate the process of data ingestion, transformation, cataloging, querying, and visualization.  
- Efficiently analyze incremental data using cost-effective AWS solutions.  

## Steps Involved  

1. **Create IAM User**  
   - Created an IAM (Identity and Access Management) user to ensure secure and controlled access to AWS resources, rather than using the root user, which has full access to all services and could pose a security risk.  
   - Assigned necessary permissions to the IAM user for accessing S3, AWS Glue, Amazon Athena, and Amazon QuickSight.  

2. **Set Up S3 Bucket**  
   - Created an Amazon S3 (Simple Storage Service) bucket to store the Superstore order data.  
   - Organized the data in folders by date (e.g., `snapshot/day=2017-01-01`) to facilitate incremental data analysis and improve data management.  

3. **Use AWS Glue for Data Cataloging**  
   - Utilized AWS Glue, a fully managed ETL (Extract, Transform, Load) service, to create a data catalog of the S3 data.  
   - Set up a Glue Crawler to automatically scan the S3 bucket and generate metadata, which is essential for efficient data querying.  
   - Created an IAM role with appropriate permissions for the Glue Crawler to access the S3 bucket, ensuring secure and automated data cataloging.  

4. **Query Data with Amazon Athena**  
   - Employed Amazon Athena, a serverless interactive query service, to analyze the data stored in S3 using standard SQL queries.  
   - Configured Athena to store query results in a specific S3 location, optimizing cost and performance by avoiding unnecessary data storage.  
   - Used partitioning (e.g., by date) to speed up queries and reduce costs by limiting the amount of data scanned.  

5. **Visualize Data with Amazon QuickSight**  
   - Connected Amazon Athena as a data source in Amazon QuickSight, a business intelligence service, for visual data analysis.  
   - Imported data into SPICE (Super-fast, Parallel, In-memory Calculation Engine) to accelerate data processing and enable rapid visualizations.  
   - Developed visualizations (e.g., pie charts, line charts) to extract insights from the data and published a dashboard for collaborative access.  
   - [View the Sample QuickSight Dashboard](https://ap-south-1.quicksight.aws.amazon.com/sn/accounts/084828585962/dashboards/2aaf79f6-d817-4aa4-88b6-17d6c453b047?directory_alias=gaurav-raj-aws-quicksight)  

## Automation  
- Automated the data pipeline to handle incremental data loads using AWS Glue Crawler and scheduled queries in Athena, ensuring continuous data availability and reducing manual intervention.  
- Set up monitoring to keep the data pipeline up-to-date and alert in case of any failures.  

## Tools and Technologies  
- **AWS Services**: IAM, S3, AWS Glue, Amazon Athena, Amazon QuickSight.  
- **Data Tools**: Python, Excel (for initial ETL tasks).  
- **Visualization**: Power BI, QuickSight.  

## Results  
- Developed an end-to-end automated data pipeline on AWS, demonstrating expertise in cloud-based data solutions.  
- Successfully analyzed incremental Superstore order data and created dynamic visualizations, providing actionable insights.  

## How to Run  
- Set up an AWS account and create an IAM user with required permissions following the step-by-step guide provided in this repository.  
- Replicate the pipeline by following the detailed instructions, including IAM user creation, S3 bucket setup, AWS Glue configuration, Athena querying, and QuickSight visualization.  
 
