---
title: Use the UploadAttachment component
description: Attach documents to a table record in the RPA Hub by using the UploadAttachment component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Attachments, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the UploadAttachment component

Attach documents to a table record in the RPA Hub by using the UploadAttachment component in the RPA Desktop Design Studio.

## Before you begin

You must have access to the required ServiceNow table to upload attachments.

Role required: none

## About this task

A table in the RPA Hub contains one or more records and each record provides certain information. Attachments can provide additional, useful information about the record. The maximum size of the attachments is 1024 MB.

You can configure the properties for the UploadAttachment component. For more information about these properties, see [Properties of the Attachment components](../reference/properties-attachment-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Attachments**.

2.  Drag the UploadAttachment component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the UploadAttachment component to the corresponding ports of the other components.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

filePath

</td><td>

The path to the file that must be uploaded to the record from a previously executed component.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SysId

</td><td>

The sys ID of the record to upload the attachment to. You can also pass this value from a previously executed component.You can get the sys ID of a record following these steps:

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

Takes the table name that comprises the record from a previously executed component.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Returns the Boolean response on whether the file was successfully uploaded and passes to the next component.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Attachments](../concept/attachments.md)

