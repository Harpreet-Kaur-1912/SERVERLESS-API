Serverless API with AWS Lambda and API Gateway


This repository contains a simple Serverless API deployed using AWS Lambda and API Gateway. The API is a basic example of creating a serverless function that responds to HTTP requests, and it is deployed using the Serverless Framework.

Prerequisites
Before you start, ensure you have the following installed:
•	Node.js (version 12.x or higher)
•	npm (Node Package Manager)
•	Serverless Framework (globally installed)


To install the Serverless Framework globally, run:
bash
Copy
npm install -g serverless
Additionally, you will need:
•	AWS Account: To deploy the API to AWS.
•	AWS CLI: To set up AWS credentials on your local machine.
•	Git: To clone the repository and manage version control.


Steps to Deploy

1. Clone the Repository
First, clone this repository to your local machine:
bash
Copy
git clone https://github.com/your-username/serverless-api.git
cd serverless-api

2. Install Dependencies
Once you have the project, navigate to the project folder and install the required dependencies:
bash
Copy
npm install
This will install all the necessary libraries, including the Serverless Framework and others required to run your Lambda function.

3. Set Up AWS Credentials
You will need to configure your AWS credentials to allow Serverless to deploy the resources.
Run the following command to configure the AWS CLI:
bash
Copy
aws configure
You will be prompted to enter your AWS Access Key, Secret Key, region, and output format. You can get your AWS Access Key and AWS Secret Access Key from the AWS IAM section.

4. Deploy the API to AWS
Now that everything is set up, you can deploy the Serverless API to AWS using the Serverless Framework.
Run the following command to deploy:
bash
Copy
serverless deploy --stage dev --region us-east-1
This will:
•	Create the necessary AWS Lambda function.
•	Set up an API Gateway endpoint to trigger the Lambda function.
•	Deploy the resources to AWS.

5. Test the API
After the deployment completes successfully, the command will output the API endpoint URL. You can test the API by visiting the URL in your browser or using a tool like Postman or cURL.
For example, you can run:
bash
Copy
curl https://your-api-id.execute-api.us-east-1.amazonaws.com/dev/hello
This should return a response from your Lambda function.

6. Monitor the Logs (Optional)
You can monitor the logs of your Lambda function in AWS CloudWatch. This will help you see the execution details and any potential issues with your function.
To view the logs for your deployed Lambda function, run:
bash
Copy
serverless logs --function hello --stage dev --region us-east-1

7. Remove the Deployment (Optional)
If you want to remove the resources deployed on AWS, you can run:
bash
Copy
serverless remove --stage dev --region us-east-1
This will clean up all the resources, including the Lambda function and API Gateway endpoint.

Folder Structure

The folder structure of the project is as follows:

bash
Copy
serverless-api/
├── handler.js             # Lambda function code
├── serverless.yml         # Serverless configuration
├── package.json           # Project dependencies
└── .gitignore             # Files and directories to ignore

Project Description
•	handler.js: Contains the Lambda function code. This is where you define the logic for your API endpoints.
•	serverless.yml: The configuration file for Serverless Framework. It defines the services, resources, and functions to be deployed.
•	package.json: Manages project dependencies.
•	.gitignore: Specifies which files and directories should not be tracked by Git.


