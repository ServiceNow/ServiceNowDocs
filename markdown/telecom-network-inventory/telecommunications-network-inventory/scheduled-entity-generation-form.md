---
title: Scheduled Entity Generation form
description: The Scheduled Entity Generation form enables you to create, review and modify the schedule generation details for a default template.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default Template forms, Reference, Telecommunications Network Inventory]
---

# Scheduled Entity Generation form

The Scheduled Entity Generation form enables you to create, review and modify the schedule generation details for a default template.

<table id="table_frl_rpf_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies this scheduled job. The default value is the template name. If required, you can update this field.

</td></tr><tr><td>

Active

</td><td>

Option that indicates that the scheduled job is active and should be executed at a specified date and time.

</td></tr><tr><td>

Application

</td><td>

Name of the application that contains the entity. Global appears if the entity is in the global scope.

</td></tr><tr><td>

Run

</td><td>

Time interval to use for running the scheduled job. To learn more, see [Automatically generate something from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_ScheduleTheGenerationOfAnEntity.md).

</td></tr><tr><td>

Time zone

</td><td>

An area that follows a specific standard time for official purposes.

</td></tr><tr><td>

Time

</td><td>

Time of day at which the scheduled job should run, expressed in hours, minutes, and seconds on a 24-hour clock. The selection that you make in the **Time** zone field determines the time zone for this entry.

</td></tr><tr><td>

Conditional

</td><td>

Option for enabling the running of the scheduled job if certain conditions are met in the associated script.

</td></tr><tr><td>

Condition

</td><td>

Conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true or false\) value. This text box appears only if you select **Condition**.

</td></tr><tr><td>

Generate this

</td><td>

Reference to the template record from which you are generating a scheduled job.

</td></tr></tbody>
</table>**Parent Topic:**[Default Template forms](default-template-forms.md)

**Related topics**  


[Create a default template](../task/create-default-templates.md)

