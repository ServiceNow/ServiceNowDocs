---
title: Use the OCR Text component
description: Extract the text from an image by using the OCR \(Optical Character Recognition\) Text component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the OCR Text component

Extract the text from an image by using the OCR \(Optical Character Recognition\) Text component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

**Important:**

Starting with the Yokohama release, the RPA Desktop Design Studio utilizes the latest version of the Tesseract OCR engine. This update improves image pre-processing, and performance optimizations. When updating older automations that include the OCR text component, you may notice slight differences in the output. Therefore, it’s important to validate your automations after the update.

Many properties of the OCR Text component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md).

The properties unique to the OCR Text component are given.

|Property|Text|
|--------|----|
|Image Source|Source from which the component takes the image.|

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **OCR Text**.

2.  Drag the OCR Text component to the Design surface.

3.  To configure the settings, click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

    The component has default settings that you may review and use.

4.  Configure the settings as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Engine|Engine name that is used for extracting the OCR fields.|
    |Language|Teseract engine that can support multiple languages. The user can select any language that is listed here.|
    |Line Height Tolerance|Font line height.|
    |ChangeDPI|Changes the Dots Per Inch \(DPI\) of Image as mentioned in the DPI property.|
    |DPI|DPI value.|
    |Extract Words|Text that is extracted in a word format. Otherwise, it's plain text.|
    |Invert|Image color that is inverted. For example, it inverts black to white.|
    |Language|Language that is used to extract.|
    |Scale Image|Scales the image by the given number.|
    |Threshold|Image that is converted out of Grayscale image or noise that is removed as per the threshold value.|
    |Threshold Value|Threshold value.|
    |Timeout|Time after which the component operation times out.|

5.  To close the OCR Settings window, click **OK**.

6.  To configure the input, see [Configure port properties](configure-input-port-properties.md).

7.  To configure the output, see [Configure output port properties](configure-output-port-properties.md).

8.  Connect the ports as described in the following table.

<table id="table_ktj_dzw_jrb"><thead><tr><th>

Port Type

</th><th>

Port name

</th><th>

Data type

</th><th>

Purpose

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Data In

</td><td>

Image/File Path

</td><td>

Bitmap/String

</td><td>

Takes the image or the path to the image.

</td><td>

The input depends on the option selected from the **Image Source**option in the Properties. -   **Port**: The data type is Bitmap.
-   **File Path**: The data type is String.


</td></tr><tr><td>

Data Out

</td><td>

Text

</td><td>

String

</td><td>

Returns the extracted text from the image.

</td><td>

 

</td></tr><tr><td>

Data Out

</td><td>

Confidence

</td><td>

Single

</td><td>

Returns the extracted text accuracy figure.

</td><td>

 

</td></tr></tbody>
</table>9.  To test the component, right-click the component bar and then click **Run From Here**.


## Extract text from images and display with the Show component

![Extract text from image and display with the Show component.](../image/OCR_Text_Filepath_2.PNG)

The OCR Text component takes a path to an image. The image comprises the text "servicenow". The component extracts the text from the image and passes the string to the Show component \(To use the Show component, see [Use the Show component](use-general-messagebox-show.md)\). The Show component takes the text through the Message Data In port and then displays the text in a window.

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

