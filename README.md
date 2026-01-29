# AWS-Deployment

This repository contains two integrated projects focused on securing cloud infrastructure according to industry-standard frameworks like NIST CSF, ISO/IEC 27001, and CIS Controls.

Project 01: IAM Identity Governance & Least Privilege
Objective: Establish a secure foundation by eliminating the use of the Root account and enforcing strictly scoped access for organizational departments.
Key Implementation Steps:
- Account Hardening: Secured the Root account with MFA and created a dedicated TechIndustries-IAM-Admin for daily operations.

- Identity Architecture: Established an AWS Account Alias (techindustriesusers) and configured a forced password reset policy for new users.

- Resource Tagging & RBAC: Deployed EC2 instances with environment tags (Marketing vs. Sales).

- Scoped Policies: Authored custom JSON policies that allow users to view their respective servers but explicitly deny high-risk actions like instance termination.

Project 02: SecOps – Logging, Monitoring & Alerting
Objective: Implement real-time visibility and automated incident response for sensitive cloud resources.
Key Implementation Steps:

- Object Storage Security: Provisioned an S3 bucket for internal documentation, applying varied access levels (Full vs. Read-only) based on group membership.

- Audit Trail: Configured AWS CloudTrail to capture management events and API activity across the entire account for compliance and forensics.

- Automated Detection: Built Amazon EventBridge rules to monitor CloudTrail logs for sensitive S3 actions (e.g., DeleteObject).

- Real-time Alerting: Integrated Amazon SNS to deliver instant security notifications to personnel when a detected event occurs.
