---
title: Statistics for external content connector user permissions crawls
description: Each crawl history entry for an external content connector's user permissions crawl includes statistics about the permissions \(user and group-membership security principals\) retrieved by the crawl.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/permission-statistics-external-content-connectors.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Statistics for external content connector user permissions crawls

Each crawl history entry for an external content connector's user permissions crawl includes statistics about the permissions \(user and group-membership security principals\) retrieved by the crawl.

|Permission statistics entry|Description|
|---------------------------|-----------|
|Mapped users|Score shows the number of users from the source system that were successfully mapped to users on your ServiceNow AI Platform® instance by the user permissions crawl.|
|Unmapped users|Score shows the number of users from the source system that weren't mapped to users on your ServiceNow AI Platform instance by the user permissions crawl.|
|Error|Score shows the number of Error-level alerts recorded for the user permissions crawl. Select **Details** to view the Alerts tab for the crawl history entry.|
|Warning|Score shows the number of Warning-level alerts recorded for the user permissions crawl. Select **Details** to view the Alerts tab for the crawl history entry.|
|Users|
|Users|Score shows the total number of users that were added to the AI Search index by the user permissions crawl.|
|Discovered|Score shows the number of users that were processed by the user permissions crawl.|
|Deleted|Score shows the number of users that were deleted from the AI Search index by the user permissions crawl.|
|Groups|
|Discovered|Score shows the number of group-membership permissions that were processed by the user permissions crawl.|
|Deleted|Score shows the number of group-membership permissions that were deleted from the AI Search index by the user permissions crawl.|

|Performance statistics entry|Description|
|----------------------------|-----------|
|Average crawl speed|Score shows the average speed of the user permissions crawl, expressed in users processed per second of crawl time.|

**Parent Topic:**[External Content Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/reference-ext-cont-connectors.md)

