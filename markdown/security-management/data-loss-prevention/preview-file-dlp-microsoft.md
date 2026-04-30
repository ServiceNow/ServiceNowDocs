---
title: Preview Evidence files for DLP incidents of type Exchange Online, OneDrive, and SharePoint
description: Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Preview Evidence Files, DLP analyst workspace, Data Loss Prevention Incident Response]
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Preview Evidence files for DLP incidents of type Exchange Online, OneDrive, and SharePoint

Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.

## Before you begin

**Important:** While using the Evidence files action in the DLP analyst workspace, the evidence files are temporarily stored in the ServiceNow database in an unencrypted format. If you don't want to store the evidence files, disable the Evidence Files preview feature. For more information, see [Configure advanced settings](../../data-loss-prevention/task/configure-advanced-settings-dlp.md).

Role required: sn\_dlir.analyst

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open a DLP incident record.

3.  From the contextual sidebar, select the Evidence files icon \(![Evidence files icon.](../../data-loss-prevention/image/icon-evidence-files.png)\).

4.  On the **Evidence Files** tab, select the **Evidence File** card to preview the evidence files in the document viewer.

    The preview feature is different for each file type, as listed in the following table.

<table id="table_bfs_kyj_k2c"><thead><tr><th>

File Format

</th><th>

File Extension

</th></tr></thead><tbody><tr><td>

Image

</td><td>

.bmp, .gif, .ico, .jpeg, .jpg, .png, .svg, and .webp.Image files open in the document viewer mode.

</td></tr><tr><td>

Microsoft Office files

</td><td>

.doc, .docx, .ppt, .pptx, .xls, and .xlsx Office files open in the document viewer mode.

</td></tr><tr><td>

Text files

</td><td>

.txtText files open in text editor mode.

</td></tr><tr><td>

Mail files

</td><td>

.eml**Note:** The file size must be less than 5MB. You must first download the file to preview its content.

</td></tr><tr><td>

PDF files

</td><td>

.pdf -   Enter a keyword to search the document.
-   Zoom-in and zoom-out features to adjust the view for better readability.
-   Rotate the page clockwise or counterclockwise to view the content more clearly.


</td></tr></tbody>
</table>    **Note:**

    Binary files won’t be rendered and have to be downloaded to preview their content. The preview evidence file feature also works for archived incidents.


**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

