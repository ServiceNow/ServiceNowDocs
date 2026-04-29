---
title: Configure the SLA timer
description: Configure the SLA timer to determine which task SLA must be displayed as part of the timer component.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Configure the SLA timer

Configure the SLA timer to determine which task SLA must be displayed as part of the timer component.

## Before you begin

Role required: sla\_admin, sla\_manager, itil, sn\_slm\_timer.sla\_timer\_admin or admin

## About this task

All Service Level Agreement \(SLAs\) attached to a task, such as an incident, problem, or change are of equal importance. However, on various scenarios and user interfaces, you might want to configure a hierarchy of preferred SLAs. After configuring the hierarchy, you can determine from the list, the most important or preferred SLA that can be displayed.

The **slm-timer-config-api** application provides the ability to set a preferred SLA for a given task using the configuration that is either dynamic, such as **First SLA to breach** or declarative from a hierarchical mapping of first to matching SLA definitions.

The SLA timer configuration provides the following foundation data which also serves as an example to customize.

-   **Do not show SLA timer**

    Use this configuration if you do not want to show the timer component.

-   **Show SLA that will breach first**

    Use this configuration to determine the task SLA that has the earliest breach time.


The **SLA Timer Configuration** application comes only with demo data, it is always advisable to create your own configuration records. You can use the demo data as a guide to help ensure the preferred task SLA record is shown against a particular task.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **Administration** &gt; **SLA Timer Configuration**.

2.  Click **New**.

3.  On the forms, fill in the fields.

<table id="table_t4t_nzb_hlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the SLA timer configuration

</td></tr><tr><td>

SLA timer source

</td><td>

The source of the SLA timer. The available options are:-   **None**

The timer is not displayed.

-   **First to breach**

Displays the task SLA with the earliest breach time.

**Note:** When a task SLA with the earliest breach time pauses, goes out of schedule, or is completed, the next task SLA is displayed.

-   **Task to SLA mapping**

Uses a customized display hierarchy of task SLAs. SLA Definition mappings must be defined to ensure a preferred SLA definition is available.

</td></tr><tr><td>

Show completed

</td><td>

Option to display the preferred task SLA that includes the breached stage. If this option is selected, on completion, the process will not move to the next SLA priority.

</td></tr><tr><td>

Show cancelled

</td><td>

Option to display task SLAs in the cancelled state.

</td></tr><tr><td>

Show actual time

</td><td>

Option to display the actual time remaining until breach time, including time outside business hours.

</td></tr></tbody>
</table>4.  Click **Update**.

5.  Open the SLA configuration you created.

6.  If the **SLA timer source** field value is set to First to breach, configure the additional filters and target fields.

<table id="table_fq4_n1y_xfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced condition

</td><td>

Option to display the condition builder to define and filter the task SLA displayed. These conditions are executed on the definitions in the SLA Definition \[contract\_sla\] table.

</td></tr><tr><td>

Condition

</td><td>

The condition builder to define the filter.**Note:** When conditions are defined, the task SLA that is earliest to the breach time and that satisfies all defined conditions is displayed. If all SLAs that satisfy the defined conditions have already been breached, the SLA that has breached first among SLAs that meet the defined conditions, is displayed.

This field appears only when the Advanced condition check box is selected.

</td></tr><tr><td>

Target

</td><td>

The target used to map the SLAs. The available options are:-   **None**

Displays the task SLA with the earliest breach time.

-   **Response**

Displays the task SLA with the earliest breach time for tasks for which Response is configured as the target field in the SLA definition.

-   **Resolution**

Displays the task SLA with the earliest breach time for which Resolution is configured as the target field in the SLA definition.

**Note:** You can customize the available options using the sys\_choice table.

</td></tr></tbody>
</table>7.  If the **SLA timer source** field is set to Task to SLA Mapping, configure the mappings.

8.  Select **New** in the SLA timer configurations mappings related list.

9.  On the form, fill in the fields.

    |Name|Description|
    |----|-----------|
    |SLA timer config|The desired timer configuration. If the timer was created from a related list, this field will be auto-populated with the parent record.|
    |Order|The hierarchical order of the task SLA. This value is pre-populated. However, you can edit it based on your requirements.|
    |Table|The table that the task belongs to,which is used as a reference qualifier on the SLA definition. The available values are Incident, Problem, or Change.|
    |SLA definition|Select the SLA definition that is available for the table.|

    **Note:** If an identical mapping for the **Order** or **SLA definition** in the selected table, the configuration is prevented from using business rules. This check ensures that there is always only one preferred SLA definition at each level in the hierarchy.

10. Click **Submit**.


If no configuration sys\_id is provided to the sla-timer-configuration API, then default behaviour is:

-   **SLA Timer source**: First to Breach
-   **Show cancel**: true
-   **Show complete**: true

However, as a best practice do not provide a configuration sys\_id to the application. Setup their your own configuration, even if it is identical to the default behavior.

**Parent Topic:**[Configuring Service Level Management](../concept/configuring-service-level-management.md)

