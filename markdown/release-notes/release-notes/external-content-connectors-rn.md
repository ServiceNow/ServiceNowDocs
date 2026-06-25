---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 3
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors application enables AI Search applications to search content and metadata from supported external source systems, such as Atlassian Confluence Cloud and Microsoft SharePoint Online. External Content Connectors was enhanced and updated in the Australia release.

## External Content Connectors highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Expand your search experience to include content and metadata from your SAP SuccessFactors Learning source system.
-   Improve search recall with automatic multimodal caption generation for images, tables, charts, and complex layouts in attachments and files retrieved by your external content connector's content crawls.
-   Make more content searchable by creating and running multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.
-   Increase flexibility by scheduling crawls on a daily, weekly, or monthly basis for your Webcrawler external content connectors.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Expand your search experience with external content connectors for Adobe Acrobat Sign, Aha! Roadmaps, Cornerstone, Fluid Topics, ManageEngine, and Workvivo source systems.
-   Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector.
-   View a content crawl's start point via links in the content crawl list and in content crawl history entries.

See [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md) for more information.

**Important:** External Content Connectors is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/sap-successfactors-external-content-connector.md)**

    Retrieve searchable content and metadata exported from your SAP SuccessFactors Learning source system.

-   **[Configuring crawl settings for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/cfg-crawl-settings-ext-cont-connector.md)**

    Activate multimodal captioning for attachments and files retrieved by your external content connector's content crawls. The multimodal service automatically generates captions for images, tables, charts, and complex layouts in the retrieved attachments and files. Searches can match attachment and file results using keywords from the generated captions.


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


## Changed in this release

-   **[ServiceNow® instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/servicenow-instance-external-content-connector.md)**

    You can now create and run multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Connector admins can now schedule crawls on a daily, weekly, or monthly basis for all Webcrawler external content connectors.


-   **[Sitemap support in the Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/webcrawler-external-content-connector.md)**

    Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-content-crawl-external-content-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/review-crawl-ext-cont-connector.md)**

    View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/atlassian-confluence-cloud-external-content-connector.md) Confluence Cloud external content connector**

    Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


## Activation information

Install External Content Connectors by requesting the External Content Connectors Application Suite from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/overview-ais.md)**

    Configure search applications to display results indexed by your external content connectors.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-admin-rn-landing.md)

