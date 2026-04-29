---
title: Deactivate streaming for all GCC customers in Microsoft Teams
description: Control streaming in Microsoft Teams for any and all Government Community Cloud \(GCC\) varieties.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual, Agent, Microsoft, Teams, GCC, Government Community Cloud, Deactivate, Activate, GCC-DoD, GCC-H, Streaming, Now Assist]
breadcrumb: [Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Deactivate streaming for all GCC customers in Microsoft Teams

Control streaming in Microsoft Teams for any and all Government Community Cloud \(GCC\) varieties.

## Before you begin

Role required: admin or virtual\_agent\_admin.

## About this task

**Note:** Custom Engine Agent \(CEA\) is replacing Declarative Agent \(DA\), the prior Microsoft Copilot integration. The CEA enables Virtual Agent to be discoverable by Microsoft Copilot, with full functional access to Now Assist in Virtual Agent and multi-turn conversations.

You must have version 10.1.1 or higher of the Microsoft Teams plugin to have CEA support. In version 10.2 of the Microsoft Teams plugin, streaming is inactive by default and CEA is active by default.

You can deactivate streaming as needed with this procedure, by setting values in the Now Assist Channel Configs \[sys\_now\_assist\_channel\_config\] and Custom Adapter Properties \[sys\_cs\_custom\_adapter\_property\] tables. You can use these instructions with all Government Community Cloud types: GCC, GCC-H, and GCC-DoD.

## Procedure

1.  Navigate to **All** &gt; **sys\_now\_assist\_channel\_config.list**.

2.  In the entry for **Teams**, set the **Streaming Ready** value to `false`.![Now Assist Channel Configs table with Teams Device Type entry highlighted.](../images/disable-gcc-streaming-01.png)

3.  Navigate to **All** &gt; **sys\_cs\_custom\_adapter\_property.list**.

4.  In the search bar, select the search value **for text** from the drop-down menu, and enter `sys_cs_custom_adapter_property`.

    One or more records for `sys_cs_custom_adapter_property` appear.

5.  Set the **Value** for each record to `false`.![Custom Adapter Properties table showing search result for publish_checkpoint_messages records.](../images/disable-gcc-streaming-02.png)


## Result

Streaming is disabled for your version of GCC in your instance.

If you want to reactivate streaming, repeat these steps, but set the **Value** for all entries to `true`.

**Parent Topic:**[Specialized Virtual Agent integrations for Microsoft Teams](../concept/specialized-va-integs-msteams.md)

