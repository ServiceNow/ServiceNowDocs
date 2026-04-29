---
title: Send Threat Lookup to TISC
description: Using this feature the security analyst can push the threat lookup data from SIR to TISC. Using the TISC Context, you can check if the threat lookup results are present in TISC, if not security analyst can push the data whenever required.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Send Threat Lookup to TISC

Using this feature the security analyst can push the threat lookup data from SIR to TISC. Using the TISC Context, you can check if the threat lookup results are present in TISC, if not security analyst can push the data whenever required.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to the **Related Records** tab on the SIR workspace to perform the TISC integration capability action.

    **Note:**

    -   You can also navigate to the **Investigation** tab, and navigate to the **Entry Points Lists** section displayed on the left side of the page and select **Associated Observables** to perform the push operation.
    -   On the **Investigation** tab, click **View Associated Info** to view all the associated threat lookup, sighting search, and enrichment data for the selected observable. For more information, see [Explore Investigation Canvas](../../secops-analyst-workspace/concept/explore-investigation-in-sir-workspace.md).
2.  Select **Threat Intel** &gt; **Threat Lookup Results** to perform the push operation and manually push the data into TISC.

3.  Select one or more Threat Lookup Results record.

4.  Click **Send Results to TISC**.

    ![Send Results to TISC](../image/tisc-send-threat-results-to-tisc.png)

    **Note:**

    -   If the selected Threat Lookup observable isn't present in TISC, then in manual mode first the observable is created as observable source and then once source observable creates TISC observable record, the observable record will be automatically associated with the newly created observable. Also, selected threat lookup will also be pushed to the newly created threat lookup observable in manual mode.
    -   In an automatic mode, the observables will not be pushed if the observable is present, then the threat lookups will be pushed automatically. If the observables are not present, then the threat lookups will not be pushed.
5.  A confirmation message is displayed that `The observable (1.9.78.242) for the selected threat lookup record does not exist in TISC. It will take sometime to create observable and to automatically associate the observable threat lookup record in TISC.`

    Once this is processed and pushed, you can see the results.

6.  Select **TISC Context**.

    **Note:** :

    -   You will now see the observable that is pushed to TISC from SIR application.

        ![TISC Context](../image/tisc-threat-lookup-results-tisc-context.png)

    -   **In a manual push operation**: The observable data can only be pushed if they are linked to the security incidents. Once the observable is pushed from SIR then that data can be identified using sources which will have reference to security incident linked to the observable.
    -   **In an automatic push operation**: The observable or enrichment data will be pushed automatically when it is associated to a security incident.
    -   **TISC Context** shows all the SIR associated observable which are also present in TISC.
    -   Using TISC context, the SIR analysts can see all the TISC Enrichment data including Threat Lookups, Sighting Search, and Observable Enrichment Results.
    -   **View Associated Info** will show all the associated observable enrichment data of the selected observables.
7.  The list view displays all the threat lookup results, however select any record and click on **View Associated Info** button.

8.  View the threat lookup results.

9.  Click on any threat lookup results record to view the record in the form view, which also shows the push or **Ingestion Type** \(automatic or manual\) and **Source** will be Security Incident Response.

    ![View threat lookup results](../image/tisc-threat-lookup-view-results.png)


**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add security incident to TISC case](add-incident-to-case.md)

[Add observables to TISC Case](observables-to-case.md)

[Send Observables to TISC](tisc-context-in-sir-workspace.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

[Send Observable Enrichment to TISC](send-observable-enrichment-to-tisc.md)

