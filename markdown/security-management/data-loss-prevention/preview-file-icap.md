---
title: Preview evidence files for ICAP
description: Preview DLP incident evidence files in the DLP IR Analyst workspace.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [DLP Analyst workspace]
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Preview evidence files for ICAP

Preview DLP incident evidence files in the DLP IR Analyst workspace.

## Before you begin

-   Navigate to **All** &gt; **DLP Administration** &gt; **Advanced Settings**.
-   Make sure the **sn\_icap\_dlp.enable\_evidence\_file\_preview** property is already enabled.

**Important:** While using the Evidence files action in the DLP analyst workspace, the evidence files are temporarily stored in the ServiceNow database in an unencrypted format for the duration you have selected using **sn\_dlir.preview\_temp\_files\_cleanup\_interval** property from the **Advanced Settings** page. You can disable the **Evidence Files** preview feature if you don't want to store any data in the ServiceNow database. For more information, see [Configure advanced settings](../../data-loss-prevention/task/configure-advanced-settings-dlp.md).

Role required: sn\_dlir.analyst

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open a DLP incident record.

3.  Select the **Evidence Files** icon, which is available on the contextual menu.

    A tab opens which fetches all the evidence files. Once the download is finished, you can view all the evidence files in the **Evidence Files** tab.

4.  Select the **Evidence File** card which you want to preview.

    The preview feature is different for each file type.

5.  Preview pdf and office docs in the document viewer by selecting the **Expand** icon on the top right of the evidence file to open the pdf in full screen.

    Office Extensions for which the document viewer opens the evidence files include- doc, docx, ppt, pptx, xls, xlsx.

    1.  Locate the search bar and enter the keyword you’re looking for.

    2.  Use the zoom-in and zoom-out features to adjust the view for better readability.

    3.  Rotate the page clockwise or counterclockwise to view the content more clearly.

    These control options enhance your ability to understand the evidence file comprehensively. Only the pdf has control options in the header.

    ![Preview files.](../../data-loss-prevention/image/preview.png)

6.  Preview eml files.

    Select the attachments in the email and preview them.

    **Note:** If the selected evidence file exceeds the 5-MB limit, it can’t be previewed in the analyst workspace. You have to download the file to preview its content. This limit is only for .eml files.

    ![Preview eml files.](../../data-loss-prevention/image/preview-eml.png)

7.  Preview images in the DLP analyst workspace.

    Images only with the .bmp, .gif, .ico, .jpeg, .jpg, .png, .svg, and .webp extensions are supported.

    ![Preview eml files.](../../data-loss-prevention/image/preview-image.png)

8.  Preview text files in the text editor by selecting the **Expand** icon on the top right of the evidence file.

    ![Preview text files.](../../data-loss-prevention/image/preview-text.png)

    **Note:** Evidence Files apart from the office docs, eml files, text, and image extensions won’t be supported for preview. Binary files won’t be rendered and have to be downloaded to preview their content. The preview evidence file feature also works for archived incidents.


**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../concept/icap-dlp-integration.md)

