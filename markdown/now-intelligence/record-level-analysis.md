---
title: Configure record level analysis in AI Data Explorer
description: Get more detailed answers based on the content of individual records to provide more meaningful insights.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-18"
reading_time_minutes: 2
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Configure record level analysis in AI Data Explorer

Get more detailed answers based on the content of individual records to provide more meaningful insights.

## Before you begin

Roles required: now\_assist\_explorer\_admin or higher

## About this task

Record-level analysis provides deeper insights into your data. You can activate it as an administrator. You can activate it as an opt-in, where you specify the tables to which it applies, or as an opt-out, where it applies to all tables you don't specify. Whether activated or not, queries that touch on more than 50 records in a table aren’t supported.

**Warning:** Take care when activating record-level analysis for a table with record-level security. The LLM applies the record-level security when analyzing records, but it applies only report\_view ACLs when the exploration is shared. Therefore, users may see data about records that they are not authorized to access when an exploration is shared with them.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the product area pane, select **Platform**.

3.  In Now Assist skills for Platform, search for the analytics exploration skill.

4.  If the **Activate skill** button is visible for this skill, press it to activate the skill.

5.  If the **Deactivate skill** button is visible for this skill, expand the 3-dot menu ![Menu icon](../../../common/image/icon-menu.png) and select **Edit**.

    ![Tile for the Analytics exploration skill showing the Edit button.](../image/ai-data-expl-edit-skill.png)

6.  Select **Advanced analysis** from the menu, which opens the Record level analysis page.

7.  Toggle on **Enable record analysis**.

    ![Analytics exploration skill settings with Enable record level analysis turned on.](../image/ai-data-explr-enable-rla.png)

8.  In the **Enable for** field, select whether to create an include list or an exclude list of tables.

    |Option|Description|
    |------|-----------|
    |**Selected tables**|Select a list of tables to which record level analysis will apply. Record level analysis will not apply to any other tables.|
    |**All except selected tables**|Select a list of tables to which record level analysis won’t apply. Record level analysis will apply to all other tables.|

9.  In the **Supported tables** or **Excluded tables** field, select which tables to include or exclude, respectively.

10. Select **Save and continue**.

11. Finish configuring the skill as described in [Activate AI Data Explorer skills](../task/activate-now-ass-explorer.md), or exit if the skill is already activated and you don’t wish to make further changes.


## Simple request with and without record level analytics

You don’t have record level analytics enabled, and you open an exploration and ask for all open incidents. You’re told "There are currently 40 open incidents. This reflects all incidents that remain unresolved at this time."

![Response in an exploration without record level analytics.](../image/ai-data-expl-response-wo-rla.png)

Now you enable record level analytics on the instance. You choose an opt-in approach and specify Incident \[incident\] as the only table included in record level analytics.

![Activating record level analytics for the Incident table.](../image/ai-data-expl-activating-rla.png)

Finally, you ask the same question again in an exploration, asking for all open incidents. Now the response includes details about the differences between open incident records. You’re told "There are 40 open incidents currently. Among these, several are marked as 1 - Critical priority, including issues such as inability to launch VPN clients, rain leaking on the main DNS server, and multiple SAP application outages. The most common categories for open incidents are inquiry / help, software, and hardware, with critical incidents distributed across all three."

![Response in an exploration with record level analytics.](../image/ai-data-expl-response-with-rla.png)

**Parent Topic:**[Configure AI Data Explorer](../task/configure-now-ass-explorer.md)

