---
title: Documents widget
description: You can add, edit, or delete documents associated with records based on user permissions through the Documents widget. You can use this widget in your portal or clone and customize it.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Documents widget

You can add, edit, or delete documents associated with records based on user permissions through the Documents widget. You can use this widget in your portal or clone and customize it.

**Note:** The Documents widget is available with the Multi Provider Document Services Framework plugin \(com.snc.multiprovider\_documents\). For more information, see [Multi Provider Document Services Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/mp-document-services-framework-landing.md).

Add, edit, and delete documents related to a record with the Documents widget. You can drag and drop multiple files at a time, including editing and adding new versions. The default version shown is the latest version.

The maximum document size is 100 MB and concurrent uploads should be less than 10 MB.

**Note:** External users don’t have permission to share documents, review or approve documents, or access records in the platform.

![Related Documents widget](../image/documents-widget.png "Related Documents widget")

## Configure the Related Documents widget

Configure the Related Documents widget for records.

<table id="table_hqw_mry_qtb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record ID

</td><td>

Sys\_id of the record for which the documents are listed.

</td></tr><tr><td>

Record table

</td><td>

Table name of reference record.

</td></tr><tr><td>

Title

</td><td>

Title of the related document widget. The default title is Documents.

</td></tr><tr><td>

Popup before upload

</td><td>

Select this option to provide a dialog box to enter document details and description for a single file.**Note:** This option doesn’t appear if multiple files are selected.

</td></tr><tr><td>

Metadata form view

</td><td>

The configured form view to be opened when **Edit Document** is selected or while uploading a single file. By default, the **dw** form view is selected. This form contains only **Name** and **Description** fields.

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

