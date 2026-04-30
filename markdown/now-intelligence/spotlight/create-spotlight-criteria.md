---
title: Create Spotlight criteria
description: Create Spotlight criteria to define when to weight a record, and the weight to assign.
locale: en-US
release: zurich
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up Spotlight, Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create Spotlight criteria

Create Spotlight criteria to define when to weight a record, and the weight to assign.

## Before you begin

[Create a Spotlight group](create-spotlight-group.md#)

Role required: pa\_spotlight or admin

## About this task

Spotlight criteria define how to weight records based on specific attributes. Each Spotlight criterion is associated with a Spotlight Group.

Spotlight criteria can refer to an indicator or can use a direct query to the facts table. The former criteria are called indicator-based criteria and the latter are called query-based criteria. The indicator for an indicator-based criterion must meet the following requirements:

-   It must be an automatic indicator.
-   It must be set to collect records.
-   It must be based on the same table that the indicator source of the main indicator is based on. This table cannot be a database view.
-   If the Spotlight group evaluates platform data, the indicator cannot use a scripted breakdown.

A query-based criterion queries the same table that the indicator source of the main indicator is based on. The suitability of indicator-based and query-based criteria depends also on whether the Spotlight group evaluates platform data or snapshots of records. For more information, see [Evaluating a snapshot or platform data](create-spotlight-group.md#).

Some criteria may be more important than others and have a higher weight. Weight from multiple criteria is cumulative within a Spotlight Group. The score of a record is the total weight from all applicable Spotlight criteria in the Spotlight Group.

If you have domain separation enabled:

-   When you create Spotlight criteria for a global Spotlight group, the criteria are created in the domain of the logged-in user.
-   When you create Spotlight criteria for a Spotlight group that is in a specific domain, the Spotlight criteria are created in that domain.

Messages appear to inform you of the domain situation when you create Spotlight criteria. For more information, see [Domain separation with Spotlight](../concept/domain-separation-spotlight.md).

## Procedure

1.  In a Spotlight group record, locate the **Spotlight Criteria** related list and click **New**.

2.  Enter the **Weight** you want to assign to records that meet this criterion.

    Consider revisiting the **Threshold** value that is set in the associated Spotlight group. Optimize the weights of the Spotlight criteria of the group and the group threshold against each other.

3.  Select the **Criteria Type** to determine which records are assigned the specified weight.

<table id="choicetable_gw3_tvp_bx"><tbody><tr><td id="d110998e153">

**Indicator**

</td><td>

Select an **Indicator** to assign the weight to all records included in that indicator. Optionally, select one or two breakdowns and elements to limit the records to only those records with the specified breakdown element values.

</td></tr><tr><td id="d110998e165">

**Query**

</td><td>

Set **Filter conditions**. The specified weight is assigned to all records from the facts table that match the filter conditions. The facts table of the main indicator of the Spotlight group is automatically selected.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

You have a criterion for a Spotlight group.

## Spotlight group with three criteria

Consider a Spotlight Group with the following three criteria, all referring to indicators:

-   Open incidents not updated in 30 days, with a weight of 1000.
-   Reassignment &gt; 3 times, with a weight of 800
-   Description is Empty, with a weight of 300

In this example, an open incident that has been reassigned 4 times and has an empty Description field has a total score of 1100. This incident is prioritized above an incident that has not been updated in 30 days, which has a total score of 1000.

## What to do next

Repeat the procedure to create as many criteria as are necessary. Then collect scores. See [Collect Spotlight scores](../concept/collect-spotlight-scores.md).

**Parent Topic:**[Setting up Spotlight](../concept/setting-up-spotlight.md)

