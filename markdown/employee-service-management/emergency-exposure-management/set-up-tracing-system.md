---
title: Set up a tracing system for an exposure data source
description: Set up a tracing system for your exposure data source to identify potentially exposed employees by running the diagnostic requests for an affected employee.
locale: en-US
release: zurich
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Tracing systems in Emergency Exposure Management, Set up Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Set up a tracing system for an exposure data source

Set up a tracing system for your exposure data source to identify potentially exposed employees by running the diagnostic requests for an affected employee.

## Before you begin

Role required: admin

## About this task

For more information about the available tracing systems, see [Tracing systems in Emergency Exposure Management](../concept/tracing-systems-exposure-mgnt.md).

## Procedure

1.  Navigate to **All** &gt; **Emergency Exposure Management** &gt; **Administration** &gt; **Tracing Systems**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_tracing_systems_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the tracing system.The title is displayed as an option for selection in the **Tracing system** list on the Diagnostic Request form.

</td></tr><tr><td>

Name

</td><td>

Name of the tracing system.

</td></tr><tr><td>

Parent

</td><td>

Tracing system for a group of other tracing systems having the similar type of input data source. If the tracing systems are in a group, only the parent tracing system displays in the **Tracing system** list on the Diagnostic Request form.

</td></tr><tr><td>

Active

</td><td>

Option for making the tracing system active. Only active tracing systems are available for selection as a data source for the diagnostic requests.

</td></tr><tr><td>

Requires dates

</td><td>

Option for enabling the start and end dates to specify a period for querying the data source for the tracing system.If selected, the **Start date** and **End date** fields appear when you select this tracing system on the Diagnostic Request form.

</td></tr><tr><td class="sub-head" colspan="2">

Processing script tab

</td></tr><tr><td>

Condition

</td><td>

Condition to determine the tracing system data for the diagnostic request on selecting a parent tracing system. For example, if two tracing systems A1 and A2 have the same parent tracing system called A. In a diagnostic request, if you select A as the tracing source, the condition determines whether to query data from A1 or A2.

 For reference, you can review the condition scripts of the base tracing systems Cisco DNA Spaces and Mist System having the parent tracing system as Wi-Fi access log.

 This field appears only when a tracing system is selected in **Parent**.

</td></tr><tr><td>

Use parent processing script

</td><td>

Option for executing the processing script of the parent tracing system. The parent tracing system's processing script populates the potentially exposed employees data in the corresponding related list on the Diagnostic Request form. If you select this option, the current tracing system's processing script does not process.This field appears only when a tracing system is selected in **Parent**.

</td></tr><tr><td>

Processing script

</td><td>

Script to populate the potentially exposed employees data in the corresponding related list on the Diagnostic Request form.

</td></tr><tr><td class="sub-head" colspan="2">

Contact graph tab

</td></tr><tr><td>

Legend icon

</td><td>

Icon representing the tracing system as data source for the potentially exposed contact's in the potentially exposed contacts visualization on the Case form.For more information, see [Working on a case through contact tracing visualization](../../contact-tracing/reference/contact-tracing-case-visualization.md).

</td></tr><tr><td>

Legend tooltip

</td><td>

Tooltip text that appears when you point to the legend icon.

</td></tr><tr><td>

Order

</td><td>

Order in which the icons appear in the Reason for exposure section.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The tracing system is created. The tracing system appears as one of the options in the **Tracing system** field on the Diagnostic Request form.

## What to do next

-   [Associate a system property with a tracing system](associate-sys-property-tracing-system.md).
-   [Create or modify a diagnostic request task configuration](create-diagnostic-task-config.md).

