---
title: Add custom fields to the Express List preview panel
description: Add custom fields from the Alert \[em\_alert\] table to the Express List Info preview panel to track alert information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/preview-alert.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up your workspace, Express List in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# Add custom fields to the Express List preview panel

Add custom fields from the Alert \[em\_alert\] table to the Express List Info preview panel to track alert information.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **System Properties** &gt; **All Properties**.

2.  In the **System Properties** list, select **evt\_mgmt.express\_list.custom\_fields**.

    If a message appears about the application scope, select **here** to be able to edit the record.

3.  In the **Value** field, enter the custom name from the Alert \[em\_alert\] table.

    If you want to provide more than one field, use commas to separate the field names.

4.  Select **Update**.

5.  View the custom fields on the preview panel:

    1.  In the primary navigation, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon\).

    2.  Select a row or the information icon at the beginning of a row.


## Result

The Info tab on the preview panel displays the custom fields at the bottom of the fields list.

