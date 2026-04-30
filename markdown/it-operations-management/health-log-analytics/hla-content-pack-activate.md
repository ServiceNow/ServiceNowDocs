---
title: Activate a content pack in Health Log Analytics
description: You can activate a content pack before configuring a data input.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, content packs, activate]
breadcrumb: [Health Log Analytics content packs for quicker time to value, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Activate a content pack in Health Log Analytics

You can activate a content pack before configuring a data input.

## Before you begin

For an overview of this feature, see [Health Log Analytics content packs for quicker time to value](../concept/hla-content-packs.md).

Role required: evt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Content Packs**.

2.  Open the appropriate content pack for your data input.

    **Note:** Currently, a content pack is available for streaming logs from Linux using Filebeat.

3.  On the **Content Pack** form, select **Activate**.

    The **Active** check-box appears selected. The activated content pack displays the script templates and source types that are associated with it.

    ![Active content pack.](../image/hla-content-pack-active.png)

    **Note:** The source types included in the content pack may already exist on your ServiceNow instance. In this case, Health Log Analytics automatically renames the content pack source types by adding a content pack suffix to their name. If you want to use the content pack source types and their mapping, delete or rename the original source types and then remove the suffix from the content pack source types. Otherwise, Health Log Analytics uses the original source types.

    On the **Data Input Mapping** form, the mapping script is listed as a JavaScript functions template option.

    ![Content pack mapping script listed as JavaScript functions template option.](../image/hla-content-pack-mapping-script.png)


## What to do next

When you have configured the data input and you're mapping your raw log data, you can select the content pack’s mapping script from the **JS functions templates** drop-down.

**Parent Topic:**[Health Log Analytics content packs for quicker time to value](../concept/hla-content-packs.md)

