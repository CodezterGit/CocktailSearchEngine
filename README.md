# CocktailSearchEngine

Overview

The Cocktail Search Engine is a web application that allows users to search for cocktail recipes. The application is powered by ec2 instances that uses AWS Lambda, API Gateway, and the Cocktail DB API.

Usage

Web Application
    The website runs entirely on the index page. The user uses the search bar to search for any desired cocktail. Press the drink up button and information about the cocktail will be returned below the search bar with a picture.

AWS Lambda and API Gateway
The backend of the Cocktail Search Engine is implemented using AWS Lambda and API Gateway. These services handle the processing of user requests and communication with external APIs.

Lambda Function
This Lambda function receives user input, queries an external cocktail database API, and returns formatted cocktail information back to the web page.

API Gateway
The API Gateway serves as the entry point for HTTP requests and directs them to the Lambda function. It also manages authentication and authorization if needed.

Deployment
To deploy the Cocktail Search Engine backend on AWS:
    Create an AWS account if you don't have one.
    Install and configure the AWS CLI with the necessary credentials.
    Deploy the AWS CloudFormation stack using the provided CloudFormation template. This template creates the required AWS resources, including the Lambda function, API Gateway, VPC, subnets, security groups, and more.
    Once the stack is created, check the AWS CloudFormation console for the stack's outputs. Retrieve the API Gateway endpoint.
    Update the apiGatewayEndpoint variable in the drink-search JavaScript file with the API Gateway endpoint.
    Open the index.html file on from one of the EC2 servers in a web browser and start searching for cocktails!

Technologies Used
    HTML, CSS, and JavaScript for the frontend
    AWS Lambda for serverless function execution
    AWS API Gateway for creating and managing APIs
    AWS CloudFormation for infrastructure as code

Contributors
Matthew Burns, Aaron McIntire, Cody Stocker, Blanche Ranguma
