---
title: Export CAD configuration
description: Export the updated CAD changes to your CAD file. Exporting the updated changes creates a copy of the modified CAD file in Indoor Mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/indoor-mapping/export-cad-config.html
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
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

1.  Select the More options menu icon \(\[Omitted image "more-options-icon.png"\] Alt text: More options menu icon.\) and select **Export to autocad**.

    \[Omitted image "wsd-cad-editor-more-options-menu.png"\] Alt text: CAD configuration showing the more options menu.

2.  The export dialog box appears.

    \[Omitted image "wsd-export-changes-cad.png"\] Alt text: Export changes to CAD file.

3.  Select **Export**.

    The application may take some time to load the changes and complete the export process. The time to load depends on the size of the CAD file.

    **Note:** Updates made to the CAD file are only locally available in Indoor Mapping until you export the changes to your CAD file. Exporting the file keeps the CAD file up to date with changes made in Indoor Mapping.

4.  The **Download updated file** option is activated in the more options menu \(\[Omitted image "more-options-icon.png"\] Alt text: More options menu.\) after you’ve exported your CAD changes.

    Selecting this option downloads the updated CAD file.

5.  Navigate to Autocad sources \(**All** and in the context menu filter by `sn_map_core_autocad_source.LIST`.

    You can find the updated CAD file changes in this table.

    **Note:** The attributes that are added, modified, or deleted are updated in the Autocad source \(sn\_map\_core\_autocad\_source\) table. Exporting the changes doesn't apply the changes to your original CAD file. A new column is added to the Autocad source table to show the updated CAD file. Your original CAD file is kept intact. For example, your original CAD file name is **demo.dxf** and the updated CAD changes are exported to a new column **demo\_updated.dxf**.

6.  From the list of CAD source files, select and open the CAD file that you updated.

    The exported CAD changes are available as a new file in the **Updated file** column.

    \[Omitted image "wsd-autocad-source-updatedfile.png"\] Alt text: Autocad source for CAD file showing the exported and updated file.


**Parent Topic:**[Autocad import tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/autocad-ovw-v2.md)

**Previous topic:**[Closing a geometry or a polyline in a layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/editing-a-shape-autocadv2.md)

**Next topic:**[Import CAD configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/import-cad-config.md)

