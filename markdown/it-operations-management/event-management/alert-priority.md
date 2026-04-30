---
title: Alert priority
description: Determine the order in which to handle alerts according to the alert priority score. Multiple factors determine the alert priority score and this value changes with changes to the underlying factors.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert priority

Determine the order in which to handle alerts according to the alert priority score. Multiple factors determine the alert priority score and this value changes with changes to the underlying factors.

## Multi-factor decisions

The value of the alert priority score is a composite of the value of the category and its relative weight. You can configure the factors that make up the score, as described in the following sections, according to **Category order**, **Category value mapping**, and **CI type weight factor mapping**. The categories are:

-   **Accumulated categories** - These categories accumulate items with different sub-types that may have a different status or weighing factor. For example, services that are factored according to different criticality or services that are factored according to cost.
-   **Choice-list categories** - A list of items. You can map any of the items to a different value, thereby changing the priority for that item. For example, critical severity, which has the value of 1 by default, can be mapped to 4 to give it a higher weight in the calculated alert priority score.

<table id="table_wsm_v5d_sbb"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Accumulated categories**

</td></tr><tr><td>

Number of impacted business-services

</td><td>

This category is factored by the business-criticality of the service. An alert that has an impact on one service has a lower priority score than an alert that has an impact on many services. For example, if a router is down, then it might affect many services and a higher priority ensures that this alert is handled before handling another alert that has an impact on fewer services. An alert that has an impact on many non-critical services must be handled with priority. However, if an alert has an impact on only a few services, but they are critical services, then this alert has a higher priority.

</td></tr><tr><td>

CI type

</td><td>

This category distinguishes between various CI types. For example, an alert on a CI type that is a router or switch may have a higher priority than an alert on another CI type, like a server or application.

</td></tr><tr><td>

Number of Secondary alerts

</td><td>

Alerts that have characteristics similar to other alerts are usually grouped together, such as alerts with the same message key. A parent alert which has many secondary alerts has a higher priority than a parent alert that has only a few secondary alerts.All secondary alerts of a parent alert are counted. If a secondary alert is closed, it is no longer correlated to the parent alert. If a parent alert is closed, all secondary alerts are no longer correlated and their priority value is calculated accordingly.

</td></tr><tr><td colspan="2">

**Choice-list categories**

</td></tr><tr><td>

Alert state

</td><td>

Priority score is not calculated for an alert that is in **Closed** state. The available states with their default values are:-   Open = mapping value 1
-   Reopen = mapping value 2
-   Flapping = mapping value 3

</td></tr><tr><td>

Alert severity

</td><td>

The priority score reflects the level of seriousness of the underlying alert, for example, an alert that has severity of **Critical** has a higher weighted value than an alert with a severity of **Minor**. Priority is not calculated for an alert that has a severity of **OK**. The available levels are:-   Critical
-   Major
-   Minor
-   Warning

</td></tr><tr><td>

Role

</td><td>

The priority score reflects the role of the alert. The priority score is higher for an alert that has a role of **Parent**, next is the role of **None**, and the least weight is given to an alert with a role of **Secondary**. A parent alert that has many secondary alerts has a higher value than a parent alert that has less secondary alerts. The available roles are:-   Parent
-   None
-   Secondary

</td></tr></tbody>
</table>## Structure of the alert priority score

