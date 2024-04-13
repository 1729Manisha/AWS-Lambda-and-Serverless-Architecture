# AWS Lambda and Serverless Architecture

This project demonstrates the implementation of a contact form on a static website hosted on Amazon S3, with the backend powered by AWS Lambda and Serverless Architecture.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Getting Started](#getting-started)
4. [Usage](#usage)
5. [Architecture](#architecture)
6. [Technologies Used](#technologies-used)

## Introduction

This project aims to solve the challenge of adding dynamic functionality, such as a contact form, to a static website hosted on Amazon S3. By leveraging AWS Lambda and Serverless Architecture, we enable the website to collect user inquiries efficiently and securely without the need for a constantly running server.

## Features

- Integration of a contact form into a static website.
- Processing of form submissions using AWS Lambda.
- Sending email notifications with Amazon SES.
- Storing form data in DynamoDB for future use.

## Getting Started

To get started with this project, follow these steps:

1. **Set up Static Website on Amazon S3:**
   - Create an Amazon S3 bucket to host the static website.
   - Upload the website files (HTML, CSS, JavaScript) to the S3 bucket.
   - Configure the bucket for static website hosting and set permissions accordingly.
   
2. **Custom Domain Configuration with Route 53:**
   - Register a domain name through Route 53 or use an existing one.
   - Create a hosted zone for the domain in Route 53.
   - Configure the domain's DNS settings to point to the S3 bucket using an alias record.
   - Optionally, set up SSL/TLS certificates using AWS Certificate Manager (ACM) for secure communication with the custom domain.

3. **Implementing the Contact Form:**
   - Design and integrate a contact form into the static website using HTML and CSS.
   - Use JavaScript to handle form submission events and client-side validation.
   - Ensure the form includes fields for relevant information such as name, email, subject, and message.
   - Implement error handling to provide feedback to users if form submission fails or if there are validation errors.

4. **Setting up Amazon API Gateway:**
   - Create an API Gateway REST API to serve as the endpoint for the contact form submissions.
   - Define a POST method on the API Gateway to receive form submissions from the static website.
   - Configure request and response mappings as necessary to pass data between the API Gateway and Lambda function.
   - Enable CORS (Cross-Origin Resource Sharing) to allow the static website to make requests to the API Gateway from a different domain.

5. **AWS Lambda Function for Processing Form Data:**
   - Create an AWS Lambda function to handle the processing of form submissions.
   - Choose a supported programming language such as Node.js, Python, Java, or C# for the Lambda function.
   - Implement logic to extract data from the form submission payload and perform any necessary validation.
   - Use AWS SDKs or libraries to interact with other AWS services such as SES and DynamoDB.

6. **Integrating with Amazon SES for Email Notifications:**
   - Configure Amazon Simple Email Service (SES) to send email notifications.
   - Verify the sender's email address or domain in SES to ensure deliverability.
   - Create an email template for the contact form submissions, including placeholders for dynamic content.
   - Modify the Lambda function to trigger an email notification with the form data upon successful form submission.

7. **Extending Functionality with DynamoDB:**
   - Set up a DynamoDB table to store form submissions for future reference.
   - Define the table's primary key and any additional attributes to store relevant information from the form submissions.
   - Update the Lambda function to store the form data in the DynamoDB table after processing it for email notifications.
   - Implement error handling and retries to ensure data consistency and durability in DynamoDB.
## Usage

Once set up, users can interact with the contact form on your static website to submit inquiries. The form submissions will be processed in the background by AWS Lambda, and email notifications will be sent out via Amazon SES. Form data can also be stored in DynamoDB for future reference.

## Architecture

![Architecture Diagram](https://github.com/1729Manisha/AWS-Lambda-and-Serverless-Architecture/blob/main/Serverless%20Architecture/Serverless_Architecture.png?raw=true)

The architecture consists of a static website hosted on Amazon S3, an API Gateway endpoint for handling form submissions, an AWS Lambda function for processing data, and integration with Amazon SES for email notifications.

![Architecture Diagram](https://github.com/1729Manisha/AWS-Lambda-and-Serverless-Architecture/blob/main/Serverless%20Architecture/DynamoDB_Architecture.png?raw=true)

DynamoDB can be used to store form submissions.

## Technologies Used

- Amazon Web Services (AWS)
  - Amazon S3
  - AWS Lambda
  - Amazon API Gateway
  - Amazon Simple Email Service (SES)
  - Amazon DynamoDB
  - AWS Route 53
  - Amazon IAM
  - HTML/CSS/JavaScript
