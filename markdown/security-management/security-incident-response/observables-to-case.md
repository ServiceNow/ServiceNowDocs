---
title: Add observables to TISC Case
description: Add observables to TISC case records.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add observables to TISC Case

Add observables to TISC case records.

## Before you begin

Role required: sn\_si.analyst, sn\_sec\_tisc.case\_write

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Locate and open any specific security incident that you are investigating.

    This can also be done by searching for the incident ID or browsing from Quick Filters section or filtering through incident state.

3.  Click on the **Related Records** tab on the workspace.

    You can perform the action of adding observables to TISC case\(s\) using various tabs from the Security Incident Response Workspace.

    **Note:** You can navigate to the

    -   Observables details page from the Related Records tab.
    -   **Investigation** tab, and navigate to the **Entry Points Lists** section displayed on the left side of the page and select **Associated Observables** to add observables to TISC case.
4.  For example, select **Threat Intel** &gt; **Associated Observables**.

5.  Select one or multiple observable\(s\) to add the selected observables to case records.

    **Note:** You can also click on any of the Observable record and it opens Observables details page in a different tab and you can add case records from here by clicking on Add to TISC Case.

6.  Click the **Capability actions** split button.

7.  Select **Add to TISC Case**.

8.  Select the case\(s\) from the **Add to Case** dialog box.

    ![Add to TISC Case.](../image/tisc-add2-case-modal.png)

    **Note:** Create a new TISC case if there no case records. For more information on how to create case\(s\), see [Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md).

9.  Click **Add**.

10. Click the Case record to view the case in TISC from the information message displayed or from the **Activity** stream.

    **Note:** If the observable does not have a corresponding TISC Observable, then the selected observable in SIR workspace will be sent to TISC automatically and will subsequently gets added to the selected TISC case record\(s\). To view the linked observables, click on the particular case record from the **Activity** stream. By clicking on this will take you to the case record in TISC workspace and the observables will get added under **Artifacts** tab of the Case Management module.


## Result

You have successfully send the observables data to Threat Intelligence Security Center case management.

**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add security incident to TISC case](add-incident-to-case.md)

[Send Observables to TISC](tisc-context-in-sir-workspace.md)

[Send Threat Lookup to TISC](send-threat-lookup-to-tisc.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

[Send Observable Enrichment to TISC](send-observable-enrichment-to-tisc.md)

