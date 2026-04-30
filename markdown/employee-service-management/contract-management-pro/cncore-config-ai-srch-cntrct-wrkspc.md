---
title: Configure AI search for Contract Workspace
description: Get improved search results in Contract Workspace by configuring the ServiceNow AI Search application to work with it.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Contract Workspace with UI Builder components, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure AI search for Contract Workspace

Get improved search results in Contract Workspace by configuring the ServiceNow® AI Search application to work with it.

## Before you begin

Role required: admin

## About this task

With the AI Search engine in Contract Workspace, you can search with keywords related to contract requests and find the most relevant search results.

If you are a new customer, the AI Search application is configured with your base system.

If you are an existing customer, you have to configure Contract Workspace to use the AI Search application.

For more information on the AI Search application, and how to use most effectively use it, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). For information about how to associate the AI Search application with Contract Workspace, see [Create a search application configuration for AI Search](https://www.servicenow.com/docs/access?context=create-search-app-config-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the Experiences section, select **Contract Workspace**.

3.  Select **Settings**.

4.  In the Global search section, in the **Search source** drop-down list, select **Contract Workspace AI Search**.

5.  Select **Save**.

6.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

7.  In the AI Search Index Sources page, select **Contract Request** and **Contract Repository**.

8.  Index tables to improve the performance and accuracy of search results by selecting **Index All Tables** from the Actions for selected rows drop-down list.


## Result

AI Search is configured for Contract Workspace.

