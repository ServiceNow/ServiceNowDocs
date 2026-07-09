---
title: Unsupported field types in Query Generation
description: Query Generation explicitly does not support some field types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/querygen-unsupported-field-types.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Unsupported field types in Query Generation

Query Generation explicitly does not support some field types.

## Unsupported field types

-   Variables
-   Tags
-   Domain Path

Reference fields are supported, but the referenced table must be included in the semantic layer. For example, a user query on caller\_id.department succeeds only if the Department table is in the semantic layer.

**Parent Topic:**[Query Generation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/query-generation-reference.md)

