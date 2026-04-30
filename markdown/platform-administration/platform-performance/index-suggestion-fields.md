---
title: Index suggestion form fields
description: A description of the fields in the index suggestion form.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-05-12"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Index suggestion form fields

A description of the fields in the index suggestion form.

|Field|Description|
|-----|-----------|
|Slow query|The slow query for which the index suggestion was generated.|
|Example|An actual SQL statement for an individual query, before being canonicalized to aggregate it with similar queries.|
|Table name|Name of the table used in the query.|
|Column names|Names of the columns used in the query.|
|Index name|Name of the index, assigned by the ISE after the index is created.|
|State|Processing state of the index. For details, refer to [Index suggestions for slow queries](../concept/index-suggestions.md) to see index suggestion states and table.|
|Imported|This box, if checked, indicates that the index suggestion was imported from a different instance for evaluation and testing.|

**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

