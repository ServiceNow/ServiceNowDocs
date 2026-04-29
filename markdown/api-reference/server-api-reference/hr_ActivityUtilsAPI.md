---
title: hr\_ActivityUtils - Scoped
description: The hrActivityUtils script include enables you to create HR cases from a record producer.Creates a case from a record producer and service. This method is intended to be called as-is to create a producer and does not require supplying data.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# hr\_ActivityUtils- Scoped

The hrActivityUtils script include enables you to create HR cases from a record producer.

This script include requires the HR Lifecycle Events plugin \(com.sn\_hr\_lifecycle\_events\) and runs in the `sn_hr_le` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## hr\_ActivityUtils - createCaseFromProducer\(GlideRecord current, Object producer, String cat\_item.sys\_id\)

Creates a case from a record producer and service. This method is intended to be called as-is to create a producer and does not require supplying data.

The following variables can be configured in a record producer to provide additional capabilities as follows:

-   `job` – References sn\_hr\_core\_job and maps to subject\_person\_job in an HR case
-   `opened_for` – References sys\_user and maps opened\_for in an HR case
-   `concurrent_job` – If the record producer includes this variable \(by activating checkbox\) and parameters have job information, creates a new job in sn\_hr\_core\_job table

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|GlideRecord for case to be created.|
|producer|Object|Comma-separated key value pair containing data as questions and answers that are automatically provided when a user submits an answer to a record producer question.|
|cat\_item.sys\_id|String|Looks up the HR service of case being created and variable names to populate the description.|

|Type|Description|
|----|-----------|
|Object|New case in related table, varies by product.|

This method is intended to be called as-is to create a producer and does not require supplying data.

```
new sn_hr_core.hr_ActivityUtils(current).createCaseFromProducer(producer, cat_item.sys_id);
```

