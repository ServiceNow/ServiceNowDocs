---
title: Create requester mapping
description: Create a requester mapping to extend the auto-import functionality to other tables.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import messages from Microsoft Teams to ServiceNow, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create requester mapping

Create a requester mapping to extend the auto-import functionality to other tables.

## Before you begin

Role required: admin

**Note:**

If there is no requestor mapping defined for a table, the interaction records will not be created. An error log is created for the admin to notify that the requestor mapping is not defined for a table.

A requestor-mapping record defines which field, in any given table, is the field representing the requestor of a ticket.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Chat Administration** &gt; **Requestor Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Table|Table to which the requestor mapping \(auto-import feature\) should be applicable.|
    |Requestor field|Field to select the requestor for a record.|
    |Inherit|Extend and apply the auto-import feature to the child tables.|
    |Active|Option to activate the requestor-mapping record.|

4.  Click **Submit**.


**Parent Topic:**[Configure Request-based chats to import messages from Microsoft Teams to ServiceNow](../concept/auto-import-messages.md)

