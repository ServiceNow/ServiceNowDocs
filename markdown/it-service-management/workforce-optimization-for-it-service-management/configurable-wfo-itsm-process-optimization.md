---
title: Workforce Optimization for ITSM integration with Process Mining components
description: Workforce Optimization for ITSM installs roles and properties to configure the Workforce Optimization for ITSM integration with Process Mining.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up the integration of Process Mining with Workforce Optimization for ITSM, Integrating Process Mining with Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Workforce Optimization for ITSM integration with Process Mining components

Workforce Optimization for ITSM installs roles and properties to configure the Workforce Optimization for ITSM integration with Process Mining.

## Properties

<table id="table_ywt_4t1_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_team\_perf.enable.po.wfo

</td><td>

Enable the integration of Process Mining with Workforce Optimization for ITSM.-   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

promin.wfo.run\_frequency

</td><td>

Time interval to re-mine Process Mining projects. After you run the Process Mining - WFO Remine Projects scheduled job to mine the data, you can run it again only at the set interval. If you run the job earlier than that, it will not remine the data.-   **Type:** integer
-   **Default value:** 7 days

</td></tr></tbody>
</table>## Roles

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Process Mining Analyst \[sn\_process\_optimization\_analyst\]|Create and share Process Mining projects.|sn\_process\_optimization\_viewer|

## Scheduled jobs

Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

|Name|Description|
|----|-----------|
|Process Mining - WFO Remine Projects|Automatically runs once a day. You can run this job on demand when additional data is added to a project so that you get the up-to-date process insights into your projects. The job will remine data based on the frequency set in the **promin.wfo.run\_frequency** property.|

**Parent Topic:**[Setting up the integration of Process Mining with Workforce Optimization for ITSM](../concept/setting-up-process-optimization-wfo-itsm.md)

