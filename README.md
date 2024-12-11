# Codtech-Project-Task-3
BUILDING A SERVERLESS APPLICATION WITH AWS LAMBDA
# **Create a serverless application using AWS Lambda.**
This project will help you understand serverless computing and how to build applications without managing servers.

This repository contains a simple AWS Serverless Application Model (SAM) application with a Lambda function and an API Gateway. The Lambda function is written in Node.js and is triggered by an HTTP GET request to the /hello path of the API Gateway.

## **Prerequisites**

To deploy and run this serverless application, you need the following:

- An AWS account
- AWS CLI installed and configured with your AWS account credentials
- AWS SAM CLI installed
- NodeJS installed

## **Project Structure**

The project has the following structure:

    .
    ├── README.md
    ├── app.js
    └── template.yaml

- **README.md:** This file, which contains the instructions to set up, deploy, and test the serverless application.
- **app.js/:** the Lambda function's source code (**app.js**).
- **template.yaml:** The AWS SAM template defining the serverless application's resources and configurations.

## **Deployment**

Follow these steps to deploy the serverless application:

1. Clone the repository:

       git clone https://github.com/Afzal-Nezam/Codtech-Project-Task-3

2. Build the serverless application using the SAM CLI:

       sam build

3. Deploy the serverless application using the SAM CLI with guided prompts:

       sam deploy --guided

Provide the necessary information when prompted, such as the stack name, AWS region, and whether to allow or disallow rollback on failure.

4. After the deployment is complete, the SAM CLI will output the API Gateway endpoint URL, which you can find under the Outputs section.

## **Testing**

To test your serverless application, make an HTTP GET request to the API Gateway's endpoint URL using a command like this:

curl https://your-api-gateway-url/Prod/hello/
Replace your-api-gateway-url with the actual URL provided in the deployment details. Upon success, the response should look like this:

json
Copy code
{
  "message": "Hello from Lambda!"
}

## **Cleanup**

To delete the serverless application and its associated resources, you can remove the CloudFormation stack using the AWS CLI with the following command:

aws cloudformation delete-stack --stack-name your-stack-name

Replace your-stack-name with the name of the stack you created during deployment. This command will clean up all the resources associated with the stack.

#**License**
This project is licensed under the terms of the MIT License.
