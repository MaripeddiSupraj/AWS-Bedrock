# AWS Bedrock Learning Repository

Welcome! This repo is where I’m capturing my learnings as I explore AWS Bedrock—from setup to simple inference calls.

## 📋 Table of Contents

1. [What Is AWS Bedrock](#what-is-aws-bedrock)  
2. [Prerequisites](#prerequisites)  
3. [Setup](#setup)  
   - [AWS CLI & IAM](#aws-cli--iam)  
   - [Python SDK (boto3)](#python-sdk-boto3)  
4. [Basic Usage](#basic-usage)  
   - [Listing Available Models](#listing-available-models)  
   - [Text Generation Example](#text-generation-example)  
5. [Next Steps](#next-steps)  
6. [Resources](#resources)

---

## What Is AWS Bedrock

AWS Bedrock is a fully managed service that lets you build and scale generative AI applications using foundation models (FMs) from leading providers (e.g., Amazon, Anthropic, AI21). You don’t manage infrastructure—just pick a model and call it.

---

## Prerequisites

- An **AWS Account** with Bedrock access enabled  
- **AWS CLI** installed and configured (`aws configure`)  
- **Python 3.8+**  
- IAM permissions: at minimum  
  ```json
  {
    "Version": "2012-10-17",
    "Statement": [
      {
        "Effect": "Allow",
        "Action": [
          "bedrock:InvokeModel",
          "bedrock:ListModels"
        ],
        "Resource": "*"
      }
    ]
  }
