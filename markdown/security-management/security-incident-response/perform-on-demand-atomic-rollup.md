---
title: Perform on demand atomic rollup
description: Rollup framework cannot handle updates to the existing linked records. In such cases, on demand atomic rollup should happen for linked records, which can be achieved via business rules.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform on demand atomic rollup

Rollup framework cannot handle updates to the existing linked records. In such cases, on demand atomic rollup should happen for linked records, which can be achieved via business rules.

To capture updates to the linked records, business rules must be created on the source table.

These business rules work on insert, update, and delete operations. When you perform insert or update, you need to add or update rolled up information to MSI. If you delete then the rolled up information will be removed from MSI.

For example, once a security incident is linked to MSI, the related information will be rolled up automatically MSI. But later, if you add a new observable to an MSI, then the newly added observable also will be rolled up to MSI. Here, **Sync rolled up observable** business rule captures the update and rollup the updated record to MSI. Similarly, the same business rule also handles the removal of the existing rolled up observables, if it gets removed from the security incident.

|Rule|Description|
|----|-----------|
|Sync rolled up indicator \(sn\_ti\_m2m\_task\_indicator\)|Use this business rule to handle the rollup and removal of indicator of compromise from Security Incident, Security Case, and Remediation task.|
|Sync rolled up observable \(sn\_ti\_m2m\_task\_observable\)|Use this business rule handles the rollup and removal of linked observables from Security Incident, Security Case, and Remediation task.|
|Sync rolled up affected user \(sn\_si\_m2m\_task\_affected\_user\)|Use this business rule handles the rollup and removal of linked affected users from Security Incident, Security Case and Remediation task.|
|Sync rolled up affected CI \(task\_ci\)|Use this business rule handles the rollup and removal of associated configuration items from Security Incident, Security Case and Remediation task.|

**Parent Topic:**[Rollup Framework for MSIM](roll-up-framework-for-major-security-incident-management.md)

**Related topics**  


[Configure Linked Records in Major Security Incident Management](../task/configuring-linked-records-in-major-security-incident-management.md)

[Configure Rollup Records in Major Security Incident Management](roll-up-record-configuration-in-major-security-incident-management.md)

[Configure List Layout in Major Security Incident Management](list-layout-confguration.md)

[Rollup example use case implementation for a Security Case](use-case-for-a-security-case.md)

