---
title: Use the Convert component
description: Convert the format of an image to a different format by using the Convert component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Image Utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Convert component

Convert the format of an image to a different format by using the Convert component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Convert component. For more information about these properties, see [Properties of the Image Utilities components](../reference/util-imageutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Image Utilities**.

2.  Drag the Convert component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Convert component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Image

</td><td>

Takes the path to the current image from a previously executed component.For example, provide a file path of the image using the ReadFromFile component from Image Utilities.

</td><td>

Data In

</td><td>

Bitmap

</td></tr><tr><td>

Format

</td><td>

Takes the new image format from a previously executed component.Double click this option to select the format type from the Static Value field and select **OK**.

For example, select Png.

![Image format options such as png, jpg.](../image/imageformat-options-convert-rpa.png "Image format options")

</td><td>

Data In

</td><td>

ImageFormat

</td></tr><tr><td>

Return

</td><td>

Returns the image that is converted to the specified format.You can additionally add the Save component from Image Utilities to save the converted image to a different filepath.

![Read file path from ReadFromFile component, convert that image format using Convert component, and save it using Save component.](../image/convert-image-utlities-rpa.png "Convert component using other components")

</td><td>

Data Out

</td><td>

Bitmap

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Image Utilities](../concept/image-utilities.md)

