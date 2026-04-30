---
title: Identifying bottlenecks using Process Mining integration with Workforce Optimization for ITSM
description: Get insights into your teams' performance and analyze anomalies or bottlenecks within the process when you drill down into a leaf node KPI.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating Process Mining with Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Identifying bottlenecks using Process Mining integration with Workforce Optimization for ITSM

Get insights into your teams' performance and analyze anomalies or bottlenecks within the process when you drill down into a leaf node KPI.

A leaf node KPI is a child KPI that cannot be drilled down further.

**Important:**

-   To integrate Process Mining with Workforce Optimization for ITSM, you must enable the Process Mining plugin \(com.sn\_po\) after you enable the Workforce Optimization for ITSM \(sn\_wfo\_cfg\_itsm\) plugin from the ServiceNow Store.
-   You must enable the **sn\_team\_perf.enable.po.wfo** system property to **True** to enable the integration of Process Mining with Workforce Optimization for ITSM. For more information, see [Workforce Optimization for ITSM integration with Process Mining](../reference/configurable-wfo-itsm-process-optimization.md).
-   You can create your own process finding definitions. You also have the option of enabling process finding definitions that have default process configurations for incidents, problems, and change requests when you install the ITSM Process Mining Content Pack \(sn\_itsm\_po\) plugin available from the ServiceNow Store. If you do not enable this plugin, you can analyze process variations but not process findings.

For more information, see [Activate Workforce Optimization for ITSM](../task/activate-configurable-workforce-optimization-itsm.md) and [Access Process Mining](https://www.servicenow.com/docs/access?context=activate-po-plugin&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

-   **[Create a Process Mining project for a KPI group](../task/create-project-po-wfo-itsm.md)**  
Create Process Mining projects for each KPI group and its assignment groups. One project is created per KPI group per table.

**Parent Topic:**[Integrating Process Mining with Workforce Optimization for ITSM](integrating-po-wfo-itsm.md)

