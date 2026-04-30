---
title: Create a business rule to apply a custom Agile Development 2.0 table map configuration
description: Create a business rule to enable export from your new custom Agile Development 2.0 table map configuration to your Jira projects.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2024-09-06"
reading_time_minutes: 1
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Create a business rule to apply a custom Agile Development 2.0 table map configuration

Create a business rule to enable export from your new custom Agile Development 2.0 table map configuration to your Jira projects.

## Before you begin

Role required: admin or sn\_jira\_int.admin

## About this task

After you create a custom table map for a single or multiple Jira projects, create a business rule similar to Synch Story with Jira to support export of information from this new table map from Agile Development 2.0 to Jira.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  From the list of available business rules, locate and open the Synch Story with Jira rule.

3.  From the context menu \(![context menu icon](../../apw-internal-integrations/images/context-menu-icon.png)\), perform an Insert and Stay operation on this business rule.

    If you have not enabled the **Insert and Stay** action in your ServiceNow instance, see [Allow insert options on records](https://www.servicenow.com/docs/access?context=advanced-form-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

4.  On the business rule form, edit the following fields.

<table id="table_hpg_yjj_hmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the business rule. For example, if your new table map is to map defects, name this rule as Sync Defect with Jira.

</td></tr><tr><td>

Table

</td><td>

Select the Agile Development 2.0 table for which you've created the custom map.For example, Defect \[rm\_defect\].

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

