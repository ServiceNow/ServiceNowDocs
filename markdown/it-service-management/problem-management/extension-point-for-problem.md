---
title: Extension point for Problem Management
description: Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add multiple incidents to a problem, Managing Problems, Problem Management, IT Service Management]
---

# Extension point for Problem Management

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code.

global.MRABulkAddRecordsFilter is a generic extension point that you can use to attach associated records. You can add its implementation to use a multi-record associator for attaching the records.

Navigate to **All** &gt; **Scripted Extension Points** to add global.MRABulkAddRecordsFilter to the \[sys\_extension\_point\] table.

**Note:** If you've already created implementations using the old extension point global.BulkAddIncidentsFilter in previous releases, you can still use that extension point for your existing customized implementations. But in the future, the global.BulkAddIncidentsFilter extension point will be deprecated. You’re encouraged to migrate your implementation to the global.MRABulkAddRecordsFilter the extension point. If you're creating implementations, use the extension point global.MRABulkAddRecordsFilter for adding one or multiple incident records to a problem.

**Parent Topic:**[Add multiple incidents to a problem](../task/add-multiple-incidents-to-problem.md)

