---
title: Make a field read only
description: Control whether a field is read only and whether it can be changed by a client script and server-side APIs.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Read-only options, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Make a field read only

Control whether a field is read only and whether it can be changed by a client script and server-side APIs.

## Before you begin

Role required: admin

## About this task

You can customize the behavior of a read-only field, including whether a client script or server-side API can modify the read-only field value. You control the read-only behavior by updating the **Read only option** field in a dictionary record.

For details on read only options, see [Configuring read-only security options](../concept/read-only-option.md).

## Procedure

1.  Navigate to the field's dictionary entry in one of the following ways.

    -   Navigate to a field on a form, right-click the field, and select **Configure Dictionary** or **Show &lt;field name&gt;**.
    -   Navigate to **System Definition** &gt; **Dictionary**, and click an entry for a field or table.
2.  Make the field read only by selecting an option in the **Read only option** field.

    The option that you select determines how strict the system treats the security of read-only values once they've been entered. Each option displays the field as read-only in the UI.

<table id="choicetable_ic3_bwk_tgc"><thead><tr><th align="left" id="d120408e109">

Option

</th><th align="left" id="d120408e112">

Description

</th></tr></thead><tbody><tr><td id="d120408e118">

**__Display Read Only__**

</td><td>

Allows changes to the read-only field through client scripts and server-side operations such as **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

</td></tr><tr><td id="d120408e140">

**__Client Script Modifiable__**

</td><td>

Allows changes to the read-only field through client scripts but not through background scripts or server-side APIs like **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

</td></tr><tr><td id="d120408e162">

**__Strict Read Only__**

</td><td>

Prevents any changes to the read-only field from both client scripts and server-side APIs.

</td></tr></tbody>
</table>3.  Select **Update**.


**Parent Topic:**[Configuring read-only security options](../concept/read-only-option.md)

