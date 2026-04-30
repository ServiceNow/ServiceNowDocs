---
title: Configure crawl settings for an Adobe Experience Manager as a Cloud Service external content connector
description: Specify the nodes you want your Adobe Experience Manager as a Cloud Service external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-22"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Adobe Experience Manager as a Cloud Service external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for an Adobe Experience Manager as a Cloud Service external content connector

Specify the nodes you want your Adobe Experience Manager as a Cloud Service external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Adobe Experience Manager as a Cloud Service external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create an Adobe Experience Manager as a Cloud Service external content connector](create-ext-cont-connector-adobe-expmgr-cs.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Adobe Experience Manager as a Cloud Service external content connector crawls all nodes located beneath the `/content/dam` node of its specified source system and sends assets with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the nodes to crawl when running content crawls
-   Inclusion or exclusion filters for the file extensions of assets to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Adobe Experience Manager as a Cloud Service external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Nodes** options:

    -   To crawl all nodes that descend from the specified start node, select **Crawl all nodes**.
    -   To crawl only a specified set of nodes that descend from the specified start node, select **Include only these nodes**, then use the **Add node path to include** field and **Add** button to enter paths for nodes you want the connector to include when crawling.

        As an example, you might enter `/content/dam/en/documentation` to only retrieve searchable content from this descendant node.

    -   To crawl all but a specified set of nodes that descend from the specified start node, select **Exclude only these nodes**, then use the **Add node path to exclude** field and **Add** button to enter paths for nodes you want the connector to exclude when crawling.

        As an example, you might enter `/content/dam/en/engineering-ui-assets` to exclude searchable content from this descendant node.

5.  Select one of the following **Assets** options:

    -   To retrieve all assets with supported file extensions from the source system, select **Crawl all assets**.
    -   To retrieve only assets with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter asset file extensions you want the connector to include when crawling.

        As an example, you might enter `.pdf` to retrieve only assets with the Portable Document Format file type.

    -   To retrieve all assets except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter asset file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude assets with the Comma-Separated Values \(CSV\) file format.

    For details on the supported asset file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

6.  Select **Save and validate**.


## Result

The Adobe Experience Manager as a Cloud Service external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Adobe Experience Manager as a Cloud Service source system using your modified crawl settings, create and run a one-time content crawl for your Adobe Experience Manager as a Cloud Service external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Adobe Experience Manager as a Cloud Service external content connector](../concept/adobe-expmgr-cs-external-content-connector.md)

