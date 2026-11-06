---
title: Statistics for external content connector content crawls
description: Each crawl history entry for an external content connector's content crawl includes statistics about the documents \(items or files with searchable content and metadata\) retrieved by the crawl.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/document-statistics-external-content-connectors.html
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-10-21"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
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

Score shows the number of Error-level alerts recorded for the content crawl. Select **Details** to view the **Alerts** tab for the crawl history entry.

</td></tr><tr><td>

Warning

</td><td>

Score shows the number of Warning-level alerts recorded for the content crawl. Select **Details** to view the **Alerts** tab for the crawl history entry.

</td></tr><tr><td>

Discovered

</td><td>

Score shows the total number of items that were processed during the content crawl.Chart shows the number of items processed by the content crawl for each result status shown in the following Discovered item result statuses table.

</td></tr></tbody>
</table><table id="table_jkg_htx_skc"><thead><tr><th>

Result status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indexed

</td><td>

The number of items successfully added to or updated in the AI Search index.

</td></tr><tr><td>

Not indexed

</td><td>

The number of items that weren't added to or updated in the AI Search index because of processing errors.

</td></tr><tr><td>

Skipped

</td><td>

The number of items that were discovered but not added to or updated in the AI Search index. This count includes the following items:-   **Items excluded by an inclusion or exclusion filter specified in the connector's crawl settings**

The connector skips a content item if it's not included in your specified inclusion filter. It similarly skips an item if it's explicitly included in your specified exclusion filter.

**Note:** Items in folders or other locations that are excluded by your inclusion or exclusion filter aren't discovered and so aren't included in the **Skipped** count.

-   **Binary files or attachments with unsupported formats**

The connector skips binary files and attachments with unsupported formats. For the list of supported binary file formats, see [Binary file extensions supported in External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/file-extensions-ext-cont-connector.md).

-   **Binary files or attachments that exceed the maximum attachment file-size limit**

The connector skips binary files and attachments that exceed the 25 MB maximum file-size limit.

-   **Items in excess of the connector's content indexing limit**

When the connector reaches its content indexing limit, it skips all newly found content items. Most connectors are limited to indexing a maximum of one million content items, but some connector types have different content indexing limits.

-   **Items excluded by connector content validation rules**

Individual external content connectors may skip content items for other reasons.


To see why a content item was skipped, you can view its record in the index inspector. For details about using the index inspector, see [Review indexing status for individual content items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/review-indexing-status-content-items.md).

</td></tr></tbody>
</table>|Performance statistics entry|Description|
|----------------------------|-----------|
|Average crawl speed|Score shows the average speed of the content crawl, expressed in documents \(items\) processed per second of crawl time.|

**Parent Topic:**[External Content Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/reference-ext-cont-connectors.md)

