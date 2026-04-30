---
title: Encrypted fields in AI Search
description: AI Search excludes source record fields encrypted with Encryption Support or Edge Encryption.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-16"
reading_time_minutes: 1
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Encrypted fields in AI Search

AI Search excludes source record fields encrypted with Encryption Support or Edge Encryption.

When dealing with an encrypted source record field, AI Search has the following limitations:

-   Content indexing excludes the encrypted field. This exclusion means that search query terms won't match terms from the encrypted field's content.
-   You can't create a facet using the encrypted field.
-   If a search query attempts to filter on the encrypted field, such as when applying an access control list \(ACL\) filter, the search query fails. An `Encrypted Field is not supported` error message is logged.

For detailed descriptions of the encryption options available for source records, see [Encryption](https://www.servicenow.com/docs/access?context=encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Parent Topic:**[Administering AI Search](administer-ais.md)

