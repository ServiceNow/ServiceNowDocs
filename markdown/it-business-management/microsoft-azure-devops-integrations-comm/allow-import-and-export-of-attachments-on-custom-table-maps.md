---
title: Allow import and export of attachments on a custom table
description: Enable import and export of attachments between Azure DevOps and Agile Development 2.0 for a custom table that you added to the map configuration of a process type.
locale: en-US
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Allow import and export of attachments on a custom table

Enable import and export of attachments between Azure DevOps and Agile Development 2.0 for a custom table that you added to the map configuration of a process type.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

2.  From the list of business rules, locate and open the Sync Attachment to Azure rule.

3.  In the When to run section of the form, include your custom table map by adding it to the filter conditions.

    For example, if the custom table that you added is Defect, do the following:

    1.  Click **Add "OR" Clause**.

    2.  Set the new clause to **Table name** **is** **rm\_defect**.

4.  Click **Update**.


**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](../reference/customizing-map-config-agile-azure.md)

