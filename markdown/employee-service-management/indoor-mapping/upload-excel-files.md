---
title: Upload Excel files
description: Import geographical data by uploading Excel files containing information about your campuses, buildings, and floors.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Bulk hierarchy upload, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Upload Excel files

Import geographical data by uploading Excel files containing information about your campuses, buildings, and floors.

## Before you begin

Make sure that you have downloaded and filled the Excel templates from the Map Studio. For more information, see [Download and fill Excel templates for bulk upload](download-bulk-template.md).

**Important:** You must import the files in the following order: **Campus** &gt; **Building** &gt; **Floor**.

Role required: sn\_map\_core.admin

## About this task

The Upload Excel files feature uses Import Sets to import the information from the Excel files. For more information about Import Sets, see the following resources:

-   [Import sets documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/import-sets-landing-page.md)
-   [Import Data ServiceNow® developer course](https://developer.servicenow.com/dev.do#!/learn/courses/zurich/app_store_learnv2_importingdata_zurich_importing_data_into_servicenow)

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  On the **Bulk hierarchy upload** card, select **Upload hierarchy**.

3.  In the Upload Excel Files section, select **Upload hierarchy data**.

4.  On the Load Data form, fill in the fields; make sure that you import the campus file first.

    For a description of the field values, see [Load data form](../../talent-acquisition/reference/import-set-table.md).

    **Note:** You can select a file from your instance by selecting **Data source** as the source of the import.

5.  Select **Submit**.

    After the Excel file is processed, the system displays information or errors related to the import. You can fix the errors and reupload the file.

6.  From the **Next steps** section, select **Run Transform**.

7.  Select a map from the Available maps column, then select **Add**.

8.  After selecting the transform maps that you want to run, select **Transform**.

    The transform maps run in the order that they’re selected. After running the transform, you can view the import set for the loaded data.


## What to do next

You can repeat the procedure to import the Excel files for your buildings, and then your floors. After all the files are imported, you can upload the floor plans. For more information about uploading floor plans in bulk, see [Upload CAD files](upload-cad-files.md).

Campuses and buildings are created based on precise geographical coordinates. You can preview your campus on the Map Studio after importing the files. For more information about viewing the map, see [Map preview](map-preview-indoor-mapping.md).

