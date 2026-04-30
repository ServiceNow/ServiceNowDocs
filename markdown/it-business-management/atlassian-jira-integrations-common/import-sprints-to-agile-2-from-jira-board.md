---
title: Import sprints from Jira to Agile Development 2.0
description: Import sprints from a Jira board so that you can track progress of these sprints directly in Agile Development 2.0.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing issues and sprints from Jira to Agile Development 2.0, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Import sprints from Jira to Agile Development 2.0

Import sprints from a Jira board so that you can track progress of these sprints directly in Agile Development 2.0.

## Before you begin

-   Ensure that the Jira board from which you want to import the sprints has team integration settings. For more information, see [Associate a Jira project and board with an assignment group in Agile Development 2.0](project-integration-settings.md).
-   Role required: sn\_jira\_int.user

## About this task

Import completed and current sprints of Jira board into Agile Development 2.0.

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Jira Projects related list, open the project that is associated to a Jira board from which you want to import the sprints.

4.  Enable the import and export of sprints by selecting the **Enable Import** and **Enable Export** options as applicable.

5.  Click **Import Issues**.

6.  Select a date range from which you want to import the sprints from Jira.

7.  Click **Submit**.

    An import request of type Import Sprints is created in the Jira Import Requests related list. Once the state of this request changes to Completed, you can view all the imported sprint data in the Sprints related list of the associated assignment group in Agile Development.


**Parent Topic:**[Importing issues and sprints from Jira to Agile Development 2.0](../concept/importing-issues-and-sprints-from-jira-to-agile-dev-2.0.md)