-   **Weighted value for each category**

    Each category has its own placement in the alert priority score, according to its order and limit. You can configure the order and limit, as described in [Modify the alert priority score](alert-priority.md#section_modify), below. There are only positive numbers.

    All category values are mapped from the **em\_alert\_priority\_category\_mapping** table, except for the following:

    -   CI Type: Mapped from the **em\_alert\_priority\_ci\_type** table.
    -   Secondary: Value is the number of secondary alerts and is not mapped from any table.

**Note:** To ensure optimal memory protection, alert groups with more than 1000 alerts may not have an accurate priority score.

<table id="table_lr4_bcs_gcb"><thead><tr><th>

Category

</th><th>

Score

</th></tr></thead><tbody><tr><td>

Services

</td><td>

\(7.0, 1000000.0\) For example, if there are 2 impacted services whose business criticality priority score is as follows:

-   Service1: Business criticality priority score = **3**
-   Service2: Business criticality priority score = **4**

The sum of the business criticality priority scores is **7**, so the computed priority value is 7,000,000 \(7 \* 1,000,000\)

 **Note:** The business criticality priority score is the mapped value \(**Value after mapping**\) in the application services entries of the Alert Priority Category Mappings table \(em\_alert\_priority\_category\_mapping\).

</td></tr><tr><td>

Severity

</td><td>

\(3.0, 100000.0\)

</td></tr><tr><td>

CI type

</td><td>

\(20.0, 100.0\)

</td></tr><tr><td>

Role

</td><td>

\(2.0, 10.0\)

</td></tr><tr><td>

Secondary

</td><td>

\(0, 0.01\)

</td></tr><tr><td>

State

</td><td>

\(3.0, 0.001\)

</td></tr></tbody>
</table>Using the scores from the preceding table, the alert priority score is computed as follows:

**\(Services value \* 1,000,000\) + \(Severity value \* 100,000\) + \(CI type value \* 100\) + \(Role value \* 10\) + \(Secondary value\) + \(State value \* 0.001\)**

Replacing the values of the categories from the preceding table into the formula:

**\(7 \* 1,000,000\) + \(3 \* 100,000\) + \(20 \* 100\) + \(2 \* 10\) + \(0 \* 0.001\) + \(3 \* 0.001\) = 7,302,020.003**

In the **Priority Breakdown** area of the **More Information** tab, the alert priority value is displayed as 7302020.003. In the Alerts list, this value is displayed as 7302 \(number of thousands\).

**Note:** If you have customized business criticality values that differ from the out-of-box values, add an entry to the Alert Priority Category Mappings table \[em\_alert\_priority\_category\_mapping\].

-   **Effect of category limits**

    Limits placed on categories enable overflow values to affect the next category that is ranked higher in priority order. Each accumulated category has a predefined limit. If the count goes above that limit, 1 is added to the next higher-order category. For example, if the number of CI types goes over the limit, then 1 is added to the next category \(Severity\) which is higher in priority: `yyy-zzz becomes yy(y+1) - 000`


## Display in All Alerts list

In the **All Alerts** list, the alert priority score value is displayed in the **Priority** column. For display purposes only, the actual calculated alert priority score is divided by 1000, while in the database, for calculation and sorting purposes, the full computed value is used.

The detailed computation of the alert priority of the selected alert is displayed in the **Priority Breakdown** area **More Information** tab.

## Calculating the alert priority score

Calculating alert priority is based on all of a group's alerts, and not only the group's primary alert. Priority is calculated for alerts that match these conditions:

-   State not-equal to **Closed**
-   Severity not-equal to **OK**

Alerts that are queued for priority calculation are listed in the `em_alert_trigger_queue` table. In the Scheduled Jobs table, there are two `Event Management - Alert Priority Queue` jobs. These two jobs can run in parallel. You can use `Insert and Stay` to create another job. The `Event Management - Alert Priority Queue` job runs once every minute and calculates priorities in batches of 1000 open alerts. There are multiple factors that determine the value of the priority of an alert. A change in severity triggers an immediate update of the alert priority score. In this case, only the severity-part of the priority is changed, together with severity information in the **Priority Breakdown** area of the **More Information** tab.

## Triggers that cause recalculation

Triggers that can cause the alert priority score to be recalculated are:

<table id="table_oc1_4km_gcb"><thead><tr><th>

Trigger

</th><th>

Effect on the alert priority score

</th></tr></thead><tbody><tr><td>

New alert

</td><td>

The generation of a new alert is a trigger to calculate the alert priority score.

</td></tr><tr><td>

Existing alert that changes from closed to any other state

</td><td>

Priority is not calculated for a closed alert, so if the alert state is changed from its current state of closed to open, reopen, or flapping, that change is a trigger to recalculate the alert priority score.

</td></tr><tr><td>

Role change, between primary, secondary, or none

</td><td>

Changes in role are a trigger for the alert priority score to be recalculated. For example:-   An alert whose type has changed to `Primary`, triggers the alert priority score to be recalculated.
-   An alert whose type has changed to `None`, triggers the alert priority score to be recalculated.
-   An alert whose type has changed to `Secondary`, triggers the alert priority score to be recalculated.

</td></tr><tr><td>

CI type

</td><td>

When a CI becomes bound to alert, that change is a trigger to recalculate the alert priority score. This trigger to recalculate the priority occurs once only, when the CI is bound to the alert.

</td></tr><tr><td>

Change of number of secondary alerts

</td><td>

A change in the number of secondary alerts triggers the alert priority score to be recalculated.

</td></tr><tr><td>

Severity

</td><td>

A change in severity is a trigger to recalculate the alert priority score. For example, changing from `OK` to `Major` triggers the score to be recalculated. Unlike the other triggers listed above, a change in severity triggers an immediate update of the severity part of the alert priority score calculation.

</td></tr></tbody>
</table>## Modify the alert priority score

You can change the importance of some categories of the alert priority, by modifying their order and/or their weight, as described below. For example, if the CI type is higher in importance than the number of impacted services, you can change their respective order. As a result, the number of services is now multiplied by 100, while CI type is now multiplied by 1000000.

**Note:** The changes that you make, using this advanced procedure, change the default method of calculating the alert priority score. Alerts that might otherwise not have a high score, by changing these configurable values, change the way you determine the order in which to handle alerts.

-   **Changing category order**

    Navigate to the **em\_alert\_priority\_category\_order** table. In the **Order** column, you can change the order of the required category.

-   **Category value mapping**

    The **em\_alert\_priority\_category\_mapping** table shows the configuration value for each category choice. Each value in a drop-down list of categories can be remapped to a different value by configuring this table.

-   **CI type weight factor mapping**

    Navigate to the **em\_alert\_priority\_ci\_type** table. You can add a new CI, for example, `DualCoreCPU` and in the **Priority** column, you can change the priority of the required category. In addition, you can edit existing Type and also change its priority value. This table is used to map the value of each CI type, for example, a mainframe that is CI\_type: cmdb\_ci\_mainframe might have a priority of 80, while a server with CI type: cmdb\_ci\_server might have a priority of 60. The mapping enables you to customize the priority of the various Ci types.


**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

