---
title: Get Workday task code for My Team's Birthday
description: Get the task code for the My Team's Birthday task from your Workday tenant. The Workday external content connector needs this task code to retrieve team birthday data from the Manager hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/get-workday-task-code-birthday.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-24"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Get Workday task code for My Team's Birthday

Get the task code for the My Team's Birthday task from your Workday tenant. The Workday external content connector needs this task code to retrieve team birthday data from the Manager hub.

## Before you begin

You need the manager role and access to the My Team's Birthday task in your organization's Workday tenant.

Role required: none

## About this task

This task is optional. The Workday external content connector can retrieve Manager hub data from your Workday source system. If you don't want to retrieve Manager hub data from Workday, you can skip this task.

## Procedure

1.  Log in to your Workday tenant with your manager credentials.

2.  In the Workday search bar, search for the **My Team's Birthday** task and select it.

3.  Copy the task code from the Workday URL for the My Team's Birthday page and store it in a secure location.

    The task code is the path element between the final slash and the `.htmld` extension in the URL shown for the My Team's Birthday page. As an example, if your My Team's Birthday page URL is `https://impl.workday.com/example/d/task/3005$6924.htmld`, the task code is `3005$6924`.

    **Important:** Your external content connector administrator needs this task code when configuring the Workday external content connector to retrieve Manager hub data.


## What to do next

Provide the task code you copied in step [3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/get-workday-task-code-birthday.md) to your connector administrator. They need this task code to configure a Workday external content connector to retrieve Manager hub data from your Workday source system.

For details on creating and configuring a Workday external content connector, see [Create a Workday external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-workday.md).

**Parent Topic:**[Workday external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/workday-external-content-connector.md)

