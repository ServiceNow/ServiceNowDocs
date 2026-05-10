---
title: Add and manage attachments
description: You can upload a file as an attachment to an incident, a knowledge article, a change request, or to another type of record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add and manage attachments

You can upload a file as an attachment to an incident, a knowledge article, a change request, or to another type of record.

## Before you begin

Role required: admin

## About this task

Administrators can configure attachments and how they work in the system. For more information, see [Administering attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AdministeringAttachments.md).

The default maximum size limit for an attachment file that can be added to a record on the ServiceNow AI Platform is 1024MB for a new out-of-box instance. If the field is left blank the default limit \(currently set at 1GB\) will be used as the maximum attachment file size.

**Note:** Do not use the **Upload File** module in the **System Definition** application. It is not compatible with multi-node instances.

## Procedure

1.  Navigate to the record.

    For example, an incident record.

2.  Click the attachments icon \(![Attachments icon](../image/UI14FormAttachments.png)\).

3.  Click **Choose Files** or **Browse**, depending on your browser, and navigate to a file.

4.  Upload multiple files in one of the following ways.

    -   Select multiple files at the same time in the file browser. Internet Explorer does not support this feature.
    -   Add each file on a separate line by clicking **Add Another Attachment**, and then clicking **Choose Files** on the next line. Repeat until all desired files are selected. This feature is available in all supported browsers.
5.  Click **Attach**.

    Attached files appear in the **Current file attachments** list and at the top of the form. There are several common error messages that a user might receive in certain cases when attempting to upload an attachment to a record on a ServiceNow instance. Common examples of these errors are as follows.

    -   When attempting to add an attachment to a specific record, the user may receive an error that the file contains a prohibited file extension.
    -   When attempting to upload an attachment to a record the user receives a message a file type is not permitted or MIME type not matching with the actual file name.
    -   When attempting to add an attachment to a record on an instance, the user receives a file size error.
6.  To correct these errors, navigate to **System Properties** **&gt; Security**.

    1.  For a disallowed file type error, attempt to save the file in a different format.

        The .zip file extension is often included as an allowed file extension and a file can be compressed and then attached.

    2.  For a file type not permitted or mime type error, locate **This property must be set to activate MIME type checking for uploads \(All version Eureka and up\). Enables \(true\) or disables \(false\) mime type validation for file attachments. File extensions configured via glide.attachment.extensions will be checked for MIME type during upload.** and activate the property by checking **Yes**.

        **Note:** The default setting for this property on an out-of-box instance is No \(unchecked\).

    3.  For a file size error, see [Manage attachments](t_ManagingAttachments.md).

7.  Close the pop-up window to return to the form.


## What to do next

Limit the users who can view attachments by applying ACL rules. For more information on ACL rules, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).

-   **[Manage attachments](t_ManagingAttachments.md)**  
View, rename, and remove the attachments on a record and adjust the maximum allowable size of attachments.
-   **[Attach files with drag-and-drop](t_AttachingFilesWithDragAndDrop.md)**  
You can drag files from your local computer into your browser window to attach them to the current record.

**Parent Topic:**[Forms in the classic environment](../concept/c_UsingForms.md)

