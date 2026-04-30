---
title: Review the breakdown sources
description: Breakdown sources represent the elements that you use to examine a KPI in more detail. Modify the breakdown source to limit the element list to only those items that are meaningful for the data analysis.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Platform Analytics Solutions, Analytics solutions, Platform Analytics]
---

# Review the breakdown sources

Breakdown sources represent the elements that you use to examine a KPI in more detail. Modify the breakdown source to limit the element list to only those items that are meaningful for the data analysis.

## Before you begin

Role required: pa\_admin, admin

## About this task

For example, the Assignment Group automated breakdown uses the Groups breakdown source. This breakdown source returns ALL active groups in your instance, and the system uses all these groups to examine your data. If you look at the Number of Open Changes indicator, and you examine the Assignment Group breakdown, you see all groups in your instance instead of just the groups that are actually working on your Change requests.

Restricting the number of elements that a breakdown source returns has the following benefits:

-   Smaller element lists make it easier for consumers to find the data they need. Sorting through a list of 25 groups associated with a particular process is easier than trying to sort through thousands of groups.
-   Smaller element lists lead to less data collection and more efficient use of data. Instead of the [data collector](../concept/performance-analytics-glossary.md#) crunching through 1,000 different groups, the data collector can analyze the 25 groups that are meaningful to the process.

**Note:** You probably do not need to change the breakdown sources in Platform Analytics Solutions. However, you may find it helpful to review and understand exactly what is being measured in your processes.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Sources** &gt; **Breakdown Sources**.

2.  Click a breakdown source to see its details.

3.  In the Source tab, examine the definition for the breakdown elements, including the table that contains the unique list of sys\_ids.

    For example, in the Change.Impact breakdown source, the unique values contained in the Change Request Impact field come from the Choice \[sys\_choice\] table. The conditions provide additional filters to ensure that the query returns only the Change Impact fields from the Choice \[sys\_choice\] table.![Change.Impact breakdown source showing unique values table and conditions](../image/review-bkdown-source.png)

4.  Click **Preview** to see the number of elements that the query returns.

    In the example, the query returns three impact elements.

    ![The number of matching conditions link that appears after clicking Preview](../image/review-bkdown-source-numb-conditions.png)

5.  Click **x records match condition** to see the specific values that the query returned.

    In the example, clicking **3 records match condition** opens a new browser tab with a filtered list of records from the Choice \[sys\_choice\] table.![Filtered list of choices matching the indicator source conditions](../image/review-bkdown-source-choices.png)

6.  Verify that the list of records match what you expect to see in the breakdown element list.

7.  If the records were not what you expected, modify the conditions in the Source tab of the breakdown source to match your environment and repeat steps 4-6 until you are satisfied.

8.  Click **Update** to save your changes.


## What to do next

You are now ready to collect data, as described in [Collect data for Platform Analytics Solutions](../concept/collect-data-nowintel-solutions.md).

**Parent Topic:**[Configure Platform Analytics Solutions](../concept/configure-nowintel-solutions.md)

**Previous topic:**[Update Performance Analytics scripts](update-pa-scripts.md)

**Next topic:**[Collect data for Platform Analytics Solutions](../concept/collect-data-nowintel-solutions.md)

**Related topics**  


[Define a breakdown source](t_DefiningABreakdownSource.md)

