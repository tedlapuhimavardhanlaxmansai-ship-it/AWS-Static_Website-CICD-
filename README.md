
# AWS Static Website Hosting with CI/CD

A production-inspired AWS DevOps project demonstrating secure static website hosting, global content delivery, automated deployment, monitoring, and notifications using Amazon Web Services.

---

## Project Overview

This project demonstrates how to deploy a secure, scalable, and globally accessible static website on **Amazon Web Services (AWS)** using a modern **CI/CD pipeline**. The website is hosted on **Amazon S3**, distributed through **Amazon CloudFront**, automatically deployed using **AWS CodePipeline**, monitored with **Amazon CloudWatch**, and integrated with **Amazon SNS** for deployment notifications.

The project simulates a real-world cloud deployment workflow where developers push code changes to GitHub and AWS automatically deploys the updated website to production without manual intervention.

---

## Objectives

* Host a static website on AWS.

* Configure a secure CloudFront distribution.

* Implement automated deployment using CI/CD.

* Monitor deployment activities and website health.

* Send notifications for pipeline events.

* Apply AWS security best practices using IAM and OAC.

* Gain practical hands-on experience with AWS DevOps services.

---

## AWS Services Used

| Service               | Purpose                                        |
| --------------------- | ---------------------------------------------- |
| **Amazon S3**         | Static website hosting                         |
| **Amazon CloudFront** | Global CDN and HTTPS delivery                  |
| **AWS CodePipeline**  | Continuous Integration / Continuous Deployment |
| **Amazon CloudWatch** | Monitoring, metrics, dashboards, and alarms    |
| **Amazon SNS**        | Email notifications for deployment events      |
| **AWS IAM**           | Secure access management                       |
| **GitHub**            | Source code repository                         |

---

## Architecture

```
Developer
    |
    v
GitHub Repository
    |
    v
AWS CodePipeline
    |
    v
Amazon S3 Website Bucket
    |
    v
Amazon CloudFront
    |
    v
End Users / Browsers
```

---

## Detailed Description

### 1. Source Code Management

The website source code is stored in a GitHub repository. All HTML, CSS, JavaScript, and image files are version-controlled, allowing easy collaboration, rollback, and change tracking.

### 2. Continuous Integration and Deployment

Whenever a developer pushes changes to the GitHub repository, AWS CodePipeline automatically detects the update. The pipeline fetches the latest source code and deploys it to the S3 bucket. This eliminates manual uploads and ensures consistent deployments.

### 3. Static Website Hosting

Amazon S3 is configured for static website hosting. It stores the website files with high durability and availability, making it suitable for hosting lightweight web applications and portfolio websites.

### 4. Global Content Delivery

Amazon CloudFront acts as a Content Delivery Network (CDN). It caches website content at edge locations around the world, reducing latency and improving page load times for users in different geographic regions.

### 5. Security Implementation

The project uses **CloudFront Origin Access Control (OAC)** to securely access the S3 bucket through CloudFront instead of exposing the bucket publicly. IAM policies follow the **least-privilege principle**, granting only the permissions required for deployment and monitoring.

### 6. Monitoring and Notifications

Amazon CloudWatch collects pipeline metrics and deployment information. Dashboards provide operational visibility, while alarms can be configured for failures or abnormal conditions. Amazon SNS sends email notifications whenever deployment events occur.

---

## Key Features

* Static website hosting on Amazon S3

* Automated deployment from GitHub

* Global CDN acceleration with CloudFront

* HTTPS content delivery

* CloudWatch monitoring dashboard

* Deployment notifications through SNS

* IAM-based secure access control

* Production-style CI/CD workflow

* Easy scalability and maintenance

---

## Project Structure

```
AWS-Static-Website-Hosting-with-CI-CD/
│
├── website/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── assets/
│       └── images/
│
├── Documentation/
│   ├── cloudfront-distribution.png.jpeg
│   ├── cloudwatch-dashboard.png.jpeg
│   ├── codepipeline-success.png.jpeg
│   └── ...
│
└── README.md
```

---

## Deployment Workflow

1. Developer modifies website files locally.

2. Changes are pushed to GitHub.

3. GitHub triggers AWS CodePipeline.

4. CodePipeline downloads the latest source code.

5. Website files are deployed to the S3 bucket.

6. CloudFront serves the updated content globally.

7. CloudWatch records deployment metrics.

8. SNS sends success or failure notifications.

---

## Live Demo

### CloudFront Production URL

CloudFront securely delivers the website using Origin Access Control (OAC) and provides global content delivery.

https://d3e31jbis4onz6.cloudfront.net


Amazon S3 Static Website Endpoint (Deployment Target)

This endpoint represents the website hosted directly on Amazon S3 and is used to verify successful deployments from AWS CodePipeline.

http://staticwebsite-pipeline4.s3-website.ap-south-1.amazonaws.com

Note: In production, users should access the website through Amazon CloudFront, while the S3 Static Website Endpoint is primarily used for deployment validation and testing.



## Setup Instructions

### Prerequisites

* AWS account

* GitHub account

* Static website files (HTML/CSS/JS)

### Step 1: Create S3 Bucket

* Create a new S3 bucket.

* Enable **Static website hosting**.

* Upload website files.

### Step 2: Create CloudFront Distribution

* Set the S3 bucket as the origin.

* Enable HTTPS.

* Configure Origin Access Control (OAC).

### Step 3: Configure CodePipeline

* Connect GitHub repository.

* Select the deployment branch.

* Configure S3 deployment stage.

### Step 4: Configure Monitoring

* Create a CloudWatch dashboard.

* Add pipeline metrics and alarms.

### Step 5: Configure Notifications

* Create an SNS topic.

* Subscribe your email address.

* Attach the topic to CloudWatch alarms or pipeline events.


## Security Best Practices Implemented

* CloudFront Origin Access Control (OAC)

* Least-privilege IAM policies

* HTTPS delivery through CloudFront

* Restricted S3 bucket access

* Version-controlled infrastructure configuration

---

## Performance Benefits

* Reduced latency through edge caching

* Lower origin load on S3

* Faster global content delivery

* High availability and durability

* Scalable architecture for increased traffic



**Manasa Lakshmi Penugonda**

GitHub: https://github.com/Manasa-266/Static_Website-CICD

