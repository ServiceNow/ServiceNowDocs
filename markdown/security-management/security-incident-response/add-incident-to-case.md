---
title: Add security incident to TISC case
description: Add security incidents to TISC case records.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add security incident to TISC case

Add security incidents to TISC case records.

## Before you begin

Role required: sn\_si.analyst, sn\_sec\_tisc.case\_write

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Locate and open any specific security incident that you are investigating.

    This can also be done by searching for the incident ID or browsing from Quick Filters section or filtering through incident state.

3.  Click on **More actions** icon.

4.  Click **Add to TISC Case** action.

    Add to TISC Case dialog box displays and this only shows those TISC cases where the incident is not already associated.

5.  Select the case\(s\) from the **Add to Case** dialog box.

    ![Add to TISC Case Modal](../image/tisc-add2-case-modal.png)

    **Note:** Create a new TISC case if there no case records. For more information on how to create case\(s\), see [Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md).

6.  Click **Add**.

7.  Click the Case record to view the case in TISC from the information message displayed or from the **Activity** stream.

    **Note:** To view the linked security incidents, click on the particular case record from the security incident **Activity** stream. By clicking on this will take you to the case record in TISC workspace and the security incidents will get added under **Artifacts** tab of the Case Management module.


**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add observables to TISC Case](observables-to-case.md)

[Send Observables to TISC](tisc-context-in-sir-workspace.md)

[Send Threat Lookup to TISC](send-threat-lookup-to-tisc.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

[Send Observable Enrichment to TISC](send-observable-enrichment-to-tisc.md)

