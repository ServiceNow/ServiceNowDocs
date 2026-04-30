---
title: Manage enhanced sync operations
description: Review pending sync operations and decide whether to process or ignore the operation.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using enhanced synchronization, Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Manage enhanced sync operations

Review pending sync operations and decide whether to process or ignore the operation.

## Before you begin

Role required: sn\_wsd\_indoor\_map.admin or sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Operations**.

2.  Filter the list to include the records that you want to process.

    Only the records that are included in the filter are processed. For more information about filtering lists, see [Create a filter in List](https://www.servicenow.com/docs/access?context=t_CreatingFilters&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    Review the pending operations, which include Workplace Space retirements or Indoor Mapping Place deactivations.

3.  Edit the operation based on your requirement.

    Records that have the operation set to **Ignore** aren’t processed.

4.  Select **Process Pending**.

    **Important:** Only the records that are included in the filter are processed.


## Result

Pending records that are set to Retire or Deactivate are processed and are synchronized with Indoor Mapping or Workplace Core.

If some records aren’t processed, you can review the error logs. You can view the sync error logs by navigating to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Error Logs**.

.

**Parent Topic:**[Using enhanced synchronization](../concept/using-enhanced-sync.md)

