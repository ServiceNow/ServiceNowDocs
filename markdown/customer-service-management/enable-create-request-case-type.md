---
title: Enable the Create Request UI action for case types
description: Enable the Create Request UI action for case type tables that extend the Case \[sn\_customerservice\_case\] table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up CSM integration with IT Service Management, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Enable the Create Request UI action for case types

Enable the **Create Request** UI action for case type tables that extend the Case \[sn\_customerservice\_case\] table.

## Before you begin

Role required: admin

## About this task

To enable the **Create Request** UI action for a case type table that extends the Case table, add an entry for the case type to the Request Parent Mapping \[request\_parent\_mapping\] table.

When an agent creates a request for a case in the case type table, the system adds the request to the Requests tab on the case record.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the Request Parent Mapping \[request\_parent\_mapping\] table.

3.  Select the Show List related link to open the list view for the table.

4.  Select **New** to create an entry for the case type table.

5.  Fill in the following fields in the Request Parent Mapping record.

    1.  Enter a name for the entry in the **Name** field.

    2.  Select the case type table in the **Parent table** field.

    3.  In the **Request parent** field, select Parent.

    4.  In the **Parent requestor** field, select Contact.

6.  Select **Submit**.


