---
title: Configure attachment system properties
description: You can disable the drag-and-drop feature. \(Users can still upload attachments by browsing to the file.\) You can also limit the attachment file size, restrict who can upload attachments, and restrict what file extensions can be uploaded.You can specify the maximum size allowable for attachments to avoid issues with the user's active session on the instance. The maximum attachment size for email attachments is configured separately.You can restrict who can upload attachments.The glide.attachment.extensions property restricts the file extensions that users can upload as attachments.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Administering attachments, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure attachment system properties

You can disable the drag-and-drop feature. \(Users can still upload attachments by browsing to the file.\) You can also limit the attachment file size, restrict who can upload attachments, and restrict what file extensions can be uploaded.

## Before you begin

Role required: admin

**Note:** To learn more about the properties that affect attachments processing, see Attachments \(instance security hardening\) in Instance Security Hardening Settings.

## Procedure

1.  To disable the drag-and-drop features, navigate to **System Properties** &gt; **UI Properties**.

2.  Clear the check box for the **Allow attachment drag and drop in supported HTML5 browsers** property.

3.  Click **Save**.


**Parent Topic:**[Administering attachments](../reference/r_AdministeringAttachments.md)

## Limit attachment file size

You can specify the maximum size allowable for attachments to avoid issues with the user's active session on the instance. The maximum attachment size for email attachments is configured separately.

### Before you begin

Role required: Admin.

### About this task

**Note:** The maximum attachment size for email attachments is configured separately.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Security**.

2.  Enter a value in the **Maximum file attachment size in megabytes** property.

    The system only allows attachment sizes up to 1 GB. By default, this field is blank. If you leave this field blank, the system uses the default maximum limit of 1 GB.

3.  Click **Save**.


## Require a role to attach files

You can restrict who can upload attachments.

### Before you begin

Role required: Admin.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Security**.

2.  In the **Attachment limits and behavior** section, locate the **List of roles \(comma-separated\) that can create attachments** property \(**glide.attachment.role**\).

3.  Enter one or more roles separated by commas.

    Only roles listed in this property are able to upload attachments to a record. If no roles are entered, then all roles can upload attachments.

4.  Click **Save**.


## Restrict attachment file extensions

The **glide.attachment.extensions** property restricts the file extensions that users can upload as attachments.

### Before you begin

Role required: Admin.

### About this task

Restrict attachment file extensions to prevent users from uploading invalid file types and file types that may be more likely than others to contain viruses or malware.

**Note:** This property does not restrict attachments based on the actual file type, only based on the extension. To enable MIME type validation, which validates that the MIME type of a file matches the file extension and can block attachments that do not pass this validation, see .

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Security**.

2.  In the **Attachment limits and behavior** section, locate the **List of file extensions \(comma-separated\) that can be attached to documents via the attachment dialog** property.

3.  Enter the file extensions and click **Save**.

    If no extensions are specified, then all extensions are allowed. However, if any extensions are specified, all unlisted extensions are restricted. Listed extensions should not include the dot \(.\) prefix or spaces after commas. For example, enter `xls,xlsx,doc,docx`.


