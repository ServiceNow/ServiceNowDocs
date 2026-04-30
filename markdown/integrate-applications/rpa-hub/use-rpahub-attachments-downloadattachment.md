---
title: Use the DownloadAttachment component
description: Download the attachments from the ServiceNow table record to the local drive by using the DownloadAttachment component in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Attachments, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the DownloadAttachment component

Download the attachments from the ServiceNow table record to the local drive by using the DownloadAttachment component in the RPA Desktop Design Studio.

## Before you begin

You must have access to the ServiceNow table record.

Role required: none

## About this task

The maximum size of the attachments is 1024 MB.

You can configure the properties for the DownloadAttachment component. For more information about these properties, see [Properties of the Attachment components](../reference/properties-attachment-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Attachments**.

2.  Drag the DownloadAttachment component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the DownloadAttachment component to the corresponding ports of the other components.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

attachmentSysID

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

folderPath

</td><td>

The path in the local drive where the attachment will be downloaded.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Overwrite

</td><td>

Returns a true or false value that indicates whether the file was successfully downloaded. If the download location already has a file with the same name, the operation fails.

</td><td>

Data In

</td><td>

Boolean

</td></tr><tr><td>

Return

</td><td>

Returns the details of the downloaded file as an object and passes it to another component.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Attachments](../concept/attachments.md)

