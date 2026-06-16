---
title: External Content Connectors Application Suite release notes
description: Version history for the External Content Connectors Application Suite application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-nowintel-external-content-connectors-app-suite.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# External Content Connectors Application Suite release notes

Version history for the External Content Connectors Application Suite application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.0.10 - June 2026**
    -   New:
        -   SAP SuccessFactors external content connector
        -   Multimodal caption generation for retrieved attachments and files
    -   Changed: Global Retry Strategy — exponential backoff implemented for 50x, 429, and 408 HTTP errors across connectors
    -   Fixed:
        -   WebCrawler stability, performance, error handling, and quality improvements
        -   Source system improvements for connector reliability and data handling
-   **Version 7.0.5 - April 2026**
    -   New:
        -   Added predefined web sources for servicenow.com, developer.servicenow.com, community.servicenow.com, support.servicenow.com, horizon.servicenow.com, and Copilot
        -   Webcrawler now supports extraction of all results from the ServiceNow developer blog
        -   Added user.countrycrawl filter option for the Microsoft SharePoint Online connector
        -   Added support for multiple ServiceNow Product Docs connector instances
        -   Suppress quota consumption for ServiceNow instance and ServiceNow product documentation connector transactions
        -   Added label tag to schema for Google Drive connector
    -   Changed:
        -   Improved admin experience with more responsive UI
        -   Improved timeout handling for Webcrawler on long running webcrawls
        -   Consistent user discovery count enforced across all external content connectors
    -   Fixed:
        -   Connectors loading very slowly due to recrawl required state processing
        -   Microsoft SharePoint Online user mappings failing to run; crawl failing with multiple errors
        -   OutOfMemory exceptions when crawling Microsoft SharePoint Online lists
        -   Table link in crawl report details view not filtering the target table correctly
        -   Crawl history for start points scan not showing the number of start points discovered
-   **Version 6.0.8 - March 2026**
    -   New:
        -   New External Content Connectors \(XCC\):​
            -   Adobe Sign
            -   Aha! Roadmap
            -   Cornerstone
            -   Fluid Topics
            -   Workvivo
        -   Add/Delete linking search sources/search profiles from the "Index Management" settings &gt; "Connected search profile" interface of XCC Admin UI.
        -   Validate mTLS connections before setting up XCC and provide warning messages.
    -   Changed:
        -   Scalable indexing: Crawl and index up to 10 million documents per connector.
        -   Unique names will be enforced for connectors.
        -   Crawls are automatically resumed to mitigate interruptions caused by temporary crawling issues.
    -   Fixed: Defect fixes across the connectors improving the XCC Admin experience
-   **Version 6.0.6 - March 2026**
    -   New:
        -   New External Content Connectors \(XCC\):​
            -   Adobe Sign
            -   Aha! Roadmap
            -   Cornerstone
            -   Fluid Topics
            -   Workvivo
        -   Add/Delete linking search sources/search profiles from the "Index Management" settings &gt; "Connected search profile" interface of XCC Admin UI.
        -   Validate mTLS connections before setting up XCC and provide warning messages.
    -   Changed:
        -   Scalable indexing: Crawl and index up to 10 million documents per connector.
        -   Unique names will be enforced for connectors.
        -   Crawls are automatically resumed to mitigate interruptions caused by temporary crawling issues.
    -   Fixed: Defect fixes across the connectors improving the XCC Admin experience
-   **Version 5.0.33 - February 2026**
    -   Fixed:
        -   Fixes in ServiceNow product documentation connector, Webcrawler predefined sources
        -   Minor fixes
-   **Version 5.0.26 - December 2025**
    -   New:
        -   New external content connectors:​
            -   Adobe Experience Manager as a Cloud Service
            -   Asana
            -   Docusign
            -   Dropbox
            -   GitHub
            -   HubSpot
            -   Lucidchart
            -   Miro
            -   monday.com
            -   Notion
            -   SAP DMS
            -   Smartsheet
            -   Trello
            -   Wordpress
            -   Workday
            -   Zoom
            -   Link external content connector search sources to search profiles in AI Search
            -   Validate connection permissions​ during connector creation
            -   Connector analytics
    -   Changed:
        -   Customizable user mapping​ settings for user permission crawls
        -   Improved management of recrawl status, force refeed​ Enhancements in metrics, error reporting
-   **Version 4.1.7 - September 2025**

    New: Support for creating multiple connectors of the same type.

-   **Version 4.0.27 - August 2025**
    -   Changed:
        -   Fixed bugs
        -   UI improvements based on feedback
-   **Version 3.0.25 - May 2025**
    -   The External Content Connectors application helps organizations bring external data repositories into AI Search, offering a seamless and secure way to unify content across systems. With support for ServiceNow documentation and external platforms like Atlassian Confluence Cloud, Microsoft SharePoint Online and more, users can access both internal and external data in one cohesive search experience.
    -   A dedicated, user-friendly UI makes it easy for administrators to manage the entire process from configuring connections and setting up crawls to monitoring performance and reviewing results. Flexible options allow you to define crawl schedules, refine content inclusion and exclusion rules, and map user permissions effortlessly, ensuring only authorized access to data.
    -   By centralizing content from multiple sources and integrating it with AI Search, External Content Connectors improves productivity, improves search accuracy, and makes it simpler for organizations to access the information they need.

**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

