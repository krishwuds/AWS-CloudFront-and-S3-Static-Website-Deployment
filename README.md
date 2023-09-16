# AWS CloudFront and S3 Static Website Deployment

This repository demonstrates how to deploy a static website using AWS CloudFront and an S3 bucket. In this setup, CloudFront serves as a Content Delivery Network (CDN) to distribute your website globally, while an S3 bucket hosts your static web content.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

1. An AWS account.
2. AWS CLI installed and configured with necessary credentials. You can set it up using `aws configure`.
3. Your static website content, including an `index.html` file.

## Deployment Steps

Follow these steps to deploy your static website:

### 1. Create an S3 Bucket

1.1. Log in to your AWS Management Console.

1.2. Open the S3 service.

1.3. Click "Create bucket" and follow the instructions to create a new bucket. Choose a unique name for your bucket.

1.4. Upload your static website files to this S3 bucket, including the `index.html` file.

### 2. Configure S3 for Static Website Hosting

2.1. Select your S3 bucket from the AWS S3 console.

2.2. Navigate to the "Properties" tab.

2.3. Scroll down to the "Static website hosting" section and click "Edit."

2.4. Choose "Use this bucket to host a website."

2.5. In the "Index document" field, enter `index.html`.

2.6. Save the changes.

### 3. Create an AWS CloudFront Distribution

3.1. Open the CloudFront service from the AWS Management Console.

3.2. Click "Create Distribution."

3.3. Select "Web" as the distribution type.

3.4. Configure the settings, including your S3 bucket as the origin.

3.5. Set up any additional desired options, such as custom domain names, SSL, and caching settings.

3.6. Create the CloudFront distribution.

### 4. Deploy Your Website

4.1. Once your CloudFront distribution is created, you will receive a CloudFront domain name (e.g., `d12345abcde.cloudfront.net`).

4.2. Access your website using the CloudFront domain name, and it should serve your static website.

### 5. Optional: Custom Domain

5.1. If you want to use a custom domain, you can configure DNS settings to point to your CloudFront distribution.

5.2. You may also need to set up an SSL certificate for your custom domain using AWS Certificate Manager (ACM).

## Cleanup

Remember to clean up your AWS resources to avoid unnecessary charges if you no longer need this setup.

## Additional Resources

- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/index.html)
- [AWS CloudFront Documentation](https://docs.aws.amazon.com/cloudfront/index.html)

Enjoy serving your static website with AWS CloudFront and S3!

