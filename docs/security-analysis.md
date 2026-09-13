AWS Security Analysis

Overview

The AWS Cloud Security & Forensics Lab demonstrated how native AWS security services can work together to provide visibility, detection, investigation, and response capabilities.

The lab focused on CloudTrail logging, S3 data-event monitoring, EventBridge detection, IAM access controls, and security monitoring.

CloudTrail

AWS CloudTrail provides an important source of security and forensic information by recording API activity.

Relevant information available in CloudTrail events includes:

- Event time
- User identity
- Event source
- Event name
- Source IP address
- Request parameters
- Response information

This information can help security analysts reconstruct activity and determine which identity performed a particular action.

S3 Data-Event Monitoring

Standard management-event logging does not provide the same visibility into every object-level operation performed against Amazon S3.

For this reason, S3 data events were configured for the investigation.

Monitoring S3 data activity can provide additional visibility into actions involving objects and can be useful when investigating unauthorized access or suspicious activity involving sensitive data.

EventBridge Detection

Amazon EventBridge was used to create an event pattern capable of identifying specific security-relevant activity.

This approach demonstrates how cloud environments can move beyond passive logging toward automated detection.

When a matching event occurs, EventBridge can route the event to an appropriate target for further processing, alerting, or response.

IAM Security

Identity and Access Management is a critical component of cloud security.

The investigation considered:

- Which identity performed an action.
- What permissions were associated with the identity.
- Whether the activity was expected.
- How excessive permissions could increase the impact of compromised credentials.

The principle of least privilege should be applied so that identities receive only the permissions necessary to perform their legitimate tasks.

Detection vs. Investigation

Logging and detection serve different purposes.

Logging provides a record of activity.

Detection identifies activity that may require attention.

Investigation provides context and determines whether the activity represents a genuine security concern.

The lab demonstrated how these capabilities can work together.

Incident Response Considerations

If suspicious activity is confirmed, potential response actions may include:

1. Identify the affected identity.
2. Review recent activity.
3. Determine the scope of the activity.
4. Restrict or revoke inappropriate access where necessary.
5. Preserve relevant logs for investigation.
6. Monitor for additional suspicious activity.
7. Document the incident and lessons learned.

Response actions should be carefully controlled to avoid unnecessarily disrupting legitimate services.

NIST Cybersecurity Framework Alignment

The project aligns particularly with the Detect and Respond functions of the NIST Cybersecurity Framework.

Detect

- Continuous security monitoring
- Event analysis
- Audit logging
- Identification of anomalous activity

Respond

- Investigation of security events
- Containment considerations
- Access control
- Security alerting

Security Improvements

Based on the lab, organizations can strengthen cloud security by:

- Enabling appropriate CloudTrail logging.
- Monitoring sensitive S3 data events.
- Applying least-privilege IAM permissions.
- Creating automated detection rules.
- Centralizing security monitoring.
- Regularly reviewing cloud identities and permissions.
- Maintaining sufficient logs for forensic investigations.

Conclusion

The lab demonstrated that effective AWS security requires more than simply enabling logging.

Security teams need appropriate visibility, meaningful detection rules, identity controls, investigation procedures, and response capabilities working together.

The combination of CloudTrail, S3 data-event monitoring, EventBridge, IAM, and security monitoring provides a foundation for investigating and responding to suspicious activity in an AWS environment.
