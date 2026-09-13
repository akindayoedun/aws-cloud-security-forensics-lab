AWS Cloud Security & Forensics Lab

Project Overview

This project documents a hands-on AWS cloud security and forensic investigation lab focused on detecting, investigating and responding to suspicious activity within an AWS environment.

The lab explored how AWS native security services can be used to provide visibility into API activity, monitor data access, identify potentially suspicious behavior and support forensic investigations.

Objectives

- Configure AWS CloudTrail for security and forensic logging.
- Enable monitoring of Amazon S3 data events.
- Analyze CloudTrail events associated with user activity.
- Configure Amazon EventBridge to detect specific security-relevant events.
- Examine IAM activity and access controls.
- Apply security monitoring and incident-response principles.
- Relate the investigation to the NIST Cybersecurity Framework.

AWS Services & Technologies

- AWS CloudTrail
- Amazon S3
- Amazon EventBridge
- AWS IAM
- Amazon CloudWatch
- AWS CLI
- NIST Cybersecurity Framework

Lab Focus

The investigation focused on understanding how AWS activity can be recorded and analyzed to identify potentially suspicious behavior.

Particular attention was given to CloudTrail event information such as:

- "eventTime"
- "userIdentity"
- "eventName"
- "eventSource"
- "sourceIPAddress"
- "requestParameters"
- "responseElements"

Events observed during the investigation included API activity such as:

- "GenerateDataKey"
- "GetBucketAcl"

These events were analyzed in the context of the surrounding activity to understand what actions were being performed and what security implications they could have.

Detection & Monitoring

Amazon CloudTrail was configured to provide visibility into AWS API activity, including Amazon S3 data events.

Amazon EventBridge was configured with an event pattern designed to identify specific security-relevant activity and support automated detection.

The lab demonstrated the importance of continuous monitoring and centralized logging when investigating activity within a cloud environment.

Identity & Access Management

AWS IAM was used to examine identity-based activity and access controls.

The investigation considered how excessive or unexpected permissions could increase the impact of compromised credentials and how access restrictions can support incident containment.

Security Analysis

The lab demonstrated several important cloud-security principles:

1. Visibility is essential for detection.
   Without appropriate logging, suspicious cloud activity can be difficult to investigate.

2. Data events require deliberate monitoring.
   Important activity involving resources such as S3 may require additional CloudTrail data-event configuration.

3. Identity activity provides valuable forensic evidence.
   CloudTrail identity information can help investigators determine which account or principal performed an action.

4. Automated detection improves response time.
   EventBridge can be used to identify specific events and initiate security workflows.

5. Least privilege reduces risk.
   IAM permissions should be limited to the access required for legitimate activities.

NIST Cybersecurity Framework Alignment

This project primarily relates to the following NIST CSF functions:

Detect

- Security monitoring
- Audit logging
- Event analysis
- Identification of potentially suspicious activity

Respond

- Investigation of security events
- Access restriction
- Containment considerations
- Security alerting

Recover

- Lessons learned
- Improving monitoring controls
- Strengthening security configurations following an investigation

Lessons Learned

This project strengthened my understanding of cloud security monitoring and forensic investigation.

Key lessons included the importance of:

- Enabling appropriate cloud logging.
- Understanding AWS API activity.
- Monitoring sensitive data-access events.
- Reviewing IAM permissions.
- Creating automated detection mechanisms.
- Using logs as forensic evidence during security investigations.

Project Limitations

This was a hands-on security laboratory exercise rather than a production AWS environment.

Original screenshots from the exercise are no longer available, so this repository documents the configurations, methodology, findings, and security analysis based on the completed lab rather than presenting reconstructed screenshots or evidence.

Disclaimer

This project was conducted for educational and cybersecurity learning purposes in a controlled environment. No unauthorized systems or resources were targeted.# aws-cloud-security-forensics-lab
Hands-on AWS cloud security and forensic investigation lab focused on CloudTrail, S3 data events, EventBridge, IAM and security monitoring.
