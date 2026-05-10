---
title: Domain separation and IDR
description: Instance Data Replication \(IDR\) functions at the data level, which means it does not explicitly support domain separation.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and IDR

Instance Data Replication \(IDR\) functions at the data level, which means it does not explicitly support domain separation.

For a typical use case, data moves from a producer instance to a consumer instance and back without regard to which domain the instance is in. You can use IDR to filter data, enabling you to segregate specific data between instances. If you must go beyond the IDR record-level filtering capability, you can use business rules to convert data from one domain to another. For more information, see [Before Query business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-before-query-business-rules.md).

**Parent Topic:**[Instance Data Replication reference](../concept/reference-instance-data-replication.md)

**Related topics**  


[Data privacy in Instance Data Replication](../concept/data-privacy-consumers-idr.md)

[Adapter descriptions for Instance Data Replication](adapter-descriptions.md)

[Excluded tables in Instance Data Replication](IDR-excluded-tables.md)

[Instance Data Replication system properties](instance-data-replication-properties.md)

[Instance Data Replication roles](instance-data-replication-roles.md#)

