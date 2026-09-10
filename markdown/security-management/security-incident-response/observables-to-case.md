---
title: Add observables to TISC Case
description: Add observables to TISC case records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/observables-to-case.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add observables to TISC Case

Add observables to TISC case records.

## Before you begin

Role required: sn\_si.analyst, sn\_sec\_tisc.case\_write

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Locate and open any specific security incident that you're investigating.

    This can also be done by searching for the incident ID or browsing from Quick Filters section or filtering through incident state.

3.  Select the **Related Records** tab on the workspace.

    You can perform the action of adding observables to TISC case\(s\) using various tabs from the Security Incident Response Workspace.

    **Note:** You can navigate through:

    -   **Observables details** page from the **Related Records** tab
    -   **Investigation** &gt; **Entry Points Lists** &gt; **Associated Observables**
4.  Select the observables to add to case records.

    **Note:** You can also select an Observable record to open the Observables details page in a different tab and add case records.

5.  Select **Add to TISC Case**.

6.  In the **Link TISC Case** dialog box, select the cases to link the artifacts.

    \[Omitted image "tisc-link-artifacts.png"\] Alt text: Link artifacts to TISC case

7.  Select **Link**.

    The linked case is displayed in the **TISC Cases** list. Select the case record to view the case in the TISC Workspace. You can also select the case record from the security incident **Activity** stream.

8.  Select **Create new TISC case** to create a TISC case within the workflow.


**Parent Topic:**[Send data from SIR Workspace to TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data]()

[Add security incident to TISC case]()

[Send Observables to TISC]()

[Send Threat Lookup to TISC]()

[Send Sighting Search to TISC]()

[Send Observable Enrichment to TISC]()

