---
title: Run transform to update data
description: Running a transform exports information from your records into an .xls file. That data can be imported into the ServiceNow space management application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Run transform to update data

Running a transform exports information from your records into an .xls file. That data can be imported into the ServiceNow space management application.

## Before you begin

Role required: admin

## About this task

An example transform map is included with the demo data. Load the demo data on a pre-production instance, go to campuses, and select the **Westfield Valley Fair** campus. Open the Westfield**Valley Fair V262-259** map set. Use the **westfield\_transform\_example.xls** file as an example. Process the campus, then run the transform.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Run Transform**.

2.  Click **Create and load an import set first**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_ing_z2n_lt"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import set table

</td><td>

Selections are create table or existing table.

</td></tr><tr><td>

Label

</td><td>

Enter a label for the new table.**Note:** This field depends on the **Create table** option being selected.

</td></tr><tr><td>

Name

</td><td>

The name is automatically generated from the **Label** you enter. **Note:** This field depends on the **Create table** option being selected.

</td></tr><tr><td>

Import set table

</td><td>

All saved import set tables are listed in a list.**Note:** This field depends on the **Existing table** option being selected.

</td></tr><tr><td>

Source of the import

</td><td>

Selections are file or data source.

</td></tr><tr><td>

File

</td><td>

Browse to the location of the file.**Note:** This field depends on the **File** option being selected.

</td></tr><tr><td>

Sheet number

</td><td>

Identifies the sheet number used for the transform.**Note:** This field depends on the **File** option being selected.

</td></tr><tr><td>

Header row

</td><td>

Identifies the row number used as the header row in the transform file.**Note:** This field depends on the **File** option being selected.

</td></tr><tr><td>

Data source

</td><td>

All data sources are listed in a list.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Click **Run transform**.

6.  Click **Transform**.

    All the spaces are populated in space management from the space details in the transform map.

7.  Navigate to **Space Management** &gt; **Spaces**

8.  Review all space details to be certain all extra details were imported.


-   **[Transform map](../concept/c_TransformMap.md)**  
A transform map is an .xls file that allows you to add spaces or details about spaces from other sources into the space management application.

**Parent Topic:**[Space management](../reference/r_SpaceManagement.md)

