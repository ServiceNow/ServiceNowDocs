---
title: Configure crawl settings for a SAP DMS external content connector
description: Specify the folders you want your SAP DMS external content connector to crawl. Define inclusion or exclusion filters to specify which content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP DMS external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a SAP DMS external content connector

Specify the folders you want your SAP DMS external content connector to crawl. Define inclusion or exclusion filters to specify which content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the SAP DMS external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a SAP DMS external content connector](create-ext-cont-connector-sap-dms.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the SAP DMS external content connector crawls all folders and repositories from its specified source system and sends all documents and their attachments with supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for documents to retrieve based on their last modification date
-   Inclusion or exclusion filters for the folders to crawl when running content crawls
-   Inclusion or exclusion filters for the repositories to crawl when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the SAP DMS external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Last modified date** options:

    -   To retrieve content from all documents regardless of their last modification date, select **All**.
    -   To only retrieve content from documents that were last modified in the preceding 365 days, select **Last 365 days**.
    -   To only retrieve content from documents that were last modified in the preceding 180 days, select **Last 180 days**.
    -   To only retrieve content from documents that were last modified in the preceding 90 days, select **Last 90 days**.
    -   To only retrieve content from documents that were last modified in the preceding 30 days, select **Last 30 days**.
    -   To only retrieve content from documents that were last modified in the preceding 7 days, select **Last 7 days**.
5.  Select one of the following **Folders** options:

    -   To crawl all folders from the source system, select **Crawl all folders**.
    -   To crawl only a specified set of folders from the source system, select **Include only these folders**, then use the **Add folder ID to include** field and **Add** button to enter IDs for folders you want the connector to include when crawling.

        As an example, you might enter `9173ggdzt1671gfeja` to only retrieve searchable content from the folder with the specified ID.

    -   To crawl all but a specified set of folders from the source system, select **Exclude only these folders**, then use the **Add folder ID to exclude** field and **Add** button to enter IDs for folders you want the connector to exclude when crawling.

        As an example, you might enter `48dhgdgf16712gvsa` to exclude searchable content from the folder with the specified ID.

6.  Select one of the following **Repositories** options:

    -   To crawl documents from all repositories on the source system, select **Crawl all repositories**.
    -   To crawl only documents from a specified set of repositories on the source system, select **Include only these repositories**, then use the **Add repositories name or ID to include** field and **Add** button to enter names or IDs for repositories you want the connector to include when crawling.

        As an example, you might enter `5b01d7f6-6263-4aeb-9b75-2186db9b201e` and `production-repo` to only retrieve documents from the specified repositories.

    -   To crawl documents from all but a specified set of repositories on the source system, select **Exclude only these repositories**, then use the **Add repositories name or ID to exclude** field and **Add** button to enter names or IDs for repositories you want the connector to exclude when crawling.

        As an example, you might enter `d11d7f07-c4ad-4742-b17d-c078869e54a5` and `test-repo` to exclude documents from the specified repositories.

7.  Select one of the following **Attachments** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file types**, then use the **File types to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file types**, then use the **File types to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

8.  Select **Save and validate**.


## Result

The SAP DMS external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your SAP DMS source system using your modified crawl settings, create and run a one-time content crawl for your SAP DMS external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[SAP DMS external content connector](../concept/sap-dms-external-content-connector.md)

