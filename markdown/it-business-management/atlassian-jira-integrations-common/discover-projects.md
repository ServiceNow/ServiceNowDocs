---
title: Discover and import Jira projects and boards
description: Discover and import all available Jira projects and boards into Agile Development 2.0 to start using the integration between the two applications.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Discover and import Jira projects and boards

Discover and import all available Jira projects and boards into Agile Development 2.0 to start using the integration between the two applications.

## Before you begin

-   [Connecting Agile Development 2.0 to Jira](../concept/connect-sn-agile-with-jira.md#).
-   Role required: sn\_jira\_int.user

## About this task

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  Click **Discover Projects**.

    This action creates requests to import Jira projects, map configuration for all these projects, and Jira Boards. You can view all the import requests in the Jira Import Requests related list and the initial state of all the requests would be **Requested**.


## Result

Once the status of each import request changes to **Complete**, you can see that the related lists of this Jira instance are populated as follows:

-   Jira Projects: All available projects from Jira
-   Jira Boards: All available boards from Jira
-   Project Style Mappings: Map configuration for all the imported Jira projects according to the type of your Jira instance as follows:

    -   The **classic\_on\_prem** project template contains the map configurations related to the Jira Server projects.
    -   The **classic** project template contains the map configurations related to Jira Cloud Classic projects.
    -   The **next-gen** project template contains the map configurations related to Jira Cloud Next-gen projects.
    Once the status of the Create Mappings request changes to **Completed**, you can see the map configuration for each of the imported Jira project under the Mapping Config column of the Jira Projects related list. For more information on the default map configuration of work items, see [Default mapping configuration between Agile Development 2.0 and Jira](../reference/jira-sn-field-mapping.md).


## What to do next

Import your issues from Jira to Agile Development 2.0. For more information, see [Importing issues and sprints from Jira to Agile Development 2.0](../concept/importing-issues-and-sprints-from-jira-to-agile-dev-2.0.md).

