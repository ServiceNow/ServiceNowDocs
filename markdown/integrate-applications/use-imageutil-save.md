---
title: Use the Save component
description: Save an image to a specific location as part of an automation Workflow by using the Save component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Image Utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Save component

Save an image to a specific location as part of an automation Workflow by using the Save component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Save component. For more information about these properties, see [Properties of the Image Utilities components](../reference/util-imageutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Image Utilities**.

2.  Drag the Save component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Save component to the corresponding ports of the other components as described in the following table.

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

Data In \(Filepath\)

</td><td>

Takes the new path to the location where the method saves the image from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Overwrite\)

</td><td>

Takes the Boolean response to whether the method should overwrite the same file at the new location from a previously executed component.

</td><td>

No

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the Boolean response to whether the operation was successful and passes to the next component.

</td><td>

Next.To preview the data, right-click the **Return** field and click **Preview Data**.

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

