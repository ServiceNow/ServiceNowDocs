---
title: Configure advanced settings for Elasticsearch data inputs
description: Configure advanced settings for data inputs used for streaming log data from Elasticsearch indices to your instance.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Advanced data input configuration, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure advanced settings for Elasticsearch data inputs

Configure advanced settings for data inputs used for streaming log data from Elasticsearch indices to your instance.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can set system parameters for reading log data that determine the actions that the system performs on log data arriving on the MID Server. For example, you can set the time zone to use if a log lacks a timestamp. If no advanced settings are configured, the system uses the default values.

For additional information about streaming logs using the Elasticsearch data input, see the [Stream logs using Elasticsearch data input - Advanced guide \[KB1080162\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1080162) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  Open an Elasticsearch data input record from the Data Inputs table.

    The data input configuration displays.

    **Note:** The number of log sources that the data input has created is shown in the **Sources count** field. For more information about data input sources, see [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md).

    **Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

3.  Select **Advanced** and then select the **Advanced** tab.

4.  On the form, fill in the fields.

    For a description of the fields, see [Elasticsearch data input configuration fields](../reference/hla-data-input-elastic-ref.md).

5.  In the Streaming Sources related list, verify that this data input is streaming log data from all relevant endpoint devices.

    For more information about streaming sources, see [Identify and resolve log streaming issues](hla-data-input-streaming.md).

    **Note:** If you experience permissions-related issues with streaming log data from Elasticsearch, refer to the [Granting privileges for data streams from Elasticsearch \[KB0967366\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=9648a9281b61b4100b8a9979b04bcb04) article in the Now Support Knowledge Base.

6.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

7.  Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    If the data input is configured to run on a MID Server cluster, the system tries to connect all the MID Servers contained in the cluster to the repository. The cluster passes the test if at least one of its MID Servers gets connected. This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. This field displays only when a streaming error has occurred.

        Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

8.  Select **Publish** to publish the data input to the MID Server.


**Parent Topic:**[Advanced data input configuration](../concept/hla-data-input-adv-configuration.md)

**Related topics**  


[Configure Elasticsearch data inputs](hla-data-input-elastic.md)

