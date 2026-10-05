# 🛡️ AWS Cloud Threat Detection & Monitoring Lab

## 📌 Project Overview:
This project is a hands-on AWS Cloud Security lab focused on building a cloud threat detection and monitoring workflow.
The lab demonstrates how AWS security and monitoring services can be used to collect activity logs, detect potential security threats, investigate security findings, and generate automated notifications.

The project will use services including **AWS CloudTrail, Amazon GuardDuty, Amazon EventBridge, and Amazon SNS** to build and validate a basic cloud security monitoring pipeline.

## 🎯 Project Objectives:
- Configure AWS CloudTrail for visibility into AWS API activity.
- Enable Amazon GuardDuty for managed threat detection.
- Generate safe sample security findings for testing.
- Analyze and investigate GuardDuty findings.
- Configure Amazon SNS for security notifications.
- Use Amazon EventBridge to route security findings.
- Build an automated threat notification workflow.
- Validate the monitoring pipeline using controlled test findings.
- Document security controls, findings, and investigation results.

## 🛠️ AWS Services Used:
## Service : Purpose
 1. AWS CloudTrail : Records AWS API and account activity for auditing and investigation.
 2. Amazon GuardDuty : Detects potentially malicious or unauthorized activity.
 3. Amazon EventBridge : Routes security events based on defined rules.
 4. Amazon SNS : Delivers security notifications.
 5. AWS IAM : Provides identity and access control.

## 🔐 Security Concepts Demonstrated:
- Cloud activity logging
- Threat detection
- Security monitoring
- Event-driven security
- Automated alerting
- Security investigation
- Least privilege
- Detection and response workflow

## 🔐 Security Implementation

### 1. AWS CloudTrail Activity Logging:
AWS CloudTrail was configured to provide audit visibility into AWS account activity and management API operations.
CloudTrail Event History was reviewed to understand how AWS records account activity, including event names, event sources, timestamps, identities, regions, and affected resources.

A dedicated trail named `cloud-security-monitoring-trail` was created for the security monitoring lab.

The trail was configured with:
- Management event logging enabled.
- Read management events enabled.
- Write management events enabled.
- Dedicated Amazon S3 storage for CloudTrail log delivery.
- CloudTrail log file validation enabled.
- SNS log-delivery notifications left disabled because security alerting will be implemented separately using Amazon GuardDuty, EventBridge, and Amazon SNS.

This configuration establishes an audit logging layer that can support security monitoring and incident investigation.

#### Evidence
**CloudTrail Event History**
![CloudTrail Event History](Screenshots/CloudTrail/(1)-Screenshot-of-CloudTrail-Eventhistory.png)

**CloudTrail Trail Configuration**
![CloudTrail Trail Configuration](Screenshots/CloudTrail/(2)-Screenshot-of-new-CloudTrail-created.png)
