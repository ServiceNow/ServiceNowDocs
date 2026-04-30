---
title: Configure attachment icons
description: Configure the icon that appears beside an attachment of a particular file type.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering attachments, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure attachment icons

Configure the icon that appears beside an attachment of a particular file type.

## Before you begin

Role required: admin

## Procedure

1.  Determine the path of the image file or upload a new image.

2.  Navigate to **System UI** &gt; **Attachment Icon Rules**.

3.  Open an existing rule or click **New** to create a new rule.

4.  Enter the rule details.

<table id="choicetable_py2_kyw_t1b"><thead><tr><th align="left" id="d61066e126">

Field

</th><th align="left" id="d61066e129">

Description

</th></tr></thead><tbody><tr><td id="d61066e135">

**Select icon by**

</td><td>

Select **MIME Type** or **File Extension**.**Note:** If a file type has an icon specified by **MIME Type** and a different icon specified by **File Extension**, the **MIME Type** icon takes precedence.

</td></tr><tr><td id="d61066e162">

**MIME type**

</td><td>

If **Select icon by** is **MIME Type**, enter the MIME type and subtype to associate with the icon, separated by a slash \(example: `application/pdf`\).

</td></tr><tr><td id="d61066e180">

**File extension**

</td><td>

If **Select icon by** is **FIle Extension**, enter the file extension to associate with the icon beginning with the period \(example: `.pdf`\).

</td></tr><tr><td id="d61066e198">

**Icon**

</td><td>

Enter the path to the icon image file \(example: `images/icons/attach_pdf.gifx`\)

</td></tr></tbody>
</table>5.  Click **Submit** or **Update**.


**Parent Topic:**[Administering attachments](../reference/r_AdministeringAttachments.md)

