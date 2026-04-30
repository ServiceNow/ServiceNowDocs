---
title: Import Jira projects to SPW
description: Discover and import all available Jira projects and boards into Strategic Planning Workspace to start using the integration between the two applications.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Import Jira projects to SPW

Discover and import all available Jira projects and boards into Strategic Planning Workspace to start using the integration between the two applications.

## Before you begin

[Connect SPW to Jira](connect-spw-to-jira.md).

Role required: sn\_jira\_int.user

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  Select **Discover Projects**.

    This action creates requests to import Jira projects and boards, and to create mapping configuration for all these projects. You can view all the import requests in the Jira Import Requests related list and the initial state of all the requests would be **Requested**


## Result

Once the status of each import request changes to **Complete**, you can see that the related lists of this Jira instance are populated as follows:

-   Jira Projects: All available projects from Jira
-   Jira Boards: All available boards from Jira
-   Project Style Mappings: Mapping configuration for all the imported Jira projects.

## What to do next

[Configure integration settings for a Jira project.](../concept/configuring-jira-project-settings-in-spw.md)

