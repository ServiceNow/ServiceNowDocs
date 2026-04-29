---
title: Send Observable Enrichment to TISC
description: Using this feature the security analyst can push the sighting search data from SIR to TISC. Using the TISC Context, the analyst can check if the sighting search data is present in TISC, if not the security analyst can push the data whenever required.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Send Observable Enrichment to TISC

Using this feature the security analyst can push the sighting search data from SIR to TISC. Using the TISC Context, the analyst can check if the sighting search data is present in TISC, if not the security analyst can push the data whenever required.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to the **Related Records** tab on the SIR workspace to perform the TISC integration capability action.

    **Note:**

    -   You can also navigate to the **Investigation** tab, and navigate to the **Entry Points Lists** section displayed on the left side of the page and select **Associated Observables** to perform the push operation.
    -   On the **Investigation** tab, click **View Associated Info** to view all the associated threat lookup, sighting search, and enrichment data for the selected observable. For more information, see [Explore Investigation Canvas](../../secops-analyst-workspace/concept/explore-investigation-in-sir-workspace.md).
2.  Select **Observable Enrichment** &gt; **Observable Enrichment Results** to perform the push operation and manually push the data into TISC.

3.  Select one or more observable record to perform **Send Results to TISC** operation to push the data.

    ![Send Observable enrichment to TISC](../image/tisc-observable-enrichment-sir.png)

4.  Click **Send Results to TISC**.

    **Note:**

    -   If the selected observable isn’t present in TISC, then first the observable will be created as observable source and then once source observable creates TISC observable record, the observable record will be automatically associated with the newly created observable.
    -   Once the observable push operation is performed, then an information message is displayed that `Observable 0.0.0.0 is successfully pushed to TISC. It may take sometime to convert to reflect in TISC context tab`.
5.  Select **TISC Context**.

    ![Observable Enrichment Results](../image/tisc-context-observables-enrichment-results.png)

    **Note:** :

    -   You will now see the observable that is pushed to TISC from SIR application.
    -   **In a manual push operation**: The observable data can only be pushed if they are linked to the security incidents. Once the observable is pushed from SIR then that data can be identified using sources which will have reference to security incident linked to the observable.
    -   **In an automatic push operation**: The observable or enrichment data will be pushed automatically when it is associated to security incident.
    -   **TISC Context** shows all the SIR associated observable which are also present in TISC.
    -   Using TISC context, the SIR analysts can see all the TISC Enrichment data including Threat Lookups, Sighting Search, and Observable Enrichment Results.
    -   **View Associated Info** will show all the associated observable enrichment data of the selected observables.
6.  View the results.

7.  Click on any observable enrichment results record to view the record in the form view, which also shows the push or **Ingestion Type** \(automatic or manual\) and **Source** will be Threat Intelligence Security Center.

    ![Observable Enrichment Results](../image/tisc-observable-enrichment-result.png)


**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add security incident to TISC case](add-incident-to-case.md)

[Add observables to TISC Case](observables-to-case.md)

[Send Observables to TISC](tisc-context-in-sir-workspace.md)

[Send Threat Lookup to TISC](send-threat-lookup-to-tisc.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

