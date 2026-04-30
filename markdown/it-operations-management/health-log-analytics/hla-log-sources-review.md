---
title: Verify your log sources in Health Log Analytics
description: Verify that all your log sources are present and active after Health Log Analytics tagging has assigned a log to a service instance and components, and has automatically mapped the log to a source.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, log sources, Log Sources table, active, status, tagging, tags, service instance, component, mapping]
breadcrumb: [Additional data input setup tasks, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Verify your log sources in Health Log Analytics

Verify that all your log sources are present and active after Health Log Analytics tagging has assigned a log to a service instance and components, and has automatically mapped the log to a source.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Log Sources**.

    The Log Sources table provides information about the sources created when you mapped the streaming data. The table lists these sources by service instance.

<table id="table_wx1_kt1_gnb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service instance

</td><td>

The service instance. Service instances represent large or complete business processes. A single service instance can consist of multiple components, whereas different service instances can include the same components.

</td></tr><tr><td>

Component

</td><td>

The components comprising the service instance. Components represent small technical parts or business processes. Typically, they represent Configuration Items \(CIs\). Several components are often clustered together in a single service instance.

</td></tr><tr><td>

Status

</td><td>

The status of the log source: Active or Inactive. The Active status indicates that logs streamed into the system from this source in the last hour.

</td></tr><tr><td>

Created

</td><td>

The creation date and time of this log source.

</td></tr><tr><td>

Last event time

</td><td>

The last time logs streamed into the system from this source.

</td></tr></tbody>
</table>2.  Make sure that the system has created all your log sources.

3.  Verify the creation, status, and log samples of a specific source in the source record.

    **Note:** Because auto-mapping can map log data to multiple sources, be sure to verify this information per source.

4.  If a log source is missing, add it.

    1.  Navigate to **Health Log Analytics** &gt; **Data Input** &gt; **Data Input Mapping**.

    2.  Use the JavaScript function to manually map a log sample to the correct service instance, component, and source type.

        For more information, see [Map raw log data in Health Log Analytics](hla-data-input-mapping.md).

    3.  Navigate back to the Log Sources page and verify that the status of the new log source is Active.

    The system creates a log source.

5.  Make sure that the status of all your log sources is Active.

    If the status of a source is Inactive, double-click it and change it to Active manually.

6.  Select **Update**.


**Parent Topic:**[Additional data input setup tasks in Health Log Analytics](../concept/hla-data-input-setup-extra.md)

**Related topics**  


[Delete a log source in Health Log Analytics](hla-log-source-delete.md)

[Stop extraction of unneeded log data in Health Log Analytics](hla-log-data-exclude.md)

[Extract specific log data in Health Log Analytics](hla-log-data-extract.md)

