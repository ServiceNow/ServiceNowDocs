---
title: Deactivate, reactivate, or delete an external content connector
description: Deactivate an external connector to pause its scheduled crawls while retaining all of the content and metadata that it has already crawled. Reactivate a deactivated connector to resume its scheduled crawls. Delete an external content connector to remove the connector's definition along with all content and metadata that it has crawled.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Deactivate, reactivate, or delete an external content connector

Deactivate an external connector to pause its scheduled crawls while retaining all of the content and metadata that it has already crawled. Reactivate a deactivated connector to resume its scheduled crawls. Delete an external content connector to remove the connector's definition along with all content and metadata that it has crawled.

## Before you begin

Role required: ais\_admin

## About this task

You can deactivate an external content connector to suspend its scheduled crawls. The connector's status changes to `Inactive`. All content, metadata, and permissions indexed from the deactivated connector's previous crawls remain available in search, but no new updates are retrieved from the external data source unless you choose to run a one-time crawl. You can reactivate the connector to resume its scheduled crawls.

You can delete an external content connector to remove its definition. When you delete a connector, AI Search removes all content, metadata, and permissions from that connector's crawls from the index. As a result, users cannot find content from the deleted connector when searching in AI Search applications.

## Procedure

1.  Use the application picker to switch to the External Content Connectors Admin application scope.

    For details on selecting an application scope using the application picker, see [Select an application from the application picker](../../../build/applications/task/t_SelectAnAppFromTheAppPicker.md).

2.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

3.  In the Connectors pane, find the record for the connector you want to deactivate or delete, and open its context menu in one of the following ways:

    -   Select the connector record's Overflow icon ![](../image/icon-action-menu-ext-cont-conn.png).
    -   Right-select the connector record.
4.  In the context menu, select one of the following options:

    -   To suspend crawling for an active connector, select **Deactivate**.
    -   To reactivate an inactive connector, select **Activate**.
    -   To permanently delete a connector, select **Delete**, then select **I understand** and **Delete** in the Delete connector dialog box.
    **Warning:** Deleting an external connector is not reversible. Once you delete a connector, you cannot restore its definition or its crawled content, metadata, and permissions.


## Result

The result depends on which selection you made:

-   If you deactivated a connector, its status changes to `Inactive`.
-   If you reactivated a deactivated connector, its status changes from `Inactive` to some other value.
-   If you deleted a connector, it disappears from the Connectors list.

## What to do next

If you deactivated an external content connector to disable its scheduled crawls, you can still run one-time crawls to update its content and metadata or its permissions on demand. For details on running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md) and [Run a one-time user mapping crawl for an external content connector](run-umap-crawl-ext-cont-connector.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

