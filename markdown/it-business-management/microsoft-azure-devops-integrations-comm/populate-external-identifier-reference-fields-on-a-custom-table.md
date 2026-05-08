---
title: Populate Azure DevOps identifier reference fields for a custom table
description: Enable Azure DevOps project identifier reference fields for an Agile Development 2.0 table that you added to the map configuration of a process type.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Populate Azure DevOps identifier reference fields for a custom table

Enable Azure DevOps project identifier reference fields for an Agile Development 2.0 table that you added to the map configuration of a process type.

## Before you begin

Role required: admin

## About this task

You can display references of ID, key, Azure DevOps project, and the project URL on your custom table form by adding this table to the Populate External Identifier Reference business rule.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

2.  From the list of business rules, locate and open the Set external URL for Work Items rule.

3.  In the When to run section of the form, include your custom table map by adding it to the filter conditions.

    For example, if the custom table that you added is Defect, do the following:

    1.  Click **Add "OR" Clause**.

    2.  Set the new clause to **Reference table** **is** **rm\_defect**.

4.  Click **Update**.


## What to do next

Configure the form layout or personalize the list layout of your custom table to display any or all of the following fields.

-   External ID
-   External Key
-   External Project
-   External URL

**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

**Related topics**  


[bundle-platux.t_PersonalizeAList]

[bundle-platadm.configure-form-layout]

