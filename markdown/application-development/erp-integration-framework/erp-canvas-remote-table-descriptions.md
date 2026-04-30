---
title: ERP Data Hub remote table form field descriptions
description: The Remote table form in ERP Data Hub enables you to create and edit remote tables in the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub remote table form field descriptions

The Remote table form in ERP Data Hub enables you to create and edit remote tables in the ERP \(Enterprise Resource Planning\) model.

<table id="table_ep5_44s_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remote table on the ServiceNow AI Platform.

</td></tr><tr><td>

ERP model

</td><td>

ERP model connected to the remote table. The ERP model controls the available fields on the remote table.**Note:** Changing the ERP model removes any previously configured table fields that aren't available on the new model.

To change the model for an ERP remote table, you must select the **Unlock ERP model field** button and then select the **Unlock model change** button on the confirmation dialog.

</td></tr><tr><td>

ERP module

</td><td>

Functional area or component within an ERP system. The module represents a distinct set of features and functionalities tailored to address a set of business processes or activities.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that the remote table is linked to. The connected system represents the ERP instance that is linked to the model, enabling data flow and interaction between the model and the connected ERP system. For more information, see [Create an ERP system in ERP Data Hub](../task/create-an-erp-system.md).

</td></tr><tr><td>

Remote table link

</td><td>

Name of and link to the remote table on the ServiceNow AI Platform.Selecting the remote table link opens a new browser tab, where you can explore, query, and manage the remote table.

</td></tr><tr><td>

Attachment setting

</td><td>

How the remote table uses attachments, which contain the remote data from the ERP system.The options are:

-   **None**: No attachment is used for the remote table.
-   **Save attachment**: Generate a new attachment when specified in the scheduled query or by selecting the **Refresh attachment data** button.
-   **Use attachment**: The current attachment, if available, is used locally.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the ERP remote table.

</td></tr><tr><td>

Long text

</td><td>

Additional details on the contents of the remote table.

</td></tr><tr><td>

Requires queryable field

</td><td>

Indicates whether you can retrieve data from the remote table without querying the source table.Smaller tables, such as a currency table, can have data stored locally and thus don't require a query to retrieve fields.

</td></tr><tr><td>

Enable schedule

</td><td>

Option to create a scheduled query \(ETL extraction\) to fetch a new version of the attachment data.**Note:** The **Attachment setting** field must be set to **Save attachment** or **Use attachment** for this option to be available.

</td></tr><tr><td>

Daily schedule time

</td><td>

Time, in 24-hour format, for when the schedule runs every day.

</td></tr><tr><td>

Scheduled encoded query

</td><td>

Details on any scheduled extraction queries for the remote table.Create an encoded query string using a filter on the remote table list and paste the string into the **Encoded query** field. For more information on creating encoded queries, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

