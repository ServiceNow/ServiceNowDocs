---
title: SharePoint Online Search Connector reference
description: The reference topics for the application provide additional information about the SharePoint Online Search Connector settings, content types, and features.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SharePoint Online Search Connector, Employee Service Management]
---

# SharePoint Online Search Connector reference

The reference topics for the application provide additional information about the SharePoint Online Search Connector settings, content types, and features.

## Crawl constraints

For more information on crawl types, see [Microsoft SharePoint crawl types](../concept/sp-crawl-types.md).

-   The time of crawling may vary, based on the content size.
-   The documents are available for search after a successful crawl.

**Note:** For the latest information on the content types and constraints, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) documentation.

## Scheduled job frequency

The default-scheduled job frequency is set to maximize the performance. For more information, see [SharePoint Online Search Connector scheduled jobs](../concept/sharepoint-scheduled-jobs-full-crawl.md).

## Look up file permissions

When Look up File Permissions action returns a blank or null array, you may face access issues. To resolve the access issue, use the Client Credentials type instead of Authorization Code and provide the API permissions on the application level where the type is application, for more information, see [KB1642515](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642515).

## Content types

-   The content types supported by the AI Search are supported in the SharePoint Online Search Connector.
-   The AI Search file size maximum of 25 MB applies.
-   The languages supported are English, Spanish, French, Japanese, and German.

## Reduce batch size value and execution time

The **sn\_sp\_con.sharepoint\_batch\_size** property controls the size of the batch in SharePoint and the default value is 200. You can update this value to reduce the batch size and the execution time of the Index flows. Navigate to System Properties **sys\_properties\_list.do**, search for **sn\_sp\_con.sharepoint\_batch\_size**, and reduce the value.

## Delegated permissions and Application permissions

When you want the search results to display only the published versions of a document, ensure you select **Application permissions** instead of the **Delegated permissions** while configuring the permissions explained in [Configure the Microsoft SharePoint tenant](../concept/setup-sp-ovrvw.md#). Admins can limit indexing only the published versions only, ensuring that drafts or unfinished work are not displayed in the search results.​

