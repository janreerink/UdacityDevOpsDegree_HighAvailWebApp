[//]: # (Image References)
[image0]: ./data/success.png "success"
[image1]: ./data/network_diagram.png "network"

# UdacityDevOpsDegree_HighAvailWebApp
Second project of the Udacity DevOps Engineer Nanodegree: deploy a highly available web-application on AWS

![alt text][image1]

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
  

  ## Deploy network and servers
  To create or update use:  

`./create Udacity-WebApp project.yml project-parameters.json`  

`./update Udacity-WebApp project.yml project-parameters.json`

Or directly in CLI:  

`aws cloudformation create-stack --stack-name Udacity-HAWebApp --template-body file://project.yml --parameters file://project-parameters.json --region=us-west-2 --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM CAPABILITY_AUTO_EXPAND`

To delete the stack:  
  `aws cloudformation delete-stack --stack-name UdacityHAWebApp --region=us-west-2`

The stack's output section contains a link to the load-balancer:
http://udaci-webap-qsy0w6i518sl-1914615155.us-west-2.elb.amazonaws.com/  

![alt text][image0]


