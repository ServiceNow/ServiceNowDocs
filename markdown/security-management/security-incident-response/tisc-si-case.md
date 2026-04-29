---
title: Add observables to TISC Case
description: Use this section to add security incidents or observables to a TISC case.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with TISC Context, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add observables to TISC Case

Use this section to add security incidents or observables to a TISC case.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **All**.

2.  Locate and open any specific security incident that you are investigating.

    This can also be done by searching for the incident ID or filtering using Quick Filters section or browsing through an incident state.

3.  Select **TISC Context** tab.

4.  Click **Add to TISC Case** button.

    Add to TISC Case dialog box displays and this only shows the TISC cases where the record is not already associated.

5.  Select the observables.

6.  Select case\(s\) and click **Add** to add the cases to the observables and associate them to the security incident.

    ![Add to TISC Case from SIR Workspace.](../image/tisc-sirw-add-to-tisc-case.png)

    **Note:** You can also create a new case by clicking on **Create new TISC Case**, in case if you don't have any existing cases.

    The following confirmation messages are displayed:

    -   The following observables are added as artifacts successfully.
    -   The following observables are sent to TISC and will be subsequently be added to the selected TISC case\(s\) records.
    **Note:** The processing and association of the observables activities are posted in the activity stream as and when the association is completed.

7.  View the associated case records by logging into Threat Intelligence Security Center Workspace for further steps.

    For more information see, [TISC integration with SIR Workspace](../concept/tisc-integration-with-sir-workspace.md).

    **Note:**

    From the Security Incident Response workspace, you can also associate observables to case records from the **Investigation** and **Related Records** tabs.

    **Note:** To associate observables from **Investigation**, follow the below procedure and to associate from **Related Records** explained here [Add observables to TISC Case](observables-to-case.md).You can also navigate to the **Investigation** tab, and navigate to the **Entry Points Lists** section displayed on the left side of the page and select **Associated Observables** to add observables to TISC case.


**Parent Topic:**[Working with TISC Context](../../secops-analyst-workspace/concept/working-with-tisc-context.md)

