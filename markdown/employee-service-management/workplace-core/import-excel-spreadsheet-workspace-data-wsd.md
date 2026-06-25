---
title: Import your workspaces data from an Excel spreadsheet
description: Import your workspaces data from an Excel spreadsheet into the Workplace Core application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/import-excel-spreadsheet-workspace-data-wsd.html
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Import your workspaces data from an Excel spreadsheet

Import your workspaces data from an Excel spreadsheet into the Workplace Core application.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Complete [Configuring spreadsheets to import workplace data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/importing-workspace-data-wsd.md).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Existing table**.

3.  In the **Import set table** field, select **Space Staging \[sn\_wsd\_core\_space\_staging\]**.

4.  In the **Source of the import** field, select **File**.

5.  Select **Choose File** and select the source Excel spreadsheet.

6.  Specify the worksheet number in the **Sheet number** field and header row number in the **Header row** field.

7.  Select **Submit**.

    The imported data is now available in the new Import Set table.

8.  Select **Run Transform**.

    **Important:** Ensure that the Import set field shows sn\_wsd\_core\_space\_staging and the selected map is Space Transform map - sn\_wsd\_core\_space.

9.  Select **Transform**.

10. Verify that the data records were imported into the Spaces table by navigating to **Workplace Safety Management** &gt; **Space Administration** &gt; **Spaces**


## What to do next

[Define shifts for your workplace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/create-shifts-wsd.md)

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Add a space type configuration]()

[Configure a workplace card]()

[Block a workplace location]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Create a workplace performer criteria]()

[Mapping employees to their designated workspaces]()

[Assign the workplace user role to employees]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[Location migration]()

[View workplace service usage analytics with Usage Insights]()

[Run an import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/t_RunImport.md)

[Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/t_CreateATransformMap.md)

