---
title: Create an export set
description: Create an export set to export records from your instance to a file on a MID Server.
locale: en-US
release: xanadu
product: System Export Sets
classification: system-export-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Export sets, Exports, Creating integrations with applications]
---

# Create an export set

Create an export set to export records from your instance to a file on a MID Server.

## Before you begin

Role required: export\_set\_admin

## About this task

**Note:** Export sets do not export attachments to records. To download an attachment, either use the REST Attachment API \(HTTP request originates from a third-party HTTP client\), or use the outbound REST Message module to send the attachment from the instance \(HTTP request originates from the instance\).

## Procedure

1.  Navigate to **All** &gt; **System Export Sets** &gt; **Create Export Set**.

2.  Enter a descriptive **Name** for the export set.

3.  In the **What to export** section, define what data to export in one of these ways.

<table id="choicetable_hdz_2mk_vs"><tbody><tr><td id="d145007e95">

**Select __Yes__ and select an __Export Definition__ record.**

</td><td>

Use this configuration if you have already created an export definition record specifying what data to export.

</td></tr><tr><td id="d145007e110">

**Select __No__ and select a table to export data from.**

</td><td>

Use this configuration if you have not created an export definition record. A new export definition record is created automatically using the selected table that includes fields from the default list view for that table. You can modify the export definition record as needed after creating the export set.

</td></tr></tbody>
</table>4.  In the **Where to export to** section, define where you want to export data to in one of these ways.

<table id="choicetable_thz_tzk_vs"><tbody><tr><td id="d145007e134">

**Select __Yes__ and select an __Export Target__ record.**

</td><td>

Use this configuration if you have already created an export target record specifying where to export data to.

</td></tr><tr><td id="d145007e149">

**Select __No__ and select a MID Server, and specify a path on the MID Server to save the exported data to.**

</td><td>

Use this configuration if you have not created an export target record. A new export target record is created automatically for the selected MID Server and file path. You can modify the export target record as needed after creating the export set.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

After creating the export set, the Export Set form appears. You can configure advanced options from the form such as specifying a data format or scheduling recurring exports.

|Field|Description|
|-----|-----------|
|Name|Enter a descriptive name for this export set.|
|File name|Enter a name for the target file.|
|Format|Select the format of the target file, such as CSV.|
|Append timestamp|Select this check box to append the current date and time to the name of the exported file.|
|Export definition|Select the export definition that specifies the data to export.|
|Export target|Select the export target that specifies the location you want to export to.|

