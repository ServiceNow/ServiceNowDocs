---
title: AI Search spoke release notes
description: Version history for the AI Search spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ai-search.html
release: store
topic_type: reference
last_updated: "2023-09-20"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# AI Search spoke release notes

Version history for the AI Search spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.3 - September 2023**

    Fixed: The license requirements.

-   **Version 2.0.2 - April 2023**

    Improved installation performance.

-   **Version 2.0.1 - February 2022**
    -   New:
        -   Delete Document action to delete a single indexed document.
        -   Delete Documents action to delete all indexed documents from an external content schema table \(with optional Glide query parameter to limit the set of documents deleted\).
    -   Changed:
        -   Flush Ingestion action renamed Commit Index.
        -   This version allows security principals to be added to content ingested for AI Search via IntegrationHub actions and optional parameters.
    -   Removed:
        -   Delete By Query action \(use new Delete Document or Delete Documents actions instead\).
        -   Ingest Data action \(use new Ingest Document action instead\).
        -   Ingest Document With Principal action \(use new Ingest Document action with optional security principal parameter instead\).
        -   Purge All Documents action \(use new Delete Documents action instead\).
        -   Remove Documents action \(use new Delete Documents action instead\).
-   **Version 1.0.0 - January 2021**

    Provides actions to automate interactions with AI Search.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

