# AWS IAM Least Privilege Security Lab

## Overview

This lab demonstrates least privilege access control in AWS using IAM, Amazon S3, a custom IAM policy, an IAM user group, and a test IAM user.

The goal was to allow a test user to read from one approved S3 bucket while denying upload, delete, and unrelated AWS service access.

## Lab Objectives

- Create an S3 bucket with a proof file
- Create a custom IAM policy
- Attach the policy to an IAM user group
- Add a test IAM user to the group
- Validate allowed and denied access
- Prove least privilege through screenshots

## Services Used

- AWS IAM
- Amazon S3
- Amazon EC2
- AWS Management Console

## What I Built

I created an S3 bucket containing a test file named `lab-proof.txt`. Then I created a custom IAM policy that allowed read-only access to that specific bucket. The policy was attached to an IAM user group, and a test user named `lab-s3-analyst` was added to the group.

The IAM user was able to access and read the approved S3 object, but was denied when trying to upload files, delete files, or access EC2 instances.

## Security Concepts Demonstrated

- Principle of least privilege
- IAM policy scoping
- Identity-based permissions
- Group-based access management
- S3 read-only access
- Denied action testing
- Security validation through access testing

## Screenshots

### 1. S3 bucket with proof file
![S3 bucket with proof file](screenshots/01-s3-bucket-lab-proof-file.png)

### 2. Custom IAM policy
![Custom IAM policy](screenshots/02-custom-iam-policy.png)

### 3. IAM group with policy attached
![IAM group with policy attached](screenshots/03-iam-group-policy-attached.png)

### 4. IAM user added to group
![IAM user added to group](screenshots/04-iam-user-added-to-group.png)

### 5. IAM user can access approved S3 file
![IAM user can access approved S3 file](screenshots/05-user-can-access-approved-s3-file.png)

### 6. IAM user denied upload access
![IAM user denied upload access](screenshots/06-user-denied-upload-access.png)

### 7. IAM user denied delete access
![IAM user denied delete access](screenshots/07-user-denied-delete-access.png)

### 8. IAM user denied EC2 access
![IAM user denied EC2 access](screenshots/08-user-denied-ec2-access.png)

## Result

This lab successfully demonstrated least privilege access control. The IAM user could only read the approved S3 object and was denied unnecessary permissions, including upload, delete, and EC2 access.
