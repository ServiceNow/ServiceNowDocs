---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2026-09-03"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI]
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.

## About External Content Connectors

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

See [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ext-cont-connectors-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Browser requirements**

    For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.

-   **Additional requirements**

    Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-admin-rn-landing.md)

## Version 8.1

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.

### What's new

-   **[Filter content by label for a Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/filter-content-label-google-drive-external-content-connector.md)**

    Configure your Google Drive external content connectors to only retrieve content items that have one or more of a specified set of label values applied.


## Version 6.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.

### What's new

-   **[Adobe Acrobat Sign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/adobe-acrobat-sign-external-content-connector.md)**

    Retrieve searchable content and metadata from your Adobe Acrobat Sign source system.

-   **[Aha! Roadmaps external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/aha-roadmaps-external-content-connector.md)**

    Retrieve searchable content and metadata from your Aha! Roadmaps source system.

-   **[Cornerstone external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/cornerstone-external-content-connector.md)**

    Retrieve searchable content and metadata from your Cornerstone source system.

-   **[Fluid Topics external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/fluid-topics-external-content-connector.md)**

    Retrieve searchable content and metadata from your Fluid Topics source system.

-   **[ManageEngine external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/manageengine-external-content-connector.md)**

    Retrieve searchable content and metadata from your ManageEngine source system.

-   **[Workvivo external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/workvivo-external-content-connector.md)**

    Retrieve searchable content and metadata from your Workvivo source system.


### What's changed

-   **[Sitemap support in the Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-content-crawl-external-content-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/review-crawl-ext-cont-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/atlassian-confluence-cloud-external-content-connector.md) Confluence Cloud external content connector**

    Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


## Version 5.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.

### What's new

-   **[Connector admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/installed-with-ext-content-connectors.md)**

    Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/adobe-expmgr-cs-external-content-connector.md)**

    Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/asana-external-content-connector.md)**

    Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/docusign-external-content-connector.md)**

    Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dropbox-external-content-connector.md)**

    Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/github-enterprise-cloud-external-content-connector.md)**

    Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/hubspot-external-content-connector.md)**

    Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/lucidchart-external-content-connector.md)**

    Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/miro-external-content-connector.md)**

    Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monday-com-external-content-connector.md)**

    Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/notion-external-content-connector.md)**

    Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/sap-dms-external-content-connector.md)**

    Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/smartsheet-external-content-connector.md)**

    Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/trello-external-content-connector.md)**

    Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/wordpress-external-content-connector.md)**

    Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/workday-external-content-connector.md)**

    Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/zoom-external-content-connector.md)**

    Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user permission settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configure-user-mapping-settings-external-content-connector.md)**

    Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for external content connector content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/document-statistics-external-content-connectors.md)**

    Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/permission-statistics-external-content-connectors.md)**

    Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/analytics-external-content-connectors.md)**

    Review metrics that show how your external content connector has run over time.


### What's changed

-   **[Connector creation UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/creating-ext-cont-connectors.md)**

    The connector creation UI now includes optional steps for configuring user permission crawls \(for connectors that support them\) and for linking connector search sources to your search profiles. If you want to change these settings for an existing connector, you can configure these settings from the connector editor.


-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/analytics-external-content-connectors.md)**

    Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-jira.md)**

    The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-microsoft-onedrive.md)**

    The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-mspo.md)**

    The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-msteams.md)**

    The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


## Version 4.1

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.

### What's new

-   **[Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/amazon-s3-external-content-connector.md)**

    Retrieve searchable content and metadata from buckets in your Amazon S3 source system.

-   **[Box external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/box-external-content-connector.md)**

    Retrieve searchable content and metadata from user boxes in your Box source system.

-   **[GitLab external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/gitlab-external-content-connector.md)**

    Retrieve searchable content and metadata from issues, wikis, merge requests, tags, branches, and commits in your GitLab source system's groups, projects, and repositories.

-   **[Microsoft OneDrive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/microsoft-onedrive-external-content-connector.md)**

    Retrieve searchable content and metadata from individual drives in your Microsoft OneDrive source system.

-   **[Microsoft Viva Engage external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/microsoft-viva-engage-external-content-connector.md)**

    Retrieve searchable content and metadata from conversations in your Microsoft Viva Engage source system's communities.

-   **[ServiceNow® instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/servicenow-instance-external-content-connector.md)**

    Retrieve searchable content and metadata from KB articles in your ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Retrieve searchable content and metadata from pages and subdomains in public web sources. Select a predefined web source or specify a custom web source.

-   **[Zendesk Guide external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/zendesk-guide-external-content-connector.md)**

    Retrieve searchable content and metadata from articles in your Zendesk Guide source system's knowledge bases.

-   **[Statistics for external content connector content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/document-statistics-external-content-connectors.md)**

    Review statistics for searchable items retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/permission-statistics-external-content-connectors.md)**

    Review statistics for user and group permissions retrieved by a user permission crawl.


### What's changed

-   **[Connector creation UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/creating-ext-cont-connectors.md)**

    The connector creation UI now includes optional steps for configuring the new connector's crawl settings and creating and scheduling crawls for it. You can still configure these settings from the connector's editor, so you can skip these steps during connector creation if you want to configure crawl settings and create crawls later on.


-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/webcrawler-external-content-connector.md)**

    The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which enables you to specify a custom web source or select a predefined one.


## Version 4.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Zurich release.

### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


