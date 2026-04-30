---
title: Populate Jira project identifier reference fields for Agile Development 2.0 custom table
description: Enable Jira identifier reference fields for your Agile Development 2.0 custom table that you added to the map configuration.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Populate Jira project identifier reference fields for Agile Development 2.0 custom table

Enable Jira identifier reference fields for your Agile Development 2.0 custom table that you added to the map configuration.

## Before you begin

Role required: admin or sn\_jira\_int.admin

## About this task

You can display references of ID, key, Jira project, and the project URL on your custom table form by adding this table to the Populate External Identifier Reference business rule.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

2.  From the list of business rules, locate and open the Populate External Identifier Reference rule.

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

**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

**Related topics**  


[Personalise a v2 list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=zurich&pubname=zurich-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US)

[Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

