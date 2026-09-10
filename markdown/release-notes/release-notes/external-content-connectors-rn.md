---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-09-03"
reading_time_minutes: 5
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.

## About External Content Connectors

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

See [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Browser requirements**

    For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.

-   **Additional requirements**

    Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-admin-rn-landing.md)

## Version 9.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.

### What's new

-   **Connector health dashboard**

    View and resolve connector health issues using the connector health dashboard.

-   **Index inspector tool**

    Verify indexing status and error counts for individual content items using the index inspector tool. Optionally review additional item details, see which users and groups can view the item in secure search, and view retrieval and indexing errors for the item.

-   **[Advanced connection settings for the Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-ext-cont-connector-amazon-s3.md)**

    Optionally specify advanced connection settings including the AWS region and Amazon S3 endpoint you want the connector to use. You can also specify a list of Amazon S3 buckets to retrieve content from, or leave this list empty to enable auto-discovery of buckets.

-   **Delta content crawls for the Google Drive connector**

    Reduce content crawl time with delta content crawls. Unlike full content crawls, delta content crawls ignore unchanged content items in a connector's source system. Delta content crawls are supported for the Google Drive external content connector.


### What's changed

-   **[Crawl schedules tab renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-content-crawl-external-content-connector.md)**

    In the external content connector editor, the **Crawl schedules** tab has been renamed to **Manage crawls**.


## Version 8.1

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Filter content by label for a Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/filter-content-label-google-drive-external-content-connector.md)**

    Configure your Google Drive external content connectors to only retrieve content items that have one or more of a specified set of label values applied.


## Version 8.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.

### What's new

-   **[SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/sap-successfactors-external-content-connector.md)**

    Retrieve searchable content and metadata exported from your SAP SuccessFactors Learning source system.

-   **[Configuring crawl settings for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/cfg-crawl-settings-ext-cont-connector.md)**

    Activate multimodal captioning for attachments and files retrieved by your external content connector's content crawls. The multimodal service automatically generates captions for images, tables, charts, and complex layouts in the retrieved attachments and files. Searches can match attachment and file results using keywords from the generated captions.


### What's changed

-   **[ServiceNow® instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/servicenow-instance-external-content-connector.md)**

    You can now create and run multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Connector admins can now schedule crawls on a daily, weekly, or monthly basis for all Webcrawler external content connectors.


## Version 6.0

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Adobe Acrobat Sign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/adobe-acrobat-sign-external-content-connector.md)**

    Retrieve searchable content and metadata from your Adobe Acrobat Sign source system.

-   **[Aha! Roadmaps external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/aha-roadmaps-external-content-connector.md)**

    Retrieve searchable content and metadata from your Aha! Roadmaps source system.

-   **[Cornerstone external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/cornerstone-external-content-connector.md)**

    Retrieve searchable content and metadata from your Cornerstone source system.

-   **[Fluid Topics external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/fluid-topics-external-content-connector.md)**

    Retrieve searchable content and metadata from your Fluid Topics source system.

-   **[ManageEngine external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/manageengine-external-content-connector.md)**

    Retrieve searchable content and metadata from your ManageEngine source system.

-   **[Workvivo external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/workvivo-external-content-connector.md)**

    Retrieve searchable content and metadata from your Workvivo source system.


### What's changed

-   **[Sitemap support in the Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-content-crawl-external-content-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/review-crawl-ext-cont-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/atlassian-confluence-cloud-external-content-connector.md) Confluence Cloud external content connector**

    Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


