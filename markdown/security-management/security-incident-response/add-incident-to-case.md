---
title: Add security incident to TISC case
description: Add security incidents to TISC case records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/add-incident-to-case.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 2
keywords: [security incident, link incident to case, Security Incident Response Workspace, Threat Intelligence Security Center, case management, security artifacts, incident investigation, TISC workspace, link TISC case]
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add security incident to TISC case

Add security incidents to TISC case records.

## Before you begin

Role required: sn\_si.analyst, sn\_sec\_tisc.case\_write

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Open the security incident you're investigating.

    This can also be done by searching for the incident ID or browsing from Quick Filters section or filtering through incident state.

3.  Select **TISC Context** &gt; **TISC Cases**.

4.  Select **Link**.

    The Link TISC Case dialog box displays the TISC cases where the incident is not already associated.

5.  Select the cases from the list and select **Link**.

    \[Omitted image "link-tisc-case.png"\] Alt text: Link TISC Case

    The linked case is displayed in the **TISC Cases** list. Select the case record to view the case in the TISC Workspace. You can also select the case record from the security incident **Activity** stream.

6.  Select **Create new TISC case** to create a TISC case within the workflow.


**Parent Topic:**[Send data from SIR Workspace to TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data]()

[Add observables to TISC Case]()

[Send Observables to TISC]()

[Send Threat Lookup to TISC]()

[Send Sighting Search to TISC]()

[Send Observable Enrichment to TISC]()

