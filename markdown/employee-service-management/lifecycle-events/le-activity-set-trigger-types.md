---
title: Lifecycle Events activity set trigger types
description: Administrators can configure activity set triggers to make activities in an activity set available.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a Lifecycle Events trigger for activity sets, Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events activity set trigger types

Administrators can configure activity set triggers to make activities in an activity set available.

## Activity set trigger types

-   **Immediate**

    Triggers all the activities in a set as soon as the lifecycle event is created.

-   **Date**

    Triggers activities in an activity set when a date or milestone. The first day for a new hire onboarding activity could be the new hire's first day at work. Date triggers require a **Trigger table** and a **Trigger field**.

<table id="table_eqj_zvd_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Trigger table**

</td><td>

Select a table from the available list.

</td></tr><tr><td>

**Trigger field**

</td><td>

Select a field from the available list.

</td></tr><tr><td>

**Ignore empty date**

</td><td>

If there is no date in the trigger field, the activity set won't trigger.

</td></tr><tr><td>

**Date offset type**

</td><td>

-   After
-   Before


</td></tr><tr><td>

**Date offset quantity**

</td><td>

The number of offset units to be evaluated.

</td></tr><tr><td>

**Date offset units**

</td><td>

-   Days
-   Weeks
-   Months


</td></tr></tbody>
</table>-   **Other activity sets**

    The activity set is triggered when another activity set is complete. When an activity set is triggered by other activity sets, the trigger isn’t activated until all dependent activities in the set are complete.

-   **Advanced**

    Use the **Advanced** trigger to add a script that evaluates custom conditions to trigger the activity set.

-   **Condition**

    Use the **Condition** trigger to define conditions based on the value of fields in a selected table.

-   **Combination**

    Combines the use for **Date**, **Other Activity Sets**, and **Condition**. All three conditions must be met to trigger the activity set.


**Parent Topic:**[Configure a Lifecycle Events trigger for activity sets](../task/le-config-event-trigger.md)

