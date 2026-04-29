---
title: Create a case digest table map
description: Create a table map to configure the fields that are copied from the case record to the post case review or the case action summary records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a case digest table map

Create a table map to configure the fields that are copied from the case record to the post case review or the case action summary records.

## Before you begin

Role required: admin

## About this task

Two table maps are included with the Case Digests plugin. The **PCR Map** uses the Case \(sn\_customerservice\_case\) table as the source table and the Post Case Review \(sn\_csm\_case\_digest\_pcr\) table as the target table. The **PCR Map** maps the following fields.

|Case field|Post Case Review field|
|----------|----------------------|
|sys\_id|Case number|
|Short description|Short description|
|Cause|Root Cause Analysis|
|Close notes|Solution provided|

The **CAS Map** uses the Case \(sn\_customerservice\_case\) table as the source table and the Case Action Summary \(sn\_csm\_case\_digest\_cas\) table as the target table. The **CAS Map** maps the following fields.

|Case field|Case Action Summary field|
|----------|-------------------------|
|sys\_id|Case number|
|Short description|Short description|

## Procedure

1.  To access the CSM Table Map list, navigate to **csm\_table\_map\_list.do**.

2.  Click **New** to create a new table map.

    You can also modify an existing table map by clicking the map name to open the map form.

3.  Fill in the following fields on the CSM Table Map form.

<table id="table_nbm_c24_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping name

</td><td>

The table map name.

</td></tr><tr><td>

Application

</td><td>

Read only. The application for this table map.

</td></tr><tr><td>

API Name

</td><td>

Read only. The API for this table map.

</td></tr><tr><td>

Advanced Field Mapping

</td><td>

Enables advanced field mapping.

</td></tr><tr><td>

Source Table

</td><td>

The source table for the map.

</td></tr><tr><td>

Target Table

</td><td>

The target table for the map.

</td></tr><tr><td>

Active

</td><td>

Enables the mapping from the source to the target tables.

</td></tr><tr><td>

Use Advanced Condition

</td><td>

Enables advanced condition mapping, which uses a script. If enabled, add a script in the **Advanced Condition** field.

</td></tr><tr><td>

Advanced Condition

</td><td>

The script to use if the **Use Advanced Condition** field is enabled.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions that apply to the table map.

</td></tr><tr><td>

Order

</td><td>

Order of priority for processing multiple matching map definitions simultaneously to resolve dependencies. -   If there is only one matching table map, the system uses that map.
-   If there are multiple matching table maps with the same order, the system uses the map with the older created date.
-   If there are multiple matching table maps with different orders, the system uses the map with the highest order.


</td></tr></tbody>
</table>4.  Click **Submit**.

5.  From the CSM Table Map list, select the table map created in step 2.

6.  In the Basic Field Mapping form section, click **New**.

7.  Select a **Source Field** and a **Target Field**.

8.  Enable the **Active** check box.

9.  Enter a number in the **Order** field

10. Click **Submit**.

11. Repeat steps 7 through10 for each field to be mapped.

12. Click **Update** on the CSM Table Map form.


