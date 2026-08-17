# AWS Cloud Security Monitoring

## Overview
A collection of AWS cloud security monitoring projects using native AWS services. 
Each project demonstrates real-world security monitoring, threat detection, and 
incident response in a cloud environment.

## Projects

### Project 1 — CloudTrail & CloudWatch Security Pipeline
Complete AWS audit logging and alerting pipeline.
- CloudTrail capturing all API calls across all regions
- S3 storing logs in compressed JSON format
- CloudWatch Logs receiving events in real time
- Metric filter detecting root account usage
- CloudWatch Alarm firing when root account is used
- SNS email notification confirmed working end to end

**Documentation:** AWS_Cloud_Security_Monitoring.pdf

### Project 2 — GuardDuty Threat Detection Lab
AWS native threat detection investigation and SOC response.
- Enabled GuardDuty with 30-day free trial
- Generated and analyzed 410 sample findings
- Investigated High severity EC2 Command & Control
