---
title: Customize business rules for actionable notifications
description: Enables you to customize the business rules for actionable notifications.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery integration, Customize Integrations for Employee Experience, Manage, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Customize business rules for actionable notifications

Enables you to customize the business rules for actionable notifications.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Notifications** &gt; **Actionable Notifications - Business Rules**.

2.  Open a business rule you would like to extend to another table.

    Example: Send comment to caller.

3.  On the **UI Actions** screen, Click **New**.

4.  On the **UI Action** form, fill the fields.

<table id="table_dsz_kwh_pnb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business rule

</td></tr><tr><td>

Table

</td><td>

Table to which the Send comment to caller is to be assigned.

</td></tr><tr><td>

Application

</td><td>

HR Service Delivery integration with Microsoft Teams

</td></tr><tr><td>

Active

</td><td>

Check this option

</td></tr><tr><td>

Advanced

</td><td>

Check this option

</td></tr><tr><td>

Where to run

</td><td>

-   When: after
-   Insert: Check this option
-   Update: Check this option
-   Filter Conditions: Apply the filter condition of the Send comment to caller business rule


</td></tr><tr><td>

Advanced

</td><td>

-   Condition: Copy and paste the value of the condition from the existing Send comment to caller business rule. Modify the values as required.
-   Script: Copy and paste the script from the existing Send comment to caller business rule. Modify the values as required.


</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Customize HR Service Delivery integration with Microsoft Teams](../concept/customize-sn-ms-teams-hr.md)

