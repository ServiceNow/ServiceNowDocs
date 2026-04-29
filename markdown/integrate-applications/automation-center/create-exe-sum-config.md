---
title: Configure execution summary
description: Configure the execution summary with the appropriate conditions.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring automation summary execution, Configure, Automation Center, Workflow Data Fabric]
---

# Configure execution summary

Configure the execution summary with the appropriate conditions.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Administration** &gt; **Automation Center** &gt; **Automation Sources**.

    The Automation sources page is displayed with a list of existing automation sources.

2.  Select the source for which you want to configure the execution summary.

    The Automation source page is displayed with the details of the source.

3.  Select **New** in the Execution Summary Configurations section.

    The Execution summary configuration form is displayed.

4.  On the form, fill in the fields.

<table id="id_jw3_jvk_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation source

</td><td>

The automation source that you’ve selected. This field is auto-populated.

</td></tr><tr><td>

Application

</td><td>

The associated application or the application scope in which the source is being created, such as Automation Center or RPA Hub. This field is auto-populated.

</td></tr><tr><td>

Table

</td><td>

The table from where you must import data.

</td></tr><tr><td>

State

</td><td>

The state of the execution summary configuration. This field is auto-populated.

</td></tr><tr><td>

Automation

</td><td>

The automation field from the selected table.

</td></tr><tr><td>

Group by

</td><td>

A field from the chosen table that you want to use to group the records.

</td></tr><tr><td>

Start date

</td><td>

Start time of the summary configuration.

</td></tr><tr><td>

End date

</td><td>

End time of the summary configuration.

</td></tr><tr><td>

Trigger type

</td><td>

An action that triggers the flow.

 The following values are available for trigger:

 -   Created: Every time a record in the source table is created.
-   Updated: Every time a record in the source table is updated.
-   Created or Updated: Every time a record in the source table is created or updated.
-   Daily: Scheduled to run daily.
-   Weekly: Scheduled to run weekly.
-   Run once: Scheduled to run only once.
-   Monthly: Scheduled to run monthly.
 These triggers can be set in the associated flow.

</td></tr></tbody>
</table>5.  Select **Submit**.

    You’re taken to the previous page. When an execution summary configuration is created, a flow is automatically created to match the configuration. The value set for the **Trigger type** field triggers this newly created flow.![Execution summary configuration](../images/exe-sum-config.png)

6.  Select the summary configuration in the Execution Summary Configurations section.

    **Note:** One automation source can have only one execution summary configuration.

7.  Select **Update**.

    **Note:** If you want to change the state of the execution summary from **Published** to **Draft**, select **Draft** at the top right of the page.


## What to do next

[Create execution state mapping](create-exe-state-mapping.md)

**Parent Topic:**[Configuring automation summary execution](../concept/config-auto-sum-exe.md)

