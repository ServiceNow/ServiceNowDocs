---
title: Process Mining components for Digital Portfolio Management
description: Admins must install the ITSM Process Mining Content Pack from the ServiceNow Store to get the insights and system property for Process Mining in Digital Portfolio Management \(DPM\). Use Process Mining to analyze and improve key performance indicator \(KPI\) outputs in DPM.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Digital Portfolio Management reference, Digital Portfolio Management, IT Service Management]
---

# Process Mining components for Digital Portfolio Management

Admins must install the ITSM Process Mining Content Pack from the ServiceNow® Store to get the insights and system property for Process Mining in Digital Portfolio Management \(DPM\). Use Process Mining to analyze and improve key performance indicator \(KPI\) outputs in DPM.

## Properties

<table id="table_ywt_4t1_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dpm.enable.po.dpm

</td><td>

Enables you to use Process Mining with DPM.-   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

sn\_itsm\_dpm.po\_mining.run\_frequency

</td><td>

Time interval to remine Process Mining projects. You must run the Process Mining scheduled job in DPM to mine the data. You can run it again only at the set interval. If you run the job earlier, it won’t remine the data.-   **Type:** integer
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
|Process Mining - DPM Remine Projects|Automatically runs once daily. You can run this job on demand when additional data is added to a project so that you get the up-to-date process insights for your projects. The job remines data based on the frequency set in the **dpm.po\_mining.run\_frequency** property.|

**Parent Topic:**[Digital Portfolio Management reference](dpm-reference-cfw.md)

**Related topics**  


[Configure Digital Portfolio Management to integrate with Process Mining](../concept/dpm-setup-po.md)

[Create Process Mining projects for KPI groups in Digital Portfolio Management](../task/dpm-create-project-po.md)

