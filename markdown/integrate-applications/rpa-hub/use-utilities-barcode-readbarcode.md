---
title: Use the ReadBarcode component
description: Read a single barcode and return its contents by using the ReadBarcode component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Barcode, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ReadBarcode component

Read a single barcode and return its contents by using the ReadBarcode component in RPA Desktop Design Studio.

## Before you begin

Add the Barcode Reader plugin from the Plugins Manager before using the connector. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Role required: none

## About this task

The ReadBarcode component reads a single barcode from an image file that it receives from another component.

The ReadBarcode component can return both the value and the encoding type \(format\) of the barcode. The encoding value that the Type parameter returns may be one of the following supported formats:

-   AZTEC
-   CODABAR
-   CODE\_39
-   CODE\_93
-   CODE\_128
-   DATA\_MATRIX
-   EAN\_8
-   EAN\_13
-   ITF
-   MAXICODE
-   PDF\_417
-   QR\_CODE
-   RSS\_14
-   RSS\_EXPANDED
-   UPC\_A
-   UPC\_E
-   All\_1D
-   UPC\_EAN\_EXTENSION
-   MSI
-   PLESSEY
-   IMB
-   PHARMA\_CODE

If the component can't read the barcode, it returns an error.

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Barcode**.

2.  Drag the ReadBarcode component to the Design surface.

3.  Confirm the configuration of the component's input fields.

    For more information, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ReadBarcode component to the corresponding ports of the other components as described in the following table.

    |Port|Description|Port type|Data type|Required|
    |----|-----------|---------|---------|--------|
    |Image|Receives an image that contains a barcode|Data In|Bitmap|Yes|
    |Type|Returns the barcode type|Data Out|String|Yes|
    |Result|Returns the encoded value of the barcode|Data Out|String|Yes|

    To test the component, on the **Design** tab, select **Run**.


**Parent Topic:**[Barcode](../concept/barcode.md)

