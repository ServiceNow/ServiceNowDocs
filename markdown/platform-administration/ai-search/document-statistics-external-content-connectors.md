---
title: Statistics for external content connector content crawls
description: Each crawl history entry for an external content connector's content crawl includes statistics about the documents \(items or files with searchable content and metadata\) retrieved by the crawl.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Statistics for external content connector content crawls

Each crawl history entry for an external content connector's content crawl includes statistics about the documents \(items or files with searchable content and metadata\) retrieved by the crawl.

<table id="table_ivm_wxv_5gc"><thead><tr><th>

Document statistics entry

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indexed

</td><td>

Score shows the total number of new and updated items that were successfully processed by the content crawl and are included in the AI Search index.

</td></tr><tr><td>

Added

</td><td>

Score shows the number of items that were added to the AI Search index by the content crawl.

</td></tr><tr><td>

Updated

</td><td>

Score shows the number of items that were updated in the AI Search index by the content crawl.

</td></tr><tr><td>

Deleted

</td><td>

Score shows the number of items that were deleted from the AI Search index by the content crawl.

</td></tr><tr><td>

Unchanged

</td><td>

Score shows the number of items that were processed by the content crawl without requiring changes to the AI Search index.

</td></tr><tr><td>

Error

</td><td>

Score shows the number of Error-level alerts recorded for the content crawl. Select **Details** to view the Alerts tab for the crawl history entry.

</td></tr><tr><td>

Warning

</td><td>

Score shows the number of Warning-level alerts recorded for the content crawl. Select **Details** to view the Alerts tab for the crawl history entry.

</td></tr><tr><td>

Discovered

</td><td>

Score shows the total number of items that were processed during the content crawl.Chart shows the number of items processed by the content crawl for each of these result statuses:

-   Indexed: the number of items successfully added to or updated in the AI Search index.
-   Skipped: the number of items not added to or updated in the AI Search index because they don't satisfy indexing limits. This includes binary files that exceed the 25 MB file-size limit as well as binary files with unsupported file formats. For the list of supported binary file formats, see [Binary file extensions supported in External Content Connectors](file-extensions-ext-cont-connector.md).
-   Not indexed: the number of items not added to or updated in the AI Search index because of processing errors.

</td></tr></tbody>
</table>|Performance statistics entry|Description|
|----------------------------|-----------|
|Average crawl speed|Score shows the average speed of the content crawl, expressed in documents \(items\) processed per second of crawl time.|

**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

