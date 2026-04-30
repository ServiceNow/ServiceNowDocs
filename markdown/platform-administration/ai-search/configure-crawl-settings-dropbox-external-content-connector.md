---
title: Configure crawl settings for a Dropbox external content connector
description: Specify the user and team folders you want your Dropbox external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-09"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Dropbox external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Dropbox external content connector

Specify the user and team folders you want your Dropbox external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Dropbox external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Dropbox external content connector](create-ext-cont-connector-dropbox.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Dropbox external content connector crawls all user and team folders from its specified source system and sends all content and binary files with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to ignore user or team folder content, or to use any of the following non-default settings:

-   Inclusion or exclusion filters for the user folders to crawl when running content crawls
-   Inclusion or exclusion filters for the team folders to crawl when running content crawls
-   Inclusion or exclusion filters for the binary file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Dropbox external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Deselect the **Crawl user content** option or the **Crawl team content** option depending on what content type you want the connecor to retrieve.

    **Note:** If you deselect both content options, the connector won't retrieve any content from your source system.

5.  If you selected **Crawl user content**, select one of the following **User content** options:

    -   To crawl all user folders from the source system, select **Crawl all users**.
    -   To crawl only a specified set of user folders from the source system, select **Include only these users**, then use the **Include only these users** field and **Add** button to enter email addresses for users whose folders you want the connector to include when crawling.

        As an example, you might enter `beth.anglin@example.com` to only retrieve searchable content from this user's folder.

    -   To crawl all but a specified set of user folders from the source system, select **Exclude only these users**, then use the **Exclude only these users** field and **Add** button to enter email addresses for users whose folders you want the connector to exclude when crawling.

        As an example, you might enter `abel.tuter@example.com` to exclude searchable content from this user's folder.

6.  If you selected **Crawl team content**, select one of the following **Team folder content** options:

    -   To crawl all team folders from the source system, select **Crawl all team folders**.
    -   To crawl only a specified set of team folders from the source system, select **Include only these team folders**, then use the **Include only these team folders** field and **Add** button to enter names for team folders you want the connector to include when crawling.

        As an example, you might enter `Marketing` and `AI Ambassadors` to only retrieve searchable content from these team folders.

    -   To crawl all but a specified set of team folders from the source system, select **Exclude only these team folders**, then use the **Exclude only these team folders** field and **Add** button to enter names for team folders you want the connector to exclude when crawling.

        As an example, you might enter `Legal` to exclude searchable content from this team folder.

7.  Select one of the following **Files** options:

    -   To retrieve all files with supported extensions from the source system, select **Crawl all files**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only files with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude files with the Comma-Separated Values \(CSV\) file format.

    For details on the supported file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

8.  Select **Save and validate**.


## Result

The Dropbox external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Dropbox source system using your modified crawl settings, create and run a one-time content crawl for your Dropbox external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Dropbox external content connector](../concept/dropbox-external-content-connector.md)

