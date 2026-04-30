---
title: Identify and resolve log streaming issues
description: Identify and address log streaming issues to ensure that the data inputs you have configured for Health Log Analytics are streaming data properly to your ServiceNow instance.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, data input, log data, streaming, fix log streaming issues]
breadcrumb: [Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Identify and resolve log streaming issues

Identify and address log streaming issues to ensure that the data inputs you have configured for Health Log Analytics are streaming data properly to your ServiceNow instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Streaming Sources**.

    The Streaming Sources page shows all data inputs and the MID Servers that are receiving logs from them.

    **Note:**

    -   When **Look up hostnames** is selected in the [advanced data input configuration](../concept/hla-data-input-adv-configuration.md), the Streaming Sources page shows the hostname of devices that use an Rsyslog or a Filebeat shipper. For Elasticsearch indices, it displays the index name.
    -   Streaming Sources is also available as a related list on the data input form. The related list displays only the endpoint devices that are relevant to that data input.
    -   If the HLA engine is down and data has stopped streaming, a notification appears at the top of the Streaming Sources page. When this happens, contact ServiceNow support.
2.  Select a data input record to view the streaming data of its sources and identify streaming issues and their possible cause.

    For example, if the last recorded event time for a data input's endpoint server is yesterday, that server might be down or configured incorrectly. A streaming issue might also be caused by the data input configuration file not being installed on the endpoint.

<table id="table_k2m_wq3_qmb"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

The status of the source. A red bullet indicates that this source has not streamed data in the last hour.

</td></tr><tr><td>

Last event time

</td><td>

The last recorded time an event arrived at the MID Server in the last one-minute interval.Health Log Analytics continuously updates the last event time. If the last event time is not up to date, data is not streaming.

</td></tr><tr><td>

Raw log lines/sec

</td><td>

The average number of raw log lines that streamed to the MID Server per second in the last one-minute interval. **Note:** This value represents the number of raw log lines before preprocessing.

</td></tr><tr><td>

Preprocessed log lines/sec

</td><td>

The average number of preprocessed log lines that streamed to the MID Server per second in the last one-minute interval. **Note:** This value can differ from the number of raw log lines per second. For example, the difference can be a result of logs having been dropped during preprocessing.

</td></tr></tbody>
</table>3.  Investigate and resolve any data streaming issues.

    **Note:** If you experience permissions-related issues with streaming log data from Elasticsearch, refer to the [Granting privileges for data streams from Elasticsearch \[KB0967366\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=9648a9281b61b4100b8a9979b04bcb04) article in the Now Support Knowledge Base.


## What to do next

When the logs are streaming properly, proceed to [map your raw log data](hla-data-input-mapping.md).

**Note:** You can choose to [edit incoming raw log data](hla-data-input-preprocess.md) before Health Log Analytics processes it. For example, preprocessing enables you to discard log portions or remove sensitive data from your logs. This task is optional.

**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

