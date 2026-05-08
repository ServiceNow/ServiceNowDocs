---
title: Configure AI search for Contract Workspace
description: Get improved search results in Contract Workspace by configuring the ServiceNow AI Search application to work with it.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [AI search in contract workspace, Search in contract request]
breadcrumb: [Configure Contract Workspace, Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure AI search for Contract Workspace

Get improved search results in Contract Workspace by configuring the ServiceNow® AI Search application to work with it.

## Before you begin

Role required: admin

## About this task

With the AI Search engine in Contract Workspace, you can search with keywords related to contract requests and find the most relevant search results.

If you are a new customer, the AI Search application is configured with your base system.

If you are an existing customer, you have to configure Contract Workspace to use the AI Search application.

For more information on the AI Search application, and how to use most effectively use it, see AI Search. For information about how to associate the AI Search application with Contract Workspace, see Create a search application configuration for AI Search.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the Experiences section, select **Contract Workspace**.

3.  Select **View experience settings**.

    ![Configure experience setting for Contract workspace in UI builder.](../image/cmpro-contract-wsp-settings.png "UI builder Contract workspace experience settings")

4.  In the Global search section, in the **Search source** drop-down list, select **Contract Workspace AI Search**.

5.  Select **Save**.

    ![Configure Ai search as the sairch engine in contract workspace](../image/cmpro-contract-wsp-aisearch-settings.png "Configure global search")

6.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

7.  In the AI Search Index Sources page, select **Contract Request** and **Contract Repository**.

8.  Index tables to improve the performance and accuracy of search results by selecting **Index All Tables** from the Actions for selected rows drop-down list.


## Result

AI Search is configured for Contract Workspace.

