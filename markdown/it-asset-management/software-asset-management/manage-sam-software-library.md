---
title: Manage Software Library
description: Use the Manage Software Library module to manually upload software library data to on-premise instances \(instances not in the cloud to receive automatic Software Library updates\). You can also choose to export your normalization content for participation in the Software Asset Management content service.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Manage Software Library

Use the Manage Software Library module to manually upload software library data to on-premise instances \(instances not in the cloud to receive automatic Software Library updates\). You can also choose to export your normalization content for participation in the Software Asset Management content service.

## Before you begin

Role required: admin \(to enable module\), sam\_admin \(to manage software library\)

Activate the Manage Software Library module to manage Software Library content imports or exports by navigating to **System Definition** &gt; **Modules**. Ensure that the **Active** column in the Manage Software Library  module is set to true.

## About this task

The Manage Software Library module must be activated using the System Definition module for it to be shown in the Software Asset Management administration navigation.

Software Library content data is provided in a zip file. The zip file contains files with consistent file sizes for improved performance. During import, data tables are successfully updated with content from the XML file during a background process.

A worker is an object that performs some work in one or more background threads. To import multiple XML files simultaneously, workers are used. To change the number of workers that run simultaneously, update the following two system properties with the number of workers being used:

-   glide.sys.schedulers
-   com.snc.samp.recon.max\_workers

To upload an attachment larger than 1 GB, you need to update the **com.glide.attachment.max\_size** system property to reflect the size of the content zip file.

You can also export your data for participation in the [Software Asset Management content service](../concept/c_SAMContentService.md) to contribute to the improvement of the normalization service.

## Procedure

1.  Navigate to **Software Asset** &gt; **Administration** &gt; **Manage Software Library**.

2.  To import the Software Library content file:

    1.  Select **Import Software Library Content File**.

    2.  Select **Attach Content File** to choose the Software Library content \(.zip\) file.

    3.  Select **Run Import**.

        In the Import Files related list, track the progress of the import by seeing how many files have been processed and how many are still being processed. All the data in the Import Files related list is stored in the SAMP Import File \[samp\_import\_file\] table. For a more high level view of the import process, you can also view the Asset Job Logs \[asset\_job\_log\] table.

3.  To export your normalization content:

    1.  Select **Content Service Opt-In: Export Normalization Content**.

    2.  Select **Run Export**.

    3.  When the export status is **Ready for Download**, select **Refresh**.

    4.  Select the attachment to open or save.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

