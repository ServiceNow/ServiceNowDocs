---
title: Statistics for external content connector user permission crawls
description: Each crawl history entry for an external content connector's user permission crawl crawl includes statistics about the permissions \(user and group-membership security principals\) retrieved by the crawl.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-10-29"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Statistics for external content connector user permission crawls

Each crawl history entry for an external content connector's user permission crawl crawl includes statistics about the permissions \(user and group-membership security principals\) retrieved by the crawl.

|Permission statistics entry|Description|
|---------------------------|-----------|
|Mapped users|Score shows the number of users from the source system that were successfully mapped to users on your ServiceNow AI Platform® instance by the user permission crawl.|
|Unmapped users|Score shows the number of users from the source system that weren't mapped to users on your ServiceNow AI Platform instance by the user permission crawl.|
|Error|Score shows the number of Error-level alerts recorded for the user permission crawl. Select **Details** to view the Alerts tab for the crawl history entry.|
|Warning|Score shows the number of Warning-level alerts recorded for the user permission crawl. Select **Details** to view the Alerts tab for the crawl history entry.|
|Users|
|Users|Score shows the total number of users that were added to the AI Search index by the user permission crawl.|
|Discovered|Score shows the number of users that were processed by the user permission crawl.|
|Deleted|Score shows the number of users that were deleted from the AI Search index by the user permission crawl.|
|Groups|
|Discovered|Score shows the number of group-membership permissions that were processed by the user permission crawl.|
|Deleted|Score shows the number of group-membership permissions that were deleted from the AI Search index by the user permission crawl.|

|Performance statistics entry|Description|
|----------------------------|-----------|
|Average crawl speed|Score shows the average speed of the user permission crawl, expressed in users processed per second of crawl time.|

**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

