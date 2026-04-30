---
title: Use the GetRecordContextID component
description: Get the Sys ID of the ServiceNow form record that is associated to an attended configuration with the GetRecordContextID component in the RPA Desktop Design Studio. Sys ID is the output of the component. For example, Sys ID is used to fetch the attachments in a record.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Forms, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetRecordContextID component

Get the Sys ID of the ServiceNow form record that is associated to an attended configuration with the GetRecordContextID component in the RPA Desktop Design Studio. Sys ID is the output of the component. For example, Sys ID is used to fetch the attachments in a record.

## Before you begin

If you are running an automation from RPA Desktop Design Studio, then assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. In the **Bot Process** field, ensure to select an attended bot process that is enabled with Embedded Task Automation. In the **Attended Config** field, ensure to select an associated attended configuration. In the **Record Context** field, ensure to enter the Sys ID or URL of the ServiceNow form record. This is the output of your component. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

Role required: none

## About this task

Use the GetRecordContextID component to fetch the Sys ID of the ServiceNow form record, from where the automation is triggered. Use the GetAttachmentsMetadata component to get the metadata of the attachments of this record. After getting the attachment Sys ID, use the DownloadAttachment component to download the attachment. For more information about these components, see [Use the DownloadAttachment component](use-rpahub-attachments-downloadattachment.md) and [Use the GetAttachmentsMetadata component](use-rpahub-attachments-getattachmentsmetadata.md).

If you are triggering the automation from the ServiceNow form's UI action \(button\) and it executes using the Attended Robot application, then the GetRecordContextID component returns the Sys ID of the ServiceNow form record.

You can configure the properties for the GetRecordContextID component. For more information about these properties, see [Properties of the Forms components](../reference/sn-forms-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Forms**.

2.  Drag the GetRecordContextID component to the Design surface.

3.  Connect the data and control ports of the GetRecordContextID component to the corresponding ports of other components as described in the following table.

    |Port Name|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |SysID \[Data Out\]|Returns the Sys ID of the ServiceNow form record.|No|
    |Control In|Connect to the Control Out port of one or more components.|Yes|
    |Control Out|Connect to the Control In port of another component or activity as per the required automation logic.|No|

4.  To test the component, right-click the title bar of the component and select **Run From Here**.


**Parent Topic:**[Forms](../concept/forms_sn_rpa_studio.md)

