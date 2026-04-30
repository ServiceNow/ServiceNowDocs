---
title: General guidelines for streaming data to Health Log Analytics
description: This section helps you identify the appropriate data input for streaming your specific data type to the Health Log Analytics application.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, streaming, data types]
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# General guidelines for streaming data to Health Log Analytics

This section helps you identify the appropriate data input for streaming your specific data type to the Health Log Analytics application.

<table id="table_wrn_3bx_hfc"><thead><tr><th>

Data type

</th><th>

Data input

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Flat files

</td><td>

ACC agent \(Agent Client Collector Framework\)

</td><td>

Use the ServiceNow ACC agent to stream flat files directly to Health Log Analytics. This method is suitable for log files, CSVs, and other structured file formats.

</td></tr><tr><td>

Cloud applications

</td><td>

Depends on the cloud: Microsoft Azure Event Hubs, Amazon Data Firehose, other methods

</td><td>

-   Microsoft Azure Event Hubs: Configure your Microsoft Azure Event Hubs to send data to Health Log Analytics using the Microsoft Azure Event Hubs data input.
-   Amazon Data Firehose: Set up an Amazon Data Firehose delivery stream to send data to Health Log Analytics using the Amazon Data Firehose data input.
-   More examples.

</td></tr><tr><td>

Data lakes

</td><td>

Apache Kafka, Cribl

</td><td>

-   Apache Kafka: Export data from your data lake to a Kafka topic and use the Apache Kafka data input to stream it to Health Log Analytics.
-   Cribl: Use Cribl to export data from your data lake and use the Cribl data input to stream it to Health Log Analytics.

</td></tr><tr><td>

Databases

</td><td>

Treat as flat files

</td><td>

Treat database logs, such as Oracle error logs, as flat files and use the ACC agent to stream them to Health Log Analytics.

</td></tr><tr><td>

Third-party tools

</td><td>

Varies by tool

</td><td>

-   VMware: vCenter can use UDP to stream data to the MID Server and Health Log Analytics using the UDP data input.
-   More examples.

</td></tr><tr><td>

APM tools

</td><td>

Varies by tool

</td><td>

-   New Relic: Use the New Relic plugin to stream events directly to Health Log Analytics. Export raw logs to a flat file and use the ACC agent to stream them to Health Log Analytics.
-   Dynatrace: Set up the Dynatrace integration to stream data directly from Dynatrace to Health Log Analytics.
-   Nagios: Use the Nagios plugin to stream events directly to Health Log Analytics. Export logs to a flat file and use the ACC agent to stream them to Health Log Analytics.
-   Datadog: Use the Vector Agent data input to stream data from Datadog to Health Log Analytics.

</td></tr></tbody>
</table>**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

