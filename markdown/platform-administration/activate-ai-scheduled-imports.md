---
title: Activate SCCM Asset Intelligence scheduled imports
description: To prevent duplicate software imports, activate either the Asset Intelligence \(AI\) or the non-AI scheduled import.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft SCCM integration, ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate SCCM Asset Intelligence scheduled imports

To prevent duplicate software imports, activate either the Asset Intelligence \(AI\) or the non-AI scheduled import.

## Before you begin

Role required: admin

## About this task

Make sure to limit the software import frequency to be no greater than the frequency of the table cleanup that tracks deleted software in SCCM.

Asset Intelligence is supported in these SCCM plugins:

-   Integration - Microsoft SCCM 2007
-   Integration - Microsoft SCCM 2012 v2
-   Integration - Microsoft SCCM 2016

**Important:** To improve the performance of your initial SCCM import, you can prevent the system from checking against deleted software prior to the import date. Navigate to **Integration - Microsoft SCCM &lt;version&gt;** &gt; **Data Sources** &gt; **SCCM &lt;version&gt; Removed Software** and enter the current date in the **Last run datetime** field, using the format **yyyy-mm-dd 00:00:00.0**. This field is populated automatically for each subsequent run of the removed software data source, so it is not necessary to alter the value after the initial import.

## Procedure

1.  Navigate to the **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Set **Active** to **false** for these data import schedules:

    -   SCCM &lt;version&gt; Software
    -   SCCM &lt;version&gt; Removed Software
3.  Set **Active** to **true** for these data import schedules:

    -   SCCM &lt;version&gt; Software \(with AI\)
    -   SCCM &lt;version&gt; Removed Software \(with AI\)

**Parent Topic:**[Microsoft SCCM integration](../concept/c_MicrosoftSCCMIntegration.md)

**Related topics**  


[Configure the SCCM integration and schedule an import](configure-sccm-data-import.md)

