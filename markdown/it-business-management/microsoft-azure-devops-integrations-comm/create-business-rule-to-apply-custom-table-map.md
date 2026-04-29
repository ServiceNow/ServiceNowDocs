---
title: Create a business rule to apply a custom table map configuration
description: Create a business rule to enable export from your new custom map configuration of an Agile Development 2.0 table to your Azure DevOps projects.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Create a business rule to apply a custom table map configuration

Create a business rule to enable export from your new custom map configuration of an Agile Development 2.0 table to your Azure DevOps projects.

## Before you begin

Role required: admin

## About this task

After you create a custom table map for an Azure DevOps process type, create a business rule similar to Synch Story with Azure DevOps to support export of information using this new table map to Azure DevOps.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  From the list of available business rules, locate and open the Synch Story with Azure DevOps rule.

3.  From the context menu \(![context menu icon](../../apw-internal-integrations/images/context-menu-icon.png)\), perform an Insert and Stay operation on this business rule.

    If you have not enabled the **Insert and Stay** action in your ServiceNow instance, see [Allow insert options on records](https://www.servicenow.com/docs/access?context=advanced-form-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

4.  On the business rule form, edit the following fields.

<table id="table_hpg_yjj_hmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the business rule. For example, if your new table map is to map defects, name this rule as Sync Defect with Azure DevOps.

</td></tr><tr><td>

Table

</td><td>

Select the table in Agile Development 2.0 for which you've created the custom map.For example, Defect \[rm\_defect\].

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

