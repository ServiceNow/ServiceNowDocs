---
title: Configure the SLA timer
description: Configure the SLA timer to determine which task SLA must be displayed as part of the timer component.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Configure the SLA timer

Configure the SLA timer to determine which task SLA must be displayed as part of the timer component.

## Before you begin

Role required: sla\_admin, sla\_manager, itil, sn\_slm\_timer.sla\_timer\_admin, or admin

## About this task

All Service Level Agreement \(SLAs\) attached to a task, such as an incident, problem, or change are of equal importance. However, on various scenarios and user interfaces, you might want to configure a hierarchy of preferred SLAs. After configuring the hierarchy, you can determine from the list the most important or preferred SLA that can be displayed.

The **slm-timer-config-api** application enables you to set a preferred SLA for a given task. You can use the configuration that is either dynamic, such as **First SLA to breach**, or declarative from a hierarchical mapping of first to matching SLA definitions.

The SLA timer configuration provides the following demo data which also serves as an example to customize.

-   **Do not show SLA timer**

    Use this configuration if you don’t want to show the timer component.

-   **Show SLA that will breach first**

    Use this configuration to determine the task SLA that has the earliest breach time.

-   **Incident Response and Resolution Team**

    Use this configuration if you prefer to display Task SLA matching specific SLA Definition in the timer component. This configuration creates a hierarchy of SLA Definitions to be displayed.


The **SLA Timer Configuration** application comes only with demo data. However, you should create your own configuration records. You can use the demo data as a guide to help ensure that the preferred task SLA record is shown against a particular task.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **Administration** &gt; **SLA Timer Configuration**.

2.  Select **New**.

3.  On the forms, fill in the fields.

<table id="table_t4t_nzb_hlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the SLA timer configuration

</td></tr><tr><td>

SLA timer source

</td><td>

Choose any one of the following:-   **None**

When you don’t want to show the timer.

-   **First to breach**

When you want to display the task SLA with the earliest breach time.

**Note:** When a task SLA with the earliest breach time pauses, goes out of schedule, or is completed, then the next task SLA is displayed.

-   **Task to SLA mapping**

When you want to create your own display hierarchy of task SLAs. If you choose this option, you must define the SLA Definition mappings to ensure that a preferred SLA definition is set.

</td></tr><tr><td>

Show completed

</td><td>

Select if you want to display the preferred task SLA that includes the breached stage. If this option is selected, on complete, it will not move to the next SLA priority.

</td></tr></tbody>
</table>4.  Select **Update**.

5.  Open the SLA configuration that you created.

6.  If the SLA timer **Source** is set to `Task to SLA Mapping`, then you must configure the mappings.

7.  To configure the task to SLA mapping, select **New** in the **SLA timer configurations mappings** related list.

8.  On the form, fill in the fields.

    |Name|Description|
    |----|-----------|
    |SLA timer config|Select the timer config from the look-up list. If created from related list, the timer config is auto-populated with the parent record.|
    |Order|The hierarchical order of the task SLA. This value is pre-populated. However, you can edit it based on your requirements.|
    |Table|Select the table that the task belongs to, for example, Incident, Problem, or Change. This selection is used as a reference qualifier on the SLA definition.|
    |SLA definition|Select the SLA definition that is available for the table.|

    **Note:** If there is an identical mapping for the **Order** or **SLA definition** in the selected table, the configuration is prevented using business rules. This check ensures that only one preferred SLA definition is set at each level in the hierarchy.

9.  Select **Submit**.


If no configuration sys\_id is provided to the sla-timer-configuration API, then the default behavior is:

-   **SLA Timer source**: First to Breach
-   **Show cancel**: true
-   **Show complete**: true

However, you must not provide a configuration sys\_id to the application. Set up your own configuration, even if it’s identical to the default behavior.

**Parent Topic:**[Configuring Service Level Management](../concept/configuring-service-level-management.md)

