---
title: Mapping Symantec DLP incident statuses with ServiceNow incident Status
description: Synchronize the status of the DLP incidents ingested on the ServiceNow with the DLP incidents of the Symantec. Map the ServiceNow Incident Status field with the Symantec Incident Status field.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a profile for Symantec DLP integration, Symantec Integration for Data Loss Prevention Incident Response, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Mapping Symantec DLP incident statuses with ServiceNow incident Status

Synchronize the status of the DLP incidents ingested on the ServiceNow with the DLP incidents of the Symantec. Map the **ServiceNow Incident Status** field with the **Symantec Incident Status** field.

## Before you begin

Role required: sn\_dlir.admin

## About this task

The incident status is retrieved dynamically from the Symantec Endpoint Source which is added in the mapping. You need to perform a one-to-one incident status mapping.

## Procedure

1.  Navigate to **Symantec DLP integration** &gt; **Incident Status mapping**.

2.  Provide a **Name** to identify the mapping.

3.  Select the **Source** integration from where you want to fetch the status.

4.  Map the **DLP Incident Status** with **Symantec Incident Status**.

    **Note:** It is not necessary to map all the states, you can map only the required states.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the mapping record.|
    |Source|The configured Symantec Endpoint source from where you want to fetch the incident status.|
    |DLP Incident Status|List of Status of DLP incidents.|
    |Symantec Incident Status|List of Status fetched from the Source \(Symantec Endpoint\).|

    ![DLP Status mapping](../image/dlp-status-mapping.png)

5.  Click **Submit**.


## Result

After successfully creating the record for mapping statuses of the ServiceNow incidents, the ServiceNow incidents status will be synced with Symantec DLP incidents status.

If you change the status of any DLP incident on your ServiceNow instance, then the status of associated Symantec DLP incidents will be changed on the source Symantec platform based on the mapping set in the record.

**Parent Topic:**[Create a profile for Symantec DLP integration](create-profile-symantec-dlp.md)

