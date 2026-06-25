---
title: Timeline in Security Incident Response Workspace
description: The timeline provides a chronological view of events related to a security incident. Events appear as point events or range events. Administrators can configure which events appear on the timeline and what details are shown in event popovers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/timeline-sir-workspace.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [security incident timeline, timeline events]
breadcrumb: [Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Timeline in Security Incident Response Workspace

The timeline provides a chronological view of events related to a security incident. Events appear as point events or range events. Administrators can configure which events appear on the timeline and what details are shown in event popovers.

Point events appear as a single marker at a specific time. Range events appear as a bar spanning a duration, such as state transitions.

## Base system timeline events

The base system provides 13 predefined event configurations.

|Name|Event Type|
|----|----------|
|Approvals|Point|
|Assignment Group Change|Point|
|Capability Executions|Point|
|Incident Created|Point|
|Incident Closed|Point|
|Incident Re-assigned|Point|
|MITRE ATT&amp;CK Mapping|Point|
|MITRE D3FEND Mapping|Point|
|Observable Added|Point|
|Playbook Executions|Point|
|State Changed|Range|
|Task Closed|Point|
|Task Opened|Point|

**Note:** You can modify base system event configurations or create custom configurations to suit your organization's requirements.

-   **[Configure timeline event configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/configure-timeline-events-sir.md)**  
Create or modify timeline event configurations to control which events appear on the security incident timeline.

**Parent Topic:**[Configuring SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/configuring-security-incident-response-workspace.md)

**Related topics**  


[Set up view of SIR Records]()

[Configure SI design time investigation]()

[SIR Workspace Related Records]()

[Define the new Risk Score Calculator Rules]()

[Configure Shift Handover]()

[Security Incident Response conference call integration]()

[Configure report templates in Security Incident Response]()

[On-Call scheduling in Security Incident Response]()

[Category management in Security Incident Response]()

[View and update Security Incident Response system properties]()

[Create quick filters for Security Incidents and Response Tasks lists]()

