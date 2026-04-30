---
title: Use the ReadBarcodes component
description: Read multiple barcodes and return their contents by using the ReadBarcode component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Barcode, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ReadBarcodes component

Read multiple barcodes and return their contents by using the ReadBarcode component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The ReadBarcodes component reads multiple barcodes from an image file that it receives from another component.

The ReadBarcodes component returns a single output that contains concatenated text, with each item on a new line.

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Barcode**.

2.  Drag the ReadBarcodes component to the Design surface.

3.  Confirm the configuration of the component's input fields.

    For more information, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ReadBarcodes component to the corresponding ports of the other components as described in the following table.

    |Port|Description|Port type|Data type|Required|
    |----|-----------|---------|---------|--------|
    |Image|Receives an image that contains barcodes|Data In|Bitmap|Yes|
    |Return|Returns a value that includes concatenated information from each barcode|Data Out|String|Yes|

    To test the component, on the **Design** tab, select **Run**.


**Parent Topic:**[Barcode](../concept/barcode.md)

