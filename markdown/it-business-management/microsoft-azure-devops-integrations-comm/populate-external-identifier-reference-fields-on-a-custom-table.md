---
title: Populate Azure DevOps identifier reference fields for a custom table
description: Enable Azure DevOps project identifier reference fields for an Agile Development 2.0 table that you added to the map configuration of a process type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/microsoft-azure-devops-integrations-comm/populate-external-identifier-reference-fields-on-a-custom-table.html
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing your map configuration for Azure DevOps integration, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Populate Azure DevOps identifier reference fields for a custom table

Enable Azure DevOps project identifier reference fields for an Agile Development 2.0 table that you added to the map configuration of a process type.

## Before you begin

Role required: admin

## About this task

You can display references of ID, key, Azure DevOps project, and the project URL on your custom table form by adding an External Identifier reference field to your custom table and then adding the table to the Populate External Identifier Reference business rule.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables** and open your custom table \(for example, `rm_defect`\).

2.  Add an External Identifier reference field to your custom table with the following values.

    -   Type: Reference
    -   Reference table: `sn_int_common_external_identifiers`
    -   Column name: `u_external_identifier`
    -   Column label: External Identifier
3.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

4.  From the list of business rules, locate and open the Populate External Identifier Reference rule.

5.  In the When to run section of the form, include your custom table map by adding it to the filter conditions.

    For example, if the custom table that you added is Defect, do the following:

    1.  Click **Add "OR" Clause**.

    2.  Set the new clause to **Reference table** **is** **rm\_defect**.

6.  Update the Advanced Script section of the rule to handle the new custom table reference and map the External Identifier field accordingly.

7.  Click **Update**.


## What to do next

Configure the form layout or personalize the list layout of your custom table to display any or all of the following fields.

-   External ID
-   External Key
-   External Project
-   External URL

**Parent Topic:**[Customizing your map configuration for Azure DevOps integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/microsoft-azure-devops-integrations-comm/customizing-map-config-agile-azure.md)

**Related topics**  


[bundle-platux.t_PersonalizeAList]

[bundle-platadm.configure-form-layout]

[Populate external identifier on custom tables for Azure DevOps](https://www.servicenow.com/community/spm-articles/populate-external-identifier-on-custom-tables-for-azure-devops/ta-p/3359244)

