---
title: Create a business rule to apply a custom table map configuration
description: Create a business rule to enable import for your new custom table map configuration from and Project Portfolio Management \(PPM\) application.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a table map, Create custom mapping configurations, Configuring Portfolio Planning with PPM, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Create a business rule to apply a custom table map configuration

Create a business rule to enable import for your new custom table map configuration from and Project Portfolio Management \(PPM\) application.

## Before you begin

Role required: sn\_align\_core\_apw.admin

## About this task

After you create a custom table map in Portfolio Planning integrations, create a business rule similar to 'Sync Data from Execution to Alignment' business rule in the rm\_epic or dmn\_demand tables.

**Note:** Ensure that the business rule is created in the execution application, PPM.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  From the list of available business rules, locate and open the Sync Data from Execution to Alignment rule.

3.  From the context menu \(![Context menu icon.](../images/context-menu-icon.png)\), perform an Insert and Stay operation on this business rule.

    If you have not enabled the **Insert and Stay** action in your ServiceNow instance, see [Allow insert options on records](https://www.servicenow.com/docs/access?context=advanced-form-administration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

4.  On the business rule form, edit the following fields.

<table id="table_hpg_yjj_hmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the business rule. For example, if your new table map is to map demands, name this rule as Sync Demands with Portfolio Planning.

</td></tr><tr><td>

Table

</td><td>

Select the table for which you've created the custom map.For example, Feature \[sn\_safe\_feature\].

</td></tr></tbody>
</table>5.  Click **Update**.


