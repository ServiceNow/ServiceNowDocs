---
title: Export CAD configuration
description: Export the updated CAD changes to your CAD file. Exporting the updated changes creates a copy of the modified CAD file in Indoor Mapping.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Autocad import tool, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Export CAD configuration

Export the updated CAD changes to your CAD file. Exporting the updated changes creates a copy of the modified CAD file in Indoor Mapping.

## About this task

Make configuration changes to your CAD source file using the CAD Editor and Map Configuration tabs. CAD configuration changes are updated in the Autocad Source \(sn\_map\_core\_autocad\_source\) table.

**Note:** Exporting the CAD configuration changes is an optional step. The updated CAD configuration changes reside in Indoor Mapping as an updated CAD file \(a copy\).

## Before you begin

Role required: admin

## Procedure

1.  Select the More options menu icon \(![More options menu icon.](../../wsd-for-mobile/images/more-options-icon.png)\) and select **Export to autocad**.

    ![CAD configuration showing the more options menu.](../images/wsd-cad-editor-more-options-menu.png)

2.  The export dialog box appears.

    ![Export changes to CAD file.](../images/wsd-export-changes-cad.png)

3.  Select **Export**.

    The application may take some time to load the changes and complete the export process. The time to load depends on the size of the CAD file.

    **Note:** Updates made to the CAD file are only locally available in Indoor Mapping until you export the changes to your CAD file. Exporting the file keeps the CAD file up to date with changes made in Indoor Mapping.

4.  The **Download updated file** option is activated in the more options menu \(![More options menu.](../../wsd-for-mobile/images/more-options-icon.png)\) after you’ve exported your CAD changes.

    Selecting this option downloads the updated CAD file.

5.  Navigate to Autocad sources \(**All** and in the context menu filter by `sn_map_core_autocad_source.LIST`.

    You can find the updated CAD file changes in this table.

    **Note:** The attributes that are added, modified, or deleted are updated in the Autocad source \(sn\_map\_core\_autocad\_source\) table. Exporting the changes doesn't apply the changes to your original CAD file. A new column is added to the Autocad source table to show the updated CAD file. Your original CAD file is kept intact. For example, your original CAD file name is **demo.dxf** and the updated CAD changes are exported to a new column **demo\_updated.dxf**.

6.  From the list of CAD source files, select and open the CAD file that you updated.

    The exported CAD changes are available as a new file in the **Updated file** column.

    ![Autocad source for CAD file showing the exported and updated file.](../images/wsd-autocad-source-updatedfile.png)


**Parent Topic:**[Autocad import tool](../concept/autocad-ovw-v2.md)

**Previous topic:**[Closing a geometry or a polyline in a layer](editing-a-shape-autocadv2.md)

**Next topic:**[Import CAD configuration](import-cad-config.md)

