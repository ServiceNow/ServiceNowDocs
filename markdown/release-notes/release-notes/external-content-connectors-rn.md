---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-12"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Yokohama release.

## External Content Connectors highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Expand your search experience with external content connectors for Adobe Experience Manager as a Cloud Service, Asana, Docusign, Dropbox, GitHub Enterprise Cloud, HubSpot, Lucidchart, Miro, monday.com, Notion, SAP DMS, Smartsheet, Trello, WordPress, Workday, and Zoom source systems.
-   Customize user permission settings, choosing the fields you want to compare when mapping source system users to ServiceNow AI Platform® users.
-   Make external content connector crawl results searchable by linking connector search sources to search profiles from the connector editor.
-   Monitor connector behavior on individual crawl runs and over time with improved crawl statistics and analytics.

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   Expand your search experience by indexing searchable content from your Amazon S3, Box, GitLab, Microsoft OneDrive, Microsoft Viva Engage, and Zendesk Guide source systems.
-   Search KB articles from your ServiceNow instance.
-   Make web content locally searchable by indexing pages from predefined or custom public web sites with the Webcrawler external content connector.
-   Configure connector settings and schedule crawls as part of connector creation using the revamped UI.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Expand your search by indexing searchable content from your Atlassian Jira Cloud, Google Drive, Microsoft Teams, and Slack source systems.
-   Make web content locally searchable by indexing pages from predefined public web sites.
-   Find answers about your ServiceNow deployment by indexing searchable content from the ServiceNow product documentation.
-   Know when your external content connectors are approaching their crawl limits with new warning messages.
-   Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.
-   Improve recall for external content searches with support for semantic vector indexing of crawled content.

See [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ext-cont-connectors-landing-page.md) for more information.

**Important:** External Content Connectors is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading External Content Connectors to Yokohama

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

## New in the Yokohama release

-   **[Connector admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/installed-with-ext-content-connectors.md)**

    Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/adobe-expmgr-cs-external-content-connector.md)**

    Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/asana-external-content-connector.md)**

    Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/docusign-external-content-connector.md)**

    Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/dropbox-external-content-connector.md)**

    Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/github-enterprise-cloud-external-content-connector.md)**

    Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/hubspot-external-content-connector.md)**

    Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/lucidchart-external-content-connector.md)**

    Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/miro-external-content-connector.md)**

    Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monday-com-external-content-connector.md)**

    Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/notion-external-content-connector.md)**

    Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/sap-dms-external-content-connector.md)**

    Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/smartsheet-external-content-connector.md)**

    Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/trello-external-content-connector.md)**

    Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/wordpress-external-content-connector.md)**

    Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/workday-external-content-connector.md)**

    Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/zoom-external-content-connector.md)**

    Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user permission settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/configure-user-mapping-settings-external-content-connector.md)**

    Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for external content connector content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/document-statistics-external-content-connectors.md)**

    Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/permission-statistics-external-content-connectors.md)**

    Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/analytics-external-content-connectors.md)**

    Review metrics that show how your external content connector has run over time.


-   **[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/amazon-s3-external-content-connector.md)**

    Retrieve searchable content and metadata from buckets in your Amazon S3 source system.

-   **[Box external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/box-external-content-connector.md)**

    Retrieve searchable content and metadata from user boxes in your Box source system.

-   **[GitLab external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/gitlab-external-content-connector.md)**

    Retrieve searchable content and metadata from issues, wikis, merge requests, tags, branches, and commits in your GitLab source system's groups, projects, and repositories.

-   **[Microsoft OneDrive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/microsoft-onedrive-external-content-connector.md)**

    Retrieve searchable content and metadata from individual drives in your Microsoft OneDrive source system.

-   **[Microsoft Viva Engage external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/microsoft-viva-engage-external-content-connector.md)**

    Retrieve searchable content and metadata from conversations in your Microsoft Viva Engage source system's communities.

-   **[ServiceNow® instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/servicenow-instance-external-content-connector.md)**

    Retrieve searchable content and metadata from KB articles in your ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Retrieve searchable content and metadata from pages and subdomains in public web sources. Select a predefined web source or specify a custom web source.

-   **[Zendesk Guide external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/zendesk-guide-external-content-connector.md)**

    Retrieve searchable content and metadata from articles in your Zendesk Guide source system's knowledge bases.

-   **[Statistics for external content connector content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/document-statistics-external-content-connectors.md)**

    Review statistics for searchable items retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/permission-statistics-external-content-connectors.md)**

    Review statistics for user and group permissions retrieved by a user permission crawl.


-   **[Atlassian Jira Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-jira.md)**

    Retrieve searchable content and user permissions from projects in your Atlassian Jira Cloud source system.

-   **[Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-gdrive.md)**

    Retrieve searchable content and user permissions from shared drives in your Google Drive source system.

-   **[Microsoft Teams external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-msteams.md)**

    Retrieve searchable content and user permissions from teams in your Microsoft Teams source system.

-   **[ServiceNow product documentation external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-snowdoc.md)**

    Retrieve searchable content from the ServiceNow product documentation site.

-   **[Slack external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-slack.md)**

    Retrieve searchable content and user permissions from public channels in your Slack source system.

-   **[Warning messages for indexed document counts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/exploring-ext-cont-connectors.md)**

    When an external content connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit of 1,000,000 documents.

-   **[Add external content search results to Now Assist in Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/add-ext-cont-srch-src-na-va.md)**

    Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.


-   **[Semantic vector indexing for crawled content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/semantic-search-ais.md)**

    Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


## UI changes

-   **[Connector creation UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/creating-ext-cont-connectors.md)**

    The connector creation UI now includes optional steps for configuring user permission crawls \(for connectors that support them\) and for linking connector search sources to your search profiles. If you want to change these settings for an existing connector, you can configure these settings from the connector editor.


-   **[Connector creation UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/creating-ext-cont-connectors.md)**

    The connector creation UI now includes optional steps for configuring the new connector's crawl settings and creating and scheduling crawls for it. You can still configure these settings from the connector editor, so you can skip these steps during connector creation if you want to configure crawl settings and create crawls later on.


-   **[New UI for creating external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/creating-ext-cont-connectors.md)**

    On the External Content Admin Home page, you now select **New** instead of **Create** to create a new connector. Next, you select the appropriate source system type on the Choose source page. Finally, you fill in required values on the Connector details page.


## Changed in this release

-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/analytics-external-content-connectors.md)**

    Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-jira.md)**

    The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-microsoft-onedrive.md)**

    The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-mspo.md)**

    The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-ext-cont-connector-msteams.md)**

    The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/webcrawler-external-content-connector.md)**

    The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which allows you to specify a custom web source or select a predefined one.


## Activation information

Install External Content Connectors by requesting the External Content Connectors Application Suite from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/overview-ais.md)**

    Configure search applications to display results indexed by your external content connectors.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)

