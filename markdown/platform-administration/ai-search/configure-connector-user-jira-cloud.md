---
title: Configure a connector user in Atlassian Jira Cloud
description: Create a user and group in your Atlassian Jira Cloud tenant with access and permissions required by the Atlassian Jira Cloud external content connector. The connector runs as this user when accessing data from your tenant.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Atlassian Jira Cloud external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a connector user in Atlassian Jira Cloud

Create a user and group in your Atlassian Jira Cloud tenant with access and permissions required by the Atlassian Jira Cloud external content connector. The connector runs as this user when accessing data from your tenant.

## Before you begin

You must have Jira administrator global permissions in your Atlassian Jira Cloud tenant.

To ensure that you grant the correct access to the connector user, you should be familiar with the project roles and issue security levels defined in your Atlassian Jira Cloud tenant.

Role required: none

## About this task

When creating an Atlassian Jira Cloud external content connector, search administrators need to supply credentials for an Atlassian Jira Cloud user that can access all necessary data in the tenant.

Atlassian administrators need to create and configure this user as part of configuration for the Atlassian Jira Cloud source system.

## Procedure

1.  Log in to your Atlassian Jira Cloud tenant.

2.  Create a new user for the Atlassian Jira Cloud external content connector.

    For information on creating a user, see the [Create, edit, or remove a user](https://confluence.atlassian.com/display/ADMINJIRASERVER/Create%2C+edit%2C+or+remove+a+user) Atlassian resource.

3.  Create a new group that includes only the connector user.

    To learn about creating and populating groups, see the [View, create, or delete a group](https://confluence.atlassian.com/display/ADMINJIRASERVER/View%2C+create%2C+or+delete+a+group) and [Modify group membership](https://confluence.atlassian.com/display/ADMINJIRASERVER/Modify+group+membership) Atlassian resources.

4.  Assign the new group access to all project roles needed to view issue comments and worklogs.

    For information on assigning group access to project roles, see the [Assign group access to a project role](https://confluence.atlassian.com/display/ADMINJIRASERVER/Assign+group+access+to+a+project+role) and [Managing project role membership](https://confluence.atlassian.com/display/ADMINJIRASERVER/Managing+project+role+membership) Atlassian resources.

5.  Add the **Jira administrators** and **Jira users** global permissions to the new group.

    To learn about adding global permissions to a group, see the [Managing global permissions](https://confluence.atlassian.com/display/ADMINJIRASERVER/Managing+global+permissions) Atlassian resource.

6.  Add the **Browse Projects** permission to the new group for each project that you want the external content connector to crawl.

    For information on adding project permissions to a group, see the [Manage project permissions](https://confluence.atlassian.com/display/ADMINJIRASERVER/Managing+project+permissions) Atlassian resource.

7.  Include the new group in all issue security levels defined for all your issue security schemes.

    To learn about including groups in issue security levels, see the [Configuring issue-level security](https://confluence.atlassian.com/display/ADMINJIRASERVER/Configuring+issue-level+security) Atlassian resource.


## What to do next

Provide the technical user credentials to your search administrators so they can use them when creating Atlassian Jira Cloud external content connectors.

**Parent Topic:**[Atlassian Jira Cloud external content connector](../concept/atlassian-jira-cloud-external-content-connector.md)

