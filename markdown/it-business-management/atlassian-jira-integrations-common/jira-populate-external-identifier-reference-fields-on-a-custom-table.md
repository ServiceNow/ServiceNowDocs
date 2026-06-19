---
title: Populate Jira project identifier reference fields for Agile Development 2.0 custom table
description: Enable Jira identifier reference fields for your Agile Development 2.0 custom table that you added to the map configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/atlassian-jira-integrations-common/jira-populate-external-identifier-reference-fields-on-a-custom-table.html
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Populate Jira project identifier reference fields for Agile Development 2.0 custom table

Enable Jira identifier reference fields for your Agile Development 2.0 custom table that you added to the map configuration.

## Before you begin

Role required: admin or sn\_jira\_int.admin

## About this task

You can display references of ID, key, Jira project, and the project URL on your custom table form by adding an External Identifier reference field to your custom table and then adding the table to the Populate External Identifier Reference business rule.

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

**Parent Topic:**[Customizing map configuration for your Jira projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/atlassian-jira-integrations-common/custom-map-configuration.md)

**Related topics**  


[bundle-platux.t_PersonalizeAList]

[bundle-platadm.configure-form-layout]

[Populate external identifier on custom tables for Azure DevOps](https://www.servicenow.com/community/spm-articles/populate-external-identifier-on-custom-tables-for-azure-devops/ta-p/3359244)

