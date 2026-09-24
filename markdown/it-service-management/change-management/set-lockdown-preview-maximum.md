---
title: Set the lockdown preview maximum
description: Change the maximum number of records that a change lockdown preview displays. This keeps the preview readable on instances with a large volume of change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/set-lockdown-preview-maximum.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [change lockdown, preview maximum, system property]
breadcrumb: [Change lockdown, Configure, Change Management, IT Service Management]
---

# Set the lockdown preview maximum

Change the maximum number of records that a change lockdown preview displays. This keeps the preview readable on instances with a large volume of change requests.

## Before you begin

Role required: sn\_change\_admin

## About this task

A lockdown with broad conditions can match more change requests than the preview dialog can display. The preview maximum controls how many records the dialog lists. The limit applies to the preview only. Every matched change request is placed on hold when the lockdown is enforced.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System Properties**.

2.  Search for `com.snc.change_management.lockdown.preview.max_changes`.

    The property is described as the maximum number of `change_request` records to display, belongs to the **Global** application, and is delivered with the value `1000`.

3.  In the **Value** field, enter the maximum number of records to display.

    To see every matched change request in the preview, enter a number that is at least as large as the number of matching records.

4.  Save the property.


## What to do next

Preview a lockdown again to confirm the number of records that the dialog now lists. For more information, see [Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md).

**Parent Topic:**[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

**Related topics**  


[Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md)

[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

