# UdacityDevOpsDegree_HighAvailWebApp
Second project of the Udacity DevOps Engineer Nanodegree: deploy a highly available web-application on AWS

## Preparation
- Set up user and install the AWS CLI.
  - Log in to AWS management console
  - select IAM
  - click add user
  - click permissions
  - select programmatic access
  - click attach existing policies tab
  - select administratoraccess policy
  - skip tags, review and create
  - copy key-id and secret key
- Configure AWS CLI
  - open CMD, provide key to `àws configure`, select us-west-2 as default region, skip output
  - test using `aws s3 ls`
  
