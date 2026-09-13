AWS Security Investigation

Investigation Overview

This document describes the investigation process used during the AWS Cloud Security & Forensics Lab.

The objective was to understand how AWS logging and monitoring services can provide visibility into activity performed within an AWS environment and how security-relevant events can be investigated.

Evidence Source

The primary source of forensic evidence was AWS CloudTrail.

CloudTrail records information about API activity and can provide important details about:

- The time an action occurred
- The identity that performed the action
- The AWS service involved
- The API operation performed
- The source IP address
- Request parameters
- Response information

Relevant Events

During the investigation, API activity including the following events was observed:

GenerateDataKey

"GenerateDataKey" is an AWS Key Management Service API operation associated with generating data keys for encryption operations.

The event was reviewed as part of the wider investigation to understand which identity initiated the activity, when it occurred, and what surrounding actions were taking place.

GetBucketAcl

"GetBucketAcl" is an Amazon S3 API operation used to retrieve the access control list associated with an S3 bucket.

The event was examined to understand the identity making the request and the context in which the request occurred.

Investigation Process

The investigation followed a basic cloud-forensics workflow:

1. Review the available CloudTrail events.
2. Identify the AWS identity associated with each event.
3. Examine the event timestamp.
4. Review the source IP address.
5. Identify the AWS service and API operation involved.
6. Examine request and response information where available.
7. Consider whether the activity was expected or potentially suspicious.
8. Identify appropriate security controls and response actions.

Security Considerations

A single API event should not automatically be considered malicious.

Security analysts should examine the surrounding activity and consider factors such as:

- Whether the identity normally performs the action.
- Whether the source IP address is expected.
- Whether the timing is unusual.
- Whether multiple related API calls occurred.
- Whether the activity involves sensitive resources.
- Whether the account or credentials may have been compromised.

Detection and Response

The investigation demonstrated how CloudTrail logs can serve as a foundation for cloud-security monitoring.

EventBridge can complement CloudTrail by identifying predefined security-relevant events and triggering automated workflows.

Appropriate response actions may include:

- Investigating the affected identity.
- Reviewing IAM permissions.
- Restricting suspicious access.
- Preserving relevant logs.
- Monitoring subsequent activity.
- Escalating confirmed incidents.

Conclusion

The investigation demonstrated the importance of cloud-native logging and monitoring when performing security investigations in AWS.

CloudTrail provides the underlying event information, while monitoring and detection mechanisms such as EventBridge can help security teams identify relevant activity more efficiently.
