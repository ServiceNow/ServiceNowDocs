---
title: Microsoft SharePoint crawl types
description: Crawling gathers the content for search. To retrieve information, the crawl operation connects to the content sources by using connectors.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SharePoint Online Search Connector reference, SharePoint Online Search Connector, Employee Service Management]
---

# Microsoft SharePoint crawl types

Crawling gathers the content for search. To retrieve information, the crawl operation connects to the content sources by using connectors.

To create a modern search experience, the search system must first crawl the content from the multiple content sources. From content sources, specify the content type, the starting URLs, and the depth of content to index.

After retrieving the content, the Crawl component passes the crawled items to the content processing component.

-   **Full Crawl**: Crawls, processes, and indexes every item in the content source, regardless of the last crawl status.
-   **Incremental Crawl**: Crawls, processes, and indexes only the items that are newly created, changed, or updated since the last crawl. This option takes less time and re-indexes only the changes.

