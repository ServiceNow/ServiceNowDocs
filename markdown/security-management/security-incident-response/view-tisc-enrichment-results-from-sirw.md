---
title: View TISC Context in SIR Workspace
description: View TISC Context under an incident in SIR workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View TISC Context in SIR Workspace

View TISC Context under an incident in SIR workspace.

## Before you begin

Role required: sn\_sec\_tisc.analyst, sn\_sec\_tisc.sir\_enrichment\_data\_writer

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select any observable\(s\) record.

3.  View the **Source** column.

    After the TISC Context is set in SIR, the **Source** observables that are linked to the security incident and the same is displayed under the Source column.

4.  Alternatively, click on the pushed observable record, which will take you to the Enrichment Results section for the TISC records.

5.  View the **Enrichment Results** tab.

    The **Enrichment Results** tab displays the TISC integrations enrichment results.

    **Note:**

    -   As the enrichment data is only in context to observable and not Security incident, you will only see source as security incident response.
    -   The enrichment data generated from TISC will have TISC as source.
    -   Using ingestion type column we can identity if the record is pushed manually or automatically.
    |Enrichment Name|Description|
    |---------------|-----------|
    |Threat Lookup Results|Lists all the associated threat lookup results for an observable enrichment record.|
    |Sightings|Lists all the associated sightings for an observable.|
    |Observable Enrichment Results|Lists all the associated observable enrichment results for an observable.|


**Parent Topic:**[Send data from SIR Workspace to TISC](../concept/send-sir-to-tisc.md)

**Related topics**  


[System properties to send data](../reference/tisc-integrations-system-properties.md)

[Add security incident to TISC case](add-incident-to-case.md)

[Add observables to TISC Case](observables-to-case.md)

[Send Observables to TISC](tisc-context-in-sir-workspace.md)

[Send Threat Lookup to TISC](send-threat-lookup-to-tisc.md)

[Send Sighting Search to TISC](send-sighting-search-to-tisc.md)

[Send Observable Enrichment to TISC](send-observable-enrichment-to-tisc.md)

