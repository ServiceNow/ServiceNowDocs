---
title: Use the ReadFromCSV component
description: Read data from a CSV file by using the ReadFromCSV component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Reader, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ReadFromCSV component

Read data from a CSV file by using the ReadFromCSV component in RPA Desktop Design Studio.

Watch this video to learn how to use the ReadFromCSV component.

How to use the ReadFromCSV component. 

## Before you begin

Role required: none

## About this task

You can configure the properties for the ReadFromCSV component. For more information about these properties, see [Properties of the Data Reader components](../reference/util-datareader-prop.md).

-   **Real-world scenario: Extracting product inventory data**

    An e-commerce company maintains stock details in a CSV file. The RPA bot uses the ReadFromCSV component to read the file and update inventory levels in the company’s database, ensuring real-time stock availability.


## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Reader**.

2.  Drag the ReadFromCSV component to the Design surface.

3.  To configure the input fields, see [Use the ReadFromCSV component](use-datareader-readfromcsv.md).

4.  Connect the data and control ports of the ReadFromCSV component to the corresponding ports of the other components as described in the following table.

    |Parameter|Description|Data Port type|Data type|
    |---------|-----------|--------------|---------|
    |FilePath|The file path of the CSV file.|Data In|String|
    |StartRow|The number of the row that will be first queried in the CSV file.|Data In|Integer|
    |Delimiter|A character that separates values in a row of the CSV file. For example, comma, tab, semicolon, pipe, or space.|Data In|String|
    |IsFirstRowHeader|True or false value that indicates whether the first row of the CSV file is a header.|Data In|Boolean|
    |Count|Returns the total number of rows containing data.|Data Out|Integer|
    |DataTable|Returns the extracted data from the CSV file in a DataTable.|Data Out|DataTable|

5.  To preview the data, right-click the **Return** field and click **Preview Data**.

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Reader](../concept/datareader-utility.md)

