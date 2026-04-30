---
title: Map Proofpoint DLP incidents status with ServiceNow incident status
description: Synchronize the status of the DLP incidents ingested on your ServiceNow instance and DLP incidents of the Proofpoint. Map the ServiceNow Incident status with the Proofpoint Incident status.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Map Proofpoint DLP incidents status with ServiceNow incident status

Synchronize the status of the DLP incidents ingested on your ServiceNow instance and DLP incidents of the Proofpoint. Map the ServiceNow Incident status with the Proofpoint Incident status.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Navigate to **Proofpoint DLP integration** &gt; **Incident** &gt; **Incident Status Mapping**.

2.  Provide a **Name** to identify the mapping.

3.  Select the **Source** \(integration configuration\) tile for which the Status Mapping should be applied.

4.  Map the **ServiceNow DLP incident Status** with **Proofpoint Incident Status**.

    |Field|Description|
    |-----|-----------|
    |Name|Placeholder for the mapping record.|
    |Source|Configured Proofpoint Endpoint source from where you want to fetch the incident status.|
    |ServiceNow Incident Status|List of Status of DLP incidents.|
    |Proofpoint Incident Status|Default mapped values for default states available in DLP incidents. For custom states, the default Proofpoint status is **New**. You can modify and add the required Proofpoint status in the input field.|

    ![Map Proofpoint DLP incident status with ServiceNow Incident status](../../data-loss-prevention/image/dlp-proofpoint-map.gif)

5.  Click **Submit**.


## Result

A record for mapping is successfully created. The statuses of the ServiceNow incidents will be synchronized with Proofpoint DLP incidents.

When you change the status of any DLP incident on your ServiceNow instance, then the status of the associated Proofpoint DLP incident will be changed on the source Proofpoint platform as per the mapping set in the record.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Proofpoint](../concept/dlp-incident-response-integration-proofpoint.md)

