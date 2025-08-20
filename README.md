# AWS IAM & Security Project

## Goal
Demonstrate IAM user creation, custom policies, and least privilege principle.

## Users
- **DeveloperUser**: Full access to EC2 and S3 only.
- **AuditorUser**: Read-only access to all AWS services.

## Policies
- DeveloperUser: Custom inline policy (ec2:* , s3:*).
- AuditorUser: AWS managed policy (ReadOnlyAccess).

## Test Cases
- DeveloperUser can create EC2/S3 resources ✅
- DeveloperUser cannot create IAM user ❌
- AuditorUser can view EC2/S3 but cannot modify ✅
- AuditorUser cannot launch EC2 instance ❌

## Architecture Diagram
DeveloperUser → EC2 + S3 (Full Access)
AuditorUser → All Services (Read-Only)
