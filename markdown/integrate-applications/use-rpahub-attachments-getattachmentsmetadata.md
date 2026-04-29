---
title: Use the GetAttachmentsMetadata component
description: Get the metadata of all attachments that are associated with a ServiceNow table record by using the GetAttachmentsMetadata component in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Attachments, ServiceNow, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetAttachmentsMetadata component

Get the metadata of all attachments that are associated with a ServiceNow table record by using the GetAttachmentsMetadata component in the RPA Desktop Design Studio.

## Before you begin

You must have access to the ServiceNow table that contains attachments.

Role required: none

## About this task

The maximum size of the attachments is 1024 MB.

You can configure the properties for the GetAttachmentsMetadata component. For more information about these properties, see [Properties of the Attachment components](../reference/properties-attachment-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Attachments**.

2.  Drag the GetAttachmentsMetadata component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetAttachmentsMetadata component to the corresponding ports of the other components.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SysID

</td><td>

The sys ID of the record that has the attachment. You can pass this value from a previously executed component.You can get the sys ID of a record following these steps:

1.  Select the record in the connected ServiceNow instance and right-click the header bar.
2.  Select Copy URL.
3.  In the URL, you can find the sys ID after the parameter sys\_id=. For example, 9d385017c611228701d22104cc95c371.


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

tableName

</td><td>

The name of the table that has the record with the attachments. You can pass this value from a previously executed component.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Returns the metadata of the attachments and passes to the next component.

</td><td>

Data Out

</td><td>

Object

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Attachments](../concept/attachments.md)

