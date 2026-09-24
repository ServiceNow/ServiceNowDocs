---
title: Process Mining Workspace for Security Incident Response
description: Process Mining scan through security incident audit logs and identify factors contributing to inefficiencies such as multiple reassignments, prolonged hold times, and periods of inactivity for security incidents. Organizations can use this information to address the inefficiencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/sir-process-mining.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Process Mining Workspace for Security Incident Response

Process Mining scan through security incident audit logs and identify factors contributing to inefficiencies such as multiple reassignments, prolonged hold times, and periods of inactivity for security incidents. Organizations can use this information to address the inefficiencies.

With process mining, you can identify the following opportunities of improvements for your security incidents.

|Opportunity|Description|
|-----------|-----------|
|Incidents with at least two assignment group changes|Incidents for which the assignment group changed for two or more times.|
|SIRT \(Max repetitions is 2\)| |
|Incidents took over 5 hours to escalate to high priority|Incidents for which the priority was escalated to a higher priority after five hours.|
|Incidents took more than 5 hours to analyze|Incidents that were in analysis state for more than five hours.|
|Incidents analyzed within 30 minutes|Incidents that were in analysis state for less than 30 minutes.|
|Review \(Max repetitions is 2\)|Incidents that were move to review state for two times.|
|Eradicate \(Max repetitions is 2\)|Incidents that were move to eradicate state for two times.|

The Process Mining Content Pack for Security Incident Response adds a prebuilt project that includes a predefined process model definition for security incidents. To create a project, see [Create process mining project for security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/create-proj-proc-min-sir.md).

**Note:** Beginning with the Brazil release, the Process Mining Content Pack application is set to be part of the core ServiceNow AI Platform and is automatically installed for Security Incident Response. To auto-install the Process Mining Content Pack application, upgrade your instance to Brazil.

Support for the standalone SIR Process Mining Content Pack \(com.sn\_sir\_process\_mining\_cp\) ends with this change; it remains active on upgrade, but is no longer supported.

