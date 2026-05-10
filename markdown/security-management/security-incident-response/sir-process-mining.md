---
title: Process Mining Workspace for Security Incident Response
description: Process Mining scan through security incident audit logs and identify factors contributing to inefficiencies such as multiple reassignments, prolonged hold times, and periods of inactivity for security incidents. Organizations can use this information to address the inefficiencies.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
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

The Process Mining Content Pack for Security Incident Response adds a prebuilt project that includes a predefined process model definition for security incidents. To create a project, see [Create process mining project for security incidents](../task/create-proj-proc-min-sir.md).

**Note:** To use the Process Mining in Security Incident Response, download and install the content pack. For more information, see [Content pack for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/sir-proc-min-content-pack.md).

