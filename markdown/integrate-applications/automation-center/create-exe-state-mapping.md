---
title: Create execution state mapping
description: Define the mapping for the source and target tables for the configuration to work as expected.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring automation summary execution, Configuring Automation Center, Automation Center, Creating integrations with applications]
---

# Create execution state mapping

Define the mapping for the source and target tables for the configuration to work as expected.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Administration** &gt; **Automation Sources**.

    The Automation sources page is displayed with a list of existing automation sources.

2.  Select the source for which you want to create the execution state mapping.

3.  Select the execution summary configuration for which you want to create the execution state mapping.

4.  Select **New** in the Execution state mappings section.

    The Execute state mapping page is displayed.

5.  On the form, fill in the fields:

<table id="id_jw3_jvk_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution state

</td><td>

Options for the **State** field of the Automation Execution Summary table.

 The following values are available:

 -   Canceled
-   Complete
-   Error
-   Queued
-   Running


</td></tr><tr><td>

Application

</td><td>

The associated application or the application scope in which the source is being created, such as Automation Center or RPA Hub. This field is auto-populated.

</td></tr><tr><td>

Source group values

</td><td>

Options for the "group by" field of the source.

</td></tr><tr><td>

Automation source

</td><td>

Name of the automation source that you’ve selected for this execution state mapping.

</td></tr></tbody>
</table>6.  Select **Submit**.

    You’re taken to the Execution summary configuration page.

7.  Select **Publish**.


## Result

The automation summary execution configuration is complete.

**Parent Topic:**[Configuring automation summary execution](../concept/config-auto-sum-exe.md)

