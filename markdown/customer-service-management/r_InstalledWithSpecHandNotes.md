---
title: Components installed with Special Handling Notes
description: Several types of components are installed with Special Handling Notes.The tables included with the Special Handling Notes plugin \(com.sn\_shn\).Some user roles are included with the Special Handling Notes \(com.sn\_shn\) plugin.Some properties are included with the Special Handling Notes \(com.sn\_shn\) plugin.The business rules included with the Special Handling Notes plugin \(com.sn\_shn\).The client scripts included with the Special Handling Notes plugin \(com.sn\_shn\).The script includes included with the Special Handling Notes plugin \(com.sn\_shn\).
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Components installed with additional plugins for Customer Service Management, Reference, Customer Service Management]
---

# Components installed with Special Handling Notes

Several types of components are installed with Special Handling Notes.

## Tables installed with Special Handling Notes

The tables included with the Special Handling Notes plugin \(com.sn\_shn\).

The Special Handling Notes plugin adds the following tables.

<table id="table_dwc_swg_v5"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Special Handling Notes\[sn\_shn\_notes\]

</td><td>

Stores the special handling notes.

</td></tr><tr><td>

Special Handling Configuration \[sn\_shn\_configuration\]

</td><td>

Stores the special handling notes table configurations.

</td></tr></tbody>
</table>## Roles installed with Special Handling Notes

Some user roles are included with the Special Handling Notes \(com.sn\_shn\) plugin.

<table id="table_fbn_ypx_yt"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_shn.admin

</td><td>

Can read, create, update, and delete special handling notes. This role contains the sn\_shn.editor role.

 The sn\_customerservice\_manager role contains the sn\_shn.admin role.

</td></tr><tr><td>

sn\_shn.editor

</td><td>

Can read and update special handling notes. This role contains the sn\_shn.user role.

 The sn\_customerservice\_agent role contains the sn\_shn.editor role.

</td></tr><tr><td>

sn\_shn.user

</td><td>

Can read special handling notes.

</td></tr></tbody>
</table>## Properties installed with Special Handling Notes

Some properties are included with the Special Handling Notes \(com.sn\_shn\) plugin.

The Special Handling Notes plugin adds the following properties.

<table id="table_dx5_hxg_v5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of notes displayed in the Special Handling Notes pop-up window\[sn\_shn.max\_num\_alerts\]

</td><td>

-   **Type**: integer
-   **Default value**: 20
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

Display special handling notes only once per session\[sn\_shn.note\_preferences\]

</td><td>

Special handling notes are displayed each time you access a record. Enable this property to display special handling notes only once per session. -   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

Width of the Special Handling Notes pop-up window in pixels\[sn\_shn.popup\_width\]

</td><td>

The width of the Special Handling Notes pop-up window in pixels. The default width is 500. If you specify less that 300, the window automatically uses the minimum width of 300 pixels.-   **Type**: integer
-   **Default value**: 500
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr></tbody>
</table>To learn more about the special handling notes properties, see [Configure special handling notes properties](../task/t_EnableOnScreenAlertProperties.md).

## Business rules installed with Special Handling Notes

The business rules included with the Special Handling Notes plugin \(com.sn\_shn\).

The Special Handling Notes plugin adds the following business rules.

<table id="table_frl_1fh_v5"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Updating the table field

</td><td>

Special Handling Notes\[sn\_shn\_notes\]

</td><td>

Populates the **Table** field with the table label rather than the whole table name.

</td></tr><tr><td>

SHN Cache Table Entry

</td><td>

Special Handling Notes Configuration \[sn\_shn\_configuration\]

</td><td>

Stores the entries in the configuration table in a cache to avoid repeated queries.

</td></tr></tbody>
</table>## Client scripts installed with Special Handling Notes

The client scripts included with the Special Handling Notes plugin \(com.sn\_shn\).

The Special Handling Notes plugin adds the following client scripts.

<table id="table_d5d_5fh_v5"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

On Load Message

</td><td>

Special Handling Notes Configuration\[sn\_shn\_configuration\]

</td><td>

On Load Message describing what the Special Handling Notes Configuration table is for.

 Create a configuration by selecting a table for which special handling notes can be created and displayed. Include notes for related entities by selecting the desired fields and adding them to the configuration.

</td></tr></tbody>
</table>## Script includes installed with Special Handling Notes

The script includes included with the Special Handling Notes plugin \(com.sn\_shn\).

The Special Handling Notes plugin adds the following script includes.

|Script include|Description|
|--------------|-----------|
|SHNProcessor|A collection of APIs for special handling notes.|
|SHNTable|Provides a list of tables for which the user can create special handling notes.|

