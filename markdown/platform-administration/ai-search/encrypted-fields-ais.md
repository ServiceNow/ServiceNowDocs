---
title: Encrypted fields in AI Search
description: AI Search excludes source record fields encrypted with Encryption Support or Edge Encryption.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/encrypted-fields-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer]
---

# Encrypted fields in AI Search

AI Search excludes source record fields encrypted with Encryption Support or Edge Encryption.

When dealing with an encrypted source record field, AI Search has the following limitations:

-   Content indexing excludes the encrypted field. This exclusion means that search query terms won't match terms from the encrypted field's content.
-   You can't create a facet using the encrypted field.
-   If a search query attempts to filter on the encrypted field, such as when applying an access control list \(ACL\) filter, the search query fails. An `Encrypted Field is not supported` error message is logged.

For detailed descriptions of the encryption options available for source records, see Encryption.

**Parent Topic:**[Administering AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/administer-ais.md)

