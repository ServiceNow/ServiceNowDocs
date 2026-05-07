---
title: Test read-only options
description: Test read-only behavior on a non-production instance before updating Read only option field values on your production instance.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Read-only options, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Test read-only options

Test read-only behavior on a non-production instance before updating **Read only option** field values on your production instance.

## Before you begin

Role required: admin

## About this task

Read-only fields created prior to the Australia release are automatically set to **Instance Configured** after upgrading to at least Australia. You can use the **Instance Configured** option to test the read-only options introduced in the Australia release in a non-production instance before making changes in your production instance.

When a field's **Read only option** is set to Instance Configured, read-only behavior is derived from the **glide.read\_only.legacy\_read\_only\_behavior** system property. By default, the property is set to client\_script\_modifiable, which honors the pre Australia read-only behavior, allowing changes to read-only fields through client scripts.

**Important:** The **glide.read\_only.legacy\_read\_only\_behavior** system property is only intended for testing read-only behavior on non-production instances. Updating this property affects all fields where the **Read only option** field is set to Instance Configured.

## Procedure

1.  Navigate to the System Properties \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search for a system property record with name **glide.read\_only.legacy\_read\_only\_behavior**.

3.  Select the **glide.read\_only.legacy\_read\_only\_behavior** system property.

4.  In the Value field, enter the read only option that you want to test.

    The option that you enter determines how strict the system treats the security of read-only values once they've been entered. Each option displays the field as read-only in the UI.

<table id="choicetable_ic3_bwk_tgc"><thead><tr><th align="left" id="d315619e139">

Option

</th><th align="left" id="d315619e142">

Description

</th></tr></thead><tbody><tr><td id="d315619e148">

**`display_read_only`**

</td><td>

Allows changes to the read-only field through client scripts and server-side operations such as **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

</td></tr><tr><td id="d315619e170">

**`client_script_modifiable`**

</td><td>

Allows changes to the read-only field through client scripts but not through background scripts or server-side APIs like **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

</td></tr><tr><td id="d315619e192">

**`strict_read_only`**

</td><td>

Prevents any changes from both client scripts and server-side APIs.

</td></tr></tbody>
</table>5.  Select **Update**.


## What to do next

Test any client scripts or server-side APIs that update read-only fields work as expected in your non-production environment. After testing the functionality, you can update individual fields in your production instance and set the **Read only option** field to the option that you verified in your non-production instance.

**Parent Topic:**[Configuring read-only security options](../concept/read-only-option.md)

