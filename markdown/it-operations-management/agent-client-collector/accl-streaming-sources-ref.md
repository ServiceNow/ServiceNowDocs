---
title: ACC data input streaming sources
description: In the ACC data input record, the Streaming Sources related list shows the streaming data of that data input's sources.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identify and resolve log streaming issues, Agent Client Collector Log Analytics setup, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# ACC data input streaming sources

In the ACC data input record, the Streaming Sources related list shows the streaming data of that data input's sources.

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
</table>**Parent Topic:**[Identify and resolve log streaming issues](../task/accl-verify-log-streaming.md)

