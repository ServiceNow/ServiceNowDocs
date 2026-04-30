---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-18"
reading_time_minutes: 3
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Xanadu release.

## External Content Connectors highlights for the Xanadu release

-   Expand your search by indexing searchable content and user permissions from your Atlassian Jira Cloud, Google Drive, Microsoft Teams, and Slack source systems.
-   Make web content locally searchable by indexing pages from predefined public web sites or from the ServiceNow product documentation site.
-   Know when your external content connectors are approaching their crawl limits with new warning messages.
-   Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.
-   Improve recall for external content searches with support for semantic vector indexing of crawled content.

See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

**Important:** External Content Connectors is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading External Content Connectors to Xanadu

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

## New in the Xanadu release

-   **[Atlassian Jira Cloud external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content and user permissions from projects in your Atlassian Jira Cloud source system.

-   **[Google Drive external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-gdrive&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content and user permissions from shared drives in your Google Drive source system.

-   **[Microsoft Teams external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content and user permissions from teams in your Microsoft Teams source system.

-   **[Predefined web sources external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-websources&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content from pages and subdomains in predefined public web sites.

-   **[ServiceNow product documentation external content connectors](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-snowdoc&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content from the ServiceNow product documentation site.

-   **[Slack external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-slack&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Retrieve searchable content and user permissions from public channels in your Slack source system.

-   **[Warning messages for indexed document counts](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When an external content connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit of 1,000,000 documents.

-   **[Add external content search results to Now Assist in Virtual Agent conversations](https://www.servicenow.com/docs/access?context=add-ext-cont-srch-src-na-va&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.


-   **[Semantic vector indexing for crawled content](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


## UI changes

-   **[New UI for creating external content connectors](https://www.servicenow.com/docs/access?context=creating-ext-cont-connectors&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    On the External Content Admin Home page, you now select **New** instead of **Create** to create a new connector. Next, you select the appropriates source system type on the Choose source page. Finally, you fill in required values on the Connector details page.


## Activation information

Install External Content Connectors by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Configure search applications to display results indexed by your external content connectors.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

