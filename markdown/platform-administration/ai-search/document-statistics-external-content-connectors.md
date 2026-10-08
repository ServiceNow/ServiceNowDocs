---
title: Statistics for external content connector content crawls
description: Each crawl history entry for an external content connector's content crawl includes statistics about the documents \(items or files with searchable content and metadata\) retrieved by the crawl.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/document-statistics-external-content-connectors.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
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

The number of items that weren't added to or updated in the AI Search index for any of the following reasons:-   **The item doesn't satisfy indexing limits**

The connector skips an item when any of these conditions is true.

    -   The item is a binary file/attachment with an unsupported format. For the list of supported binary file formats, see [Binary file extensions supported in External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/file-extensions-ext-cont-connector.md).
    -   The item is a binary file/attachment that exceeds the maximum file-size limit \(25 MB\).
    -   The connector has reached its content indexing limit.
-   **The item is excluded by an inclusion or exclusion filter in the connector's crawl settings**

The connector skips an item if it or its location is not included in your specified inclusion filter. It similarly skips an item if it or its location is explicitly included in your specified exclusion filter.

-   **The item doesn't satisfy the connector's content validation rules**

Individual external content connectors have their own validation rules that determine what content they accept for indexing. As an example, the Webcrawler external content connector rejects HTML pages that don't have a title element. The connector skips any item that doesn't satisfy its content validation rules.


</td></tr></tbody>
</table>|Performance statistics entry|Description|
|----------------------------|-----------|
|Average crawl speed|Score shows the average speed of the content crawl, expressed in documents \(items\) processed per second of crawl time.|

**Parent Topic:**[External Content Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/reference-ext-cont-connectors.md)

