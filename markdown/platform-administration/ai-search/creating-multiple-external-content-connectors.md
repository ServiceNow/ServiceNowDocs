---
title: Creating multiple external content connectors of the same type
description: Admins can create multiple external content connectors of the same type. These connectors can crawl different source systems or the same source system. Connectors that crawl the same source system can include overlapping crawl locations.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-07"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Creating external content connectors, Explore, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Creating multiple external content connectors of the same type

Admins can create multiple external content connectors of the same type. These connectors can crawl different source systems or the same source system. Connectors that crawl the same source system can include overlapping crawl locations.

## Supported configurations

The system supports these configurations for multiple external content connectors of the same type.

-   **Multiple external content connectors of the same type that crawl different source systems**

    For example, one Microsoft SharePoint Online external content connector crawls sites 1A and 1B in source system 1, while a second Microsoft SharePoint Online external content connector crawls sites 2A and 2B in source system 2. The two external content connectors have no sites in common, so there's no duplication of retrieved content.

-   **Multiple external content connectors of the same type that crawl the same source system with distinct crawl scopes**

    For example, one Microsoft SharePoint Online external content connector crawls sites 1A and 1B in source system 1, while a second Microsoft SharePoint Online external content connector crawls sites 1C and 1D in source system 1. The two external content connectors have no sites in common, so there's no duplication of retrieved content.

-   **Multiple external content connectors of the same type that crawl the same source system with overlapping crawl scopes**

    For example, one Microsoft SharePoint Online external content connector crawls sites 1A and 1B in source system 1, while a second Microsoft SharePoint Online external content connector crawls sites 1B and 1C in source system 1. The two external content connectors have site 1B in common, so content from that site may be retrieved by both connectors. There's no duplication of retrieved content from the other sites.


## Behavior notes

When you create multiple external content connectors of the same type, they behave as described in the following list.

-   **All external content connectors of the same type feed their retrieved content to the same indexed source**

    In the previous examples, all content retrieved by either of the two Microsoft SharePoint Online external content connectors would be fed to the SharePoint Online indexed source.

-   **During indexing of crawled content, retrieved items are deduplicated across all external content connectors of the same type**

    As an example, if two different Microsoft SharePoint Online external content connectors both retrieve the same file from the same site, only one copy of the retrieved file is indexed and appears in your search results.

-   **User permissions are specific to an individual external content connector, not shared between all external content connectors of the same type**

    Admins need to run a separate user permission crawl for each external content connector of the same type. In the preceding examples, each Microsoft SharePoint Online external content connector needs its own user permission crawl. Running a user permission crawl for the first Microsoft SharePoint Online external content connector does not populate security principals for the second connector.

-   **The system executes crawl jobs for external content connectors of the same type in parallel if sufficient resources are available**

    If sufficient resources for parallel execution aren't available, the system executes the crawl jobs sequentially instead.

-   **The crawl limit of one million items applies separately to each external content connector of the same type**

    In the preceding examples, each individual Microsoft SharePoint Online external content connector can crawl up to one million items.


## Considerations for parallel execution

When creating multiple external content connectors of the same type, bear the following considerations in mind.

-   **Increased request load on source system**

    Creating multiple external content connectors that crawl the same source system in parallel can increase the rate at which requests are made to the source system. This may trigger rate-limit issues on the source system.

-   **Indexed source contention when running in parallel**

    Running crawl jobs for multiple external content connectors of the same type in parallel can cause contention when they send retrieved content to their shared indexed source. This contention may reduce the connectors' retrieval rate when their crawl jobs are run in parallel.


**Parent Topic:**[Creating external content connectors](../task/creating-ext-cont-connectors.md)

