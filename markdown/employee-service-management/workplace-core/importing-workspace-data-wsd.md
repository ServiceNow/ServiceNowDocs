---
title: Configuring spreadsheets to import workplace data
description: Import work location data in bulk through spreadsheets into the Workplace Core application to avoid manually entering redundant data for each workplace, which saves time and effort.Customize the information in your organization's existing workspace spreadsheet to avoid having to manually enter repeated information for each workspace. You can then import the data into your ServiceNow instance.Create a Microsoft Excel spreadsheet from the data you entered into the Workplace Core so you can avoid having to manually enter global information such as the site or building names for each workspace. You can then import the data into your ServiceNow instance.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Workplace Core, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configuring spreadsheets to import workplace data

Import work location data in bulk through spreadsheets into the Workplace Core application to avoid manually entering redundant data for each workplace, which saves time and effort.

By using a spreadsheet that contains the global information for your work sites, you can enter only the distinguishing space information instead of having to manually repeat information such as the region, site, building, and floor. You can either create an Excel spreadsheet from the data you've entered into the Workplace Core application or modify an existing workplaces spreadsheet.

**Parent Topic:**[Configure Workplace Core](configure-wsd.md)

**Related topics**  


[Install Workplace Core](../task/install-workplace-service-delivery.md)

[Providing your workplace data](providing-your-workplace-data-wsd.md)

[Activate Virtual Agent for Workplace Service Delivery](../task/actuvate-va-for-wsd.md)

## Configure an existing workspaces spreadsheet

Customize the information in your organization's existing workspace spreadsheet to avoid having to manually enter repeated information for each workspace. You can then import the data into your ServiceNow instance.

### Before you begin

Role required: sn\_wsd\_core.admin

### About this task

If you have a spreadsheet containing your organization's workspaces data, you need to customize it to match the record information in your ServiceNow instance.

This example describes how to modify the floor information for your workspace data. Repeat these instructions to replace the fields for your building, campus, site, and region, as appropriate.

### Procedure

1.  Modify the data in the spreadsheet to match the record information in your ServiceNow instance.

    1.  Navigate to **Workplace Safety Management** &gt; **Space Administration** &gt; **Floors**.

    2.  Search for the desired floor record and open it.

    3.  Copy the value of the **Number** field.

    4.  Paste the value in place of "Floor 1" in the Excel spreadsheet.

        The example uses the following sample entry for workspaces that belong to Floor 1 of Building 1 at Florida Campus 2, Florida, USA:

        -   FLOR0001694 represents Floor 1
        -   BLDG0001028 represents Building 1
        -   CMPS0001013 represents Florida Campus 2
        -   SITE0001007 represents Florida
        -   RGIN0001002 represents USA
        **Note:** You can exclude the **Area** column as it is not mandatory. Enter a dummy value in the column instead of leaving it empty.

        ![Import workspace data](../../../reuse/workplace-safety-mgmt/images/import-workspace-data.gif)

2.  In your workspaces spreadsheet, add individual workspace information in the **Name** column.

3.  Save your spreadsheet.


## Create a workplace data spreadsheet

Create a Microsoft Excel spreadsheet from the data you entered into the Workplace Core so you can avoid having to manually enter global information such as the site or building names for each workspace. You can then import the data into your ServiceNow instance.

### Before you begin

Role required: sn\_wsd\_core.admin

### About this task

If you have a large number of work sites, consider creating a spreadsheet that you can then import into your ServiceNow instance to avoid having to manually enter global information such as the site or building names for each workspace.

**Note:** If you already have an existing workspaces spreadsheet for your organization, follow the instructions in [Configure an existing workspaces spreadsheet](importing-workspace-data-wsd.md#) to customize it for exporting the data.

### Procedure

1.  Navigate to **All** &gt; **Workplace Safety Management** &gt; **Space Administration**.

2.  Select the module for the smallest unit for which you want to repeat the data.

    For example, if you have created global information records of regions, sites, buildings, and floors, you would select **Floors**.

3.  Customize the columns to be displayed.

    For example, you can choose to hide the **Campus** column if your organization does not have campuses by entering a dummy value instead of leaving it empty.

4.  Export the data by holding and selecting \(or right-clicking\) on any column, selecting **Export**, and selecting **Excel \(.xlsx\)**.

    Data is exported from the application so that you can download it as an Excel file.

5.  Select **Download**.

6.  In your workspaces spreadsheet, add individual workspace information in the **Name** column.

7.  Save your spreadsheet.


### What to do next

[Import your workspaces data from an Excel spreadsheet](../task/import-excel-spreadsheet-workspace-data-wsd.md)

