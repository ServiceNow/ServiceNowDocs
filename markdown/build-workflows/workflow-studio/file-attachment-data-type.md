---
title: File attachment data type
description: Store a single file attachment as part of the action or flow's associated record rather than a record in the system Attachment table.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Input and output data variables, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# File attachment data type

Store a single file attachment as part of the action or flow's associated record rather than a record in the system Attachment table.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|

## General guidelines

-   **Create one input per attachment**

    Create a separate file attachment input for each file attachment you want to store. The file attachment data type only supports adding one attachment file per input. The input stores the file attachment in the same record as that associated with the action or flow. You may have to create a custom field of the data type file attachment to store a single attachment.

-   **Manage attachments with existing actions**

    Use the existing attachment actions to manage attachments associated with records and email. There are existing actions to copy, delete, get from record, look up, and move attachments. Storing an attachment as a file attachment data type prevents you from managing attachments with the standard attachment actions.


**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

