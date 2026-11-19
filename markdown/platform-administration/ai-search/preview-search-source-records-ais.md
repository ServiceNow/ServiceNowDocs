---
title: Preview matching records for an AI Search search source
description: View the ServiceNow AI Platform table records that match a search source's indexed source table and filter conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/preview-search-source-records-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-28"
reading_time_minutes: 1
breadcrumb: [Search sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Preview matching records for an AI Search search source

View the ServiceNow AI Platform® table records that match a search source's indexed source table and filter conditions.

## Before you begin

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Sources**.

2.  Open the search source that you want to preview matching records for.

3.  On the Search Source form, select the **preview** link in the informational message that reports the number of matching records.

    For a description of the field values, see [Search Source form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/search-source-form-ais.md).


## Result

The ServiceNow AI Platform table specified in the search source's indexed source appears, with filter conditions applied to match conditions from the search source. This filtered view displays all records that are searchable through the search source.

**Note:** Preview uses the saved conditions from the search source. If you change a search source's conditions, preview doesn't reflect your changes until you save them.

**Parent Topic:**[Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/search-sources-ais.md)

