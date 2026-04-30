---
title: Set up a work configuration
description: Create a work configuration for a work item. Add filters that display key information that the manager wants to analyze. This work configuration will determine how the work items display on the Work scheduler calendar in manager workspace.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Work scheduler in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Set up a work configuration

Create a work configuration for a work item. Add filters that display key information that the manager wants to analyze. This work configuration will determine how the work items display on the Work scheduler calendar in manager workspace.

## Before you begin

Role required: sn\_wfo\_work\_sched.admin

## Procedure

1.  Navigate to **All** &gt; **Work Scheduler** &gt; **Work Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_bsv_rvy_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the work configuration.

</td></tr><tr><td>

Table

</td><td>

Table for which you want to create the work configuration.Case table is available by default to create work configurations.

</td></tr><tr><td>

Description field

</td><td>

The field from the selected table that you want to use for describing the work item.

</td></tr><tr><td>

Assigned to field

</td><td>

The field from the selected table that you want to use for assigning an agent to the work item.

</td></tr><tr><td>

Assignment group field

</td><td>

The field from the selected table that you want to use for assigning a group to the work item.

</td></tr><tr><td>

Start date field

</td><td>

The field from the selected table that you want to use to display the start date for the work item.

</td></tr><tr><td>

End date field

</td><td>

The field from the selected table that you want to use to display the end date for the work item.

</td></tr><tr><td>

Default color

</td><td>

The preferred color to display the work item card in the manager workspace.

</td></tr><tr><td>

UX app route

</td><td>

The route where the card layout is defined for this work item type. The route displays in UI Builder in the list of experiences. This UX app route determines the layout of the work item card. By default, it is set to **Default card**, which displays the following fields:-   Description field
-   Assigned to field
-   Assignment group field
-   Start date field
-   End date field
If you need additional fields, you must add them in the **Extra fields** field. For information on defining a card layout, see [Create a Work Scheduler card using UI Builder](https://www.servicenow.com/docs/access?context=create-workscheduler-card-wfo-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Order

</td><td>

The display order of the work item.

</td></tr><tr><td>

Extra fields

</td><td>

**Important:** If you need additional fields on the selected table that you would like to display in the work item card in the manager workspace, you must add it in this field.

</td></tr><tr><td>

Matching rule

</td><td>

Select a matching rule for the work configuration.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Submit**.

5.  Create a work configuration filter.

    1.  In the **Work Configuration filters** related list, click **New**.

    2.  In the **Name** field, enter a unique name for the filter.

    3.  Right-click and save the form to add the selected table.

    4.  Add the desired conditions for the work configuration filter.

        For information on adding conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    5.  Select **Update**.


**Parent Topic:**[Setting up Work scheduler in Workforce Optimization for Customer Service](../concept/setting-up-work-scheduler-wfo-cs.md)

