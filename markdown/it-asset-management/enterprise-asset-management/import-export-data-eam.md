---
title: Import and export content data for Enterprise Asset Management
description: Import and export content data to the ServiceNow Enterprise Asset Management Content Service to improve the normalization process. On-premise users can use the Manage Enterprise Library module to import or export data via a zip file.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Enterprise Asset Management by enterprise administrators, Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Import and export content data for Enterprise Asset Management

Import and export content data to the ServiceNow Enterprise Asset Management Content Service to improve the normalization process. On-premise users can use the Manage Enterprise Library module to import or export data via a zip file.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **All** &gt; **Modules** &gt; **Manage Enterprise Library**.

2.  Open the Manage Enterprise Library form layout and select the **Active** check box to activate the module.

3.  Select **Save** and refresh the form layout.

4.  Navigate to the Manage Enterprise Library module.

5.  Import the content data to get the new data into your system.

    1.  Select **Import Enterprise Library Content**.

    2.  Select **Attach Content File** and then select the zip file that contains the content.

    3.  Select **Run Import**.

        After the data is imported, the content update schedule job,**EAM - Apply latest content changes**, is triggered to process the content updates.

6.  Export content to send the custom data or any enterprise models that are not fully normalized to the ServiceNow content service team.

    1.  Select **Content Service Opt-in: Export Enterprise Normalization Content**.

    2.  If you already haven't opted in to share the data with ServiceNow content service, select **opt-in** and refresh the Manage Enterprise Library page.

        For details on opting-in, see [Opt-in to Enterprise Asset Management Content Service](optin-cs-eam.md).

    3.  Select **Run Export**.

    4.  After the status changes to Ready for Download, refresh the page.

        A zip file is created and appears at the top of the Manage Enterprise Library page. If there is no content to export, an error message appears informing you that no content exists.

    5.  Download and send this zip file to the ServiceNow content service team.


**Parent Topic:**[Configuring Enterprise Asset Management by enterprise administrators](../concept/config-eam-enterrpriseadmins.md)

