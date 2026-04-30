---
title: View attachments with Document Viewer
description: View documents within the platform using Document Viewer rather than having to download them to your own file system.
locale: en-US
release: yokohama
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Document Viewer, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View attachments with Document Viewer

View documents within the platform using Document Viewer rather than having to download them to your own file system.

## Before you begin

Make sure that Document Viewer is enabled for the table containing the record. For more information, see [Enable Document Viewer](../../../administer/form-administration/task/enable-document-viewer.md).

Role required: none

## About this task

Document Viewer supports inline viewing of certain [document types](../concept/Documentviewer.md#ul_jvx_dzy_whb) within the platform.

## Procedure

1.  Navigate to a record \(incident, form, list, and so on\) with an attachment.

2.  Click View next to the file attachment name.

    Document Viewer displays the document.

    If the document does not display, Document Viewer does not support inline viewing in your situation and a message instructs you to download the document. The possible reasons are:

    -   The document uploaded is platform encrypted or edge encrypted.
    -   The file size exceeds the maximum allowed value of 50 MB.
    -   The document is password-protected but it is not a PDF file.
    Click **Download Document** to view the document in the relevant external application.


**Related topics**  


[Enable Document Viewer](../../../administer/form-administration/task/enable-document-viewer.md)

