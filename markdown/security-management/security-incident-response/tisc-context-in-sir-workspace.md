---
title: Send Observables to TISC
description: Using this feature the security analyst can push the observables data from SIR to TISC. Using the TISC Context, you can check if the observables are present in TISC, if not security analyst can push the data whenever required.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Send Observables to TISC

Using this feature the security analyst can push the observables data from SIR to TISC. Using the TISC Context, you can check if the observables are present in TISC, if not security analyst can push the data whenever required.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to the **Related Records** tab on the SIR workspace to perform the TISC integration capability action.

    **Note:**

    -   You can also navigate to the **Investigation** tab, and navigate to the **Entry Points Lists** section displayed on the left side of the page and select **Associated Observables** to perform the push operation.
    -   On the **Investigation** tab, click **View Related Info** to view all the associated threat lookup, sighting search, and enrichment data for the selected observable. For more information, see [Explore Investigation Canvas](../../secops-analyst-workspace/concept/explore-investigation-in-sir-workspace.md).
2.  For example, select **Threat Intel** &gt; **Associated Observables** to perform the push operation and manually push the data into TISC.

3.  Select one or more observable record to perform **Send Observable to TISC** operation to push the data.

    ![SIR Workspace - Send Observable to TISC](../image/sir-send-to-tisc-observables-page.png)

4.  Click **Send Observable to TISC**.

    **Note:**

    -   If the selected observable isn’t present in TISC, then first the observable will be created as observable source and then once source observable creates TISC observable record, the observable record will be automatically associated with the newly created observable.
    -   Once the observable push operation is performed, then an information message is displayed that `Observable 0.0.0.0 is successfully pushed to TISC. It may take sometime to convert to reflect in TISC context tab`.
    ![Send to TISC Push observable operation](../image/sir-send-to-tisc-results.png)

5.  Select **TISC Context**.

    **Note:** :

    -   You will now see the observable that is pushed to TISC from SIR application.

        ![View observables associated info.](../image/tisc-context-associate-observables.png)

    -   **In a manual push operation**: The observable data can only be pushed if they are linked to the security incidents. Once the observable is pushed from SIR then that data can be identified using sources which will have reference to security incident linked to the observable.
    -   **In an automatic push operation**: The observable or enrichment data will be pushed automatically when it is associated to security incident.
    -   **TISC Context** shows all the SIR associated observable which are also present in TISC.
    -   Using TISC context, the SIR analysts can see all the TISC Enrichment data including Threat Lookups, Sighting Search, and Observable Enrichment Results.
    -   **View Associated Info** will show all the associated observable enrichment data of the selected observables.
6.  View the results.


**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add security incident to TISC case](add-incident-to-case.md)

[Add observables to TISC Case](observables-to-case.md)

[Send Threat Lookup to TISC](send-threat-lookup-to-tisc.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

[Send Observable Enrichment to TISC](send-observable-enrichment-to-tisc.md)

[View TISC Context in SIR Workspace](view-tisc-enrichment-results-from-sirw.md)

