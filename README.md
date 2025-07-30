📦 Data Sources
1. S3 Bucket
Bucket Name: loan-etl-iti-bucket
Files:
fact_loans/fact_loan.csv
hardships/hardships.csv

Access Instructions:
-Install AWS CLI
-Configure CLI:
  aws configure
  Add your Access Key, Secret Key
  Set region: us-east-1
  Output format: json

Example Commands:
  aws s3 ls s3://loan-etl-iti-bucket/
  aws s3 cp s3://loan-etl-iti-bucket/fact_loans/fact_loan.csv .
  aws s3 cp s3://loan-etl-iti-bucket/hardships/hardships.csv .
2. PostgreSQL (via Docker)
  Tables:
    credit_history  
    borrower
Access Instructions:
  -Ensure Docker is installed.
  -Start the containerized PostgreSQL instance:
    docker-compose up
3. Local CSV Files
  Files:
    loan_details.csv
    loan_status.csv
These are stored locally and used directly in the pipeline.
