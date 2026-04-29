---
title: Configure crawl settings for a Zendesk Guide external crawl connector
description: Specify the article locales and attachment file types you want your Zendesk Guide external content connector to crawl when running content crawls. Define inclusion or exclusion filters for domains to restrict the set of users the crawl retrieves access permissions for when running user permission crawls.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Zendesk Guide external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Zendesk Guide external crawl connector

Specify the article locales and attachment file types you want your Zendesk Guide external content connector to crawl when running content crawls. Define inclusion or exclusion filters for domains to restrict the set of users the crawl retrieves access permissions for when running user permission crawls.

## Before you begin

A connector admin must have already created the Zendesk Guide external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Zendesk Guide external content connector](create-ext-cont-connector-zendesk-guide.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Zendesk Guide external content connector crawls all users from the source system during user permission crawls. During content crawls, it defaults to retrieving help center articles from all locales and retrieving all attachments with supported file extensions. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the user accounts to access on the source system when running user permission crawls
-   Inclusion or exclusion filters for the help center article locales to crawl when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Zendesk Guide external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **User permission filtering** options:

    -   To retrieve user permissions for all users from the source system, select **Map all users**.
    -   To only retrieve user permissions for users from specified domains in the source system, select **Map only these users**, then use the **Add domain for user email addresses to include** field and **Add** button to enter domains whose users you want to include in the user permission crawl.

        For example, you might enter `example.com` to include only user permissions for users from the specified domain.

5.  Select one of the following **Locale filtering** options:

    -   To crawl articles from all locales defined in the source system, select **Crawl all locales**.
    -   To crawl only articles from a specified set of locales defined in the source system, select **Include only these locales**, then use the **Locales to include** field to enter identifiers for the locales of articles that you want to include in the crawl.

        For example, you might enter `en-US` and `es-MX` to only crawl searchable content from articles with the US English or Mexican Spanish locales.

    -   To crawl all articles except those from a specified set of locales defined in the source system, select **Exclude only these locales**, then use the **Locales to exclude** field to enter identifiers for the locales of articles that you want to exclude from the crawl.

        For example, you might enter `pt-BR` to exclude searchable content from articles with the Brazilian Portuguese locale.

6.  Select one of the following **Attachment filtering** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

7.  Select **Save and validate**.


## Result

The Zendesk Guide external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Zendesk Guide source system using your modified crawl settings, create and run a one-time content crawl for your Zendesk Guide external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Zendesk Guide external content connector](../concept/zendesk-guide-external-content-connector.md)

