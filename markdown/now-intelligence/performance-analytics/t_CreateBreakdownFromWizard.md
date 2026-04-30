---
title: Create a breakdown from a wizard
description: Create a breakdown, breakdown source, and breakdown mappings, and associate the breakdown with indicators.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Performance Analytics breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a breakdown from a wizard

Create a breakdown, breakdown source, and breakdown mappings, and associate the breakdown with indicators.

## Before you begin

Role required: pa\_power\_user, pa\_data\_collector, or admin

**Note:** Users with only the pa\_power\_user role cannot create breakdown sources.

## About this task

Create a simple breakdown based on an existing indicator. To create more advanced breakdowns or breakdown sources, such as to limit data sets with complex filters, create or update breakdown and breakdown source records directly.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Breakdowns** &gt; **Create New**.

2.  Select the **Indicator** that you want to create the breakdown for.

    The **Table** field is automatically populated based on the indicator source table. You can apply the new breakdown to other indicators with the same source table on the **Link to indicators** tab.

3.  Select the **Field** to base the breakdown on.

    The breakdown uses values from this field as breakdown elements and breaks down collected data based on the value of this field in each record.

4.  Click **Next**.

    The **Define the breakdown** tab displays different data depending on if a breakdown, breakdown source, or breakdown mapping exist for the specified indicator, table, and field.

5.  Perform one of the following actions.

<table id="choicetable_xxh_jqm_h5"><tbody><tr><td id="d96089e136">

**Create a breakdown, breakdown source, and mapping**

</td><td>

If no breakdown or breakdown source exists for the specified table, enter a name for the new breakdown. A breakdown source and mapping for the selected table and field are created automatically. Click **Show filter to make adjustments** to filter the data included in the breakdown source.

</td></tr><tr><td id="d96089e148">

**Create a mapping using an existing breakdown source**

</td><td>

If at least one breakdown source exists for the specified table and there are one or more breakdowns using the source, select the breakdown to create a mapping for. If a mapping exists between a breakdown with the selected source and a field on a parent of the indicator table, you can only select an existing breakdown to create the mapping for. If no such mapping exists for a parent table, you can select an existing breakdown or create a new breakdown.

</td></tr><tr><td id="d96089e160">

**Review existing records**

</td><td>

If a breakdown and breakdown source exist for the specified table, and a breakdown mapping exists for the specified breakdown and field, review the settings. You do not need to make any changes.

</td></tr></tbody>
</table>6.  Click **Next**.

7.  On the **Link to indicators** tab, select any additional indicators that you want to apply the breakdown to.

    You can apply the breakdown to other indicators with the same source table as the indicator you selected first. If the breakdown already applies to an indicator, that indicator is not displayed.

8.  Click **Next**.

9.  On the **Data Collection** tab, select how many days of historical, broken-down scores and snapshots to collect, or clear the **Collect data from the past** to skip historical data collection.

10. Click **Next**.

11. Review the settings and confirm that the correct records will be created, then click **Apply**.

    A check mark appears next to each record after it is created. When all records are created the **Create another breakdown** button appears.


**Parent Topic:**[Performance Analytics breakdowns](../concept/c_CreatingBreakdowns.md)

