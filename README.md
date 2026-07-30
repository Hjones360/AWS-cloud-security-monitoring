# AWS Cloud Security Monitoring

## Overview
A complete AWS cloud security monitoring pipeline built using native AWS services. 
This project demonstrates how to capture, store, analyze, and alert on security 
events in an AWS environment.

## Pipeline Architecture
CloudTrail → S3 → CloudWatch Logs → Metric Filter → CloudWatch Alarm → SNS Email Alert

## Services Used
- **AWS CloudTrail** — captures every API call made in the AWS account
- **Amazon S3** — stores CloudTrail logs in compressed JSON format
- **Amazon CloudWatch Logs** — receives CloudTrail events in real time
- **CloudWatch Metric Filter** — detects root account usage pattern
- **CloudWatch Alarm** — fires when root account activity is detected
- **Amazon SNS** — sends email alert when alarm triggers

## What Was Built
1. Multi-region CloudTrail trail logging all AWS API activity
2. S3 bucket storing compressed CloudTrail logs automatically
3. CloudWatch Logs integration receiving events in real time
4. IAM user creation captured as provisioning audit log
5. Root account usage metric filter and alarm
6. SNS email notification confirmed working end to end

## Detection Rule
Root account usage alert fires when:
{ $.userIdentity.type = "Root" && $.userIdentity.invokedBy NOT EXISTS && $.eventType != "AwsServiceEvent" }

## Compliance Relevance
- SOC 2 — CC6.1 Logical access controls and privileged account monitoring
- PCI DSS — Requirement 10 track and monitor all access to sensitive data
- CIS AWS Benchmark — CIS 3.3 root account usage metric filter and alarm

## Documentation
Full project report: AWS_Cloud_Security_Monitoring.pdf

## Author
Houston Jones | Atlanta, GA
GitHub: Hjones360
Medium: medium.com/@agentjones
