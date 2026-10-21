---
title: Archive table names
description: Archive tables use the ar\_ prefix followed by the live table name.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/archive-table-names.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [archive table, table names, naming convention, ar\_ prefix]
breadcrumb: [Reference, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Archive table names

Archive tables use the ar\_ prefix followed by the live table name.

## Naming pattern

Archive tables follow a consistent naming pattern: the prefix `ar_` is prefixed to the live table name. For example, `incident` is set to `ar_incident`, and `problem` is set to `ar_problem`.

## Common archive tables

The following table shows common live tables and their archive counterparts.

|Live table|Archive table|
|----------|-------------|
|`incident`|`ar_incident`|
|`problem`|`ar_problem`|
|`change_request`|`ar_change_request`|
|`task`|`ar_task`|
|`sc_request`|`ar_sc_request`|
|`sc_req_item`|`ar_sc_req_item`|
|`sn_customerservice_case`|`ar_sn_customerservice_case`|

