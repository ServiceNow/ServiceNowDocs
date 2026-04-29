---
title: Use the AdjustBrightness component
description: Adjust the brightness of an image as part of an automation Workflow by using the AdjustBrightness component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Image Utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the AdjustBrightness component

Adjust the brightness of an image as part of an automation Workflow by using the AdjustBrightness component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the AdjustBrightness component. For more information about these properties, see [Properties of the Image Utilities components](../reference/util-imageutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Image Utilities**.

2.  Drag the AdjustBrightness component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the AdjustBrightness component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Image\)

</td><td>

Takes the image from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Value\)

</td><td>

Takes the value to adjust the brightness from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the image with the specified brightness.

</td><td>

Yes.To preview the data, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Connects to the Control Out port of one or more components.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of any other component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Image Utilities](../concept/image-utilities.md)

