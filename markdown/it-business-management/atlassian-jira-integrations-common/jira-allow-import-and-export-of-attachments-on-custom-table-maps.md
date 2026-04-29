---
title: Allow import and export of attachments on a custom Agile Development 2.0 table
description: Enable import and export of attachments between Jira and Agile Development 2.0 for a custom Agile 2.0 table that you added to the map configuration.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing map configuration for your Jira projects, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Allow import and export of attachments on a custom Agile Development 2.0 table

Enable import and export of attachments between Jira and Agile Development 2.0 for a custom Agile 2.0 table that you added to the map configuration.

## Before you begin

Role required: admin or sn\_jira\_int.admin

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Business Rules**.

2.  From the list of business rules, locate and open the Sync Attachment to Jira rule.

3.  In the When to run section of the form, include your custom table map by adding it to the filter conditions.

    For example, if the custom table that you added is Defect, do the following:

    1.  Click **Add "OR" Clause**.

    2.  Set the new clause to **Table name** **is** **rm\_defect**.

4.  Click **Update**.


**Parent Topic:**[Customizing map configuration for your Jira projects](../reference/custom-map-configuration.md)

