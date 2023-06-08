# Deploying Static Websites on AWS S3 with AWS CodePipeline and AWS CloudFront

This repository provides a hands-on guide and sample website files for deploying static websites on AWS S3 using AWS CodePipeline and AWS CloudFront. By following the steps outlined in this guide, you will be able to automate the deployment process for your static websites, ensuring a smooth and efficient workflow.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Steps](#steps)
- [Deployment](#deployment)
- [Customizations](#customizations)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Deploying static websites on AWS S3 offers a cost-effective and scalable solution for hosting and delivering your website's content. AWS CodePipeline is a fully managed continuous delivery service that helps you automate your release pipelines, while AWS CloudFront provides a global content delivery network (CDN) to improve performance and reduce latency.

This project aims to guide you through the process of setting up an automated deployment pipeline for your static website using AWS S3, CodePipeline, and CloudFront. The provided sample website files serve as a starting point for your own project.

## Prerequisites

Before getting started, ensure that you have the following prerequisites in place:

1. An AWS account: To use AWS services, you need an active AWS account. If you don't have one, you can create a new account on the [AWS website](https://aws.amazon.com/).
2. Git: Install Git on your local machine if you haven't already. You can download Git from the [official Git website](https://git-scm.com/downloads).

## Steps

- [Setting up GitHub and AWS CodeCommit repositories](https://github.com/ohansck/HandsOn-s3-cloudfront/blob/main/setup-repo.md)
- [Creating an S3 bucket](https://github.com/ohansck/HandsOn-s3-cloudfront/blob/main/S3.md)
- [Creating an AWS CodePipeline](https://github.com/ohansck/HandsOn-s3-cloudfront/blob/main/codepipeline.md)
- [Configuring AWS CloudFront for website delivery](https://github.com/ohansck/HandsOn-s3-cloudfront/blob/main/cloudfront.md)

## Deployment

To deploy your static website using the automated pipeline, follow these steps:

1. Make changes to your website files locally.
2. Commit and push the changes to your GitHub or AWS CodeCommit repository.
3. AWS CodePipeline will automatically detect the changes and trigger a new pipeline execution.
4. Monitor the pipeline execution in the AWS CodePipeline console.
5. Once the pipeline completes successfully, your website will be deployed to the S3 bucket and accessible via the bucket's URL.

## Customizations

Feel free to customize the sample website files and the deployment pipeline to suit your specific needs. Here are some possible customizations:

- Modify the HTML, CSS, and JavaScript files to build your own website.
- Extend the deployment pipeline to include additional stages, such as testing or security scanning.
- Configure AWS CloudFront to enable custom domain names or SSL certificates.

Remember to update the documentation and instructions accordingly if you make significant changes to the project.

## Contributing

Contributions to this project are welcome! If you have any ideas, improvements, or bug fixes, please submit a pull request. Make sure to follow the existing code style and provide clear commit messages.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute the code in accordance with the terms and conditions of the license.
