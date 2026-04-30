---
title: Mapping DLP incident status with Netskope
description: The incident status mapping section enables the users to provide the mappings between the DLP Incident status in ServiceNow and Netskope Object status.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Mapping DLP incident status with Netskope

The incident status mapping section enables the users to provide the mappings between the DLP Incident status in ServiceNow and Netskope Object status.

## Before you begin

The mapping will be used when ingesting any DLP incident from Netskope to ServiceNow as well as syncing any state change of DLP incident in ServiceNow back to Netskope.

Synchronize the status of the DLP incidents ingested on the ServiceNow with the DLP incident of Netskope. Map the ServiceNow Incident Status field with the Netskope Object Status field.

Role required: sn\_dlir.admin

## About this task

You need to create a one-to-one incident status mapping of Netskope and ServiceNow status.

## Procedure

1.  Navigate to **Netskope DLP integration** &gt; **Incident status mapping**.

2.  Provide a Name to identify the mapping.

3.  Select the Source integration.

4.  Map the DLP Incident Status with Netskope Object Status \(Duplicate Netskope state can also be mapped\).

    The status sync from ServiceNow to Netskope will be disabled if you don’t create a mapping record.

    **Important:** You need to map all the Netskope object statuses to all ServiceNow statuses. Select the source in order to sync DLP Incident status back to Netskope object.

    The following information and alert messages are displayed when you map the incident status, review the messages and proceed further.

    **Note:**

    -   Status mapping is case-sensitive.
    -   Provide the internal name of the default status \(For example: new, in\_progress, closed\) or exact name of status in case of custom state for the Netskope Object Status fields.
    **Warning:** Do not modify the status on the Netskope platform after completing the status mapping configuration from here.

    ![Netskope DLP incident status mapping.](../image/dlp-netskope-incident-mapping.png)

    |Field|Description|
    |-----|-----------|
    |Name|Name of the mapping record.|
    |Source|The configured Netskope Endpoint source from where you want to sync the incident status.|
    |DLP Incident Status|Indicates the list of DLP incidents status.|
    |Netskope Object Status|Indicates the list of Netskope object status.|

5.  Click **Submit**.


## Result

After successfully creating the record for status mapping, whenever there is an update on ServiceNow DLP incident’s state then it will automatically reflect it on Netskope side as per the mapping.

**Note:** If you change the status of any DLP incident on Netskope tenant directly, then the status sync from SN to Netskope will not work considering the API limitations. Ensure you map all the DLP incident status with Netskope object status carefully.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

