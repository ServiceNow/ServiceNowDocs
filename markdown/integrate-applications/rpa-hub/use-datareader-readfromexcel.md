---
title: Use the ReadFromExcel component
description: Extract data from a Microsoft Excel file as a DataTable by using the ReadFromExcel component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Reader, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ReadFromExcel component

Extract data from a Microsoft Excel file as a DataTable by using the ReadFromExcel component in RPA Desktop Design Studio.

## Before you begin

To use the ReadFromExcel component, install [Microsoft Access Database Engine](https://www.microsoft.com/en-us/download/details.aspx?id=54920).

Role required: none

## About this task

You can configure the properties for the ReadFromExcel component. For more information about these properties, see [Properties of the Data Reader components](../reference/util-datareader-prop.md).

-   **Real-world scenario: Importing employee records**

    An HR department maintains employee details in an Excel file. The ReadFromExcel component extracts this data into a DataTable, which is then used to update an HR management system.


## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Reader**.

2.  Drag the ReadFromExcel component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ReadFromExcel component to the corresponding ports of the other components as described in the following table.

    |Parameter|Description|Data Port type|Data type|
    |---------|-----------|--------------|---------|
    |Filepath|Path to the Excel file that you can pass from the previously executed component.|Data In|String|
    |Sheetname|Name of the sheet in the Excel file that you can pass from a previously executed component.|Data In|String|
    |IsFirstRowHeader|Specifies true or false value that indicates the first row of the Excel sheet is a header or not.|Data In|Boolean|
    |Count|Returns the total number of rows containing data.|Data Out|Integer|
    |Data|Returns the extracted data from the Excel file in a DataTable.|Data Out|DataTable|

5.  To preview the data, right-click the **Return** field and click **Preview Data**.

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Reader](../concept/datareader-utility.md)

