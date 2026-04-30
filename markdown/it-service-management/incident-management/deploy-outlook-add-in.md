---
title: Deploy the ServiceNow Add-in for Microsoft Outlook
description: Deploy the ServiceNow add-in for Microsoft Outlook to chat with a virtual agent, create incidents and VTB tasks from within the Microsoft Outlook.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Microsoft Outlook to create incidents and VTB tasks, Configure, Incident Management, IT Service Management]
---

# Deploy the ServiceNow Add-in for Microsoft Outlook

Deploy the ServiceNow add-in for Microsoft Outlook to chat with a virtual agent, create incidents and VTB tasks from within the Microsoft Outlook.

## Before you begin

In addition to having one of the following roles on the ServiceNow instance, you must be an Office365 administrator to deploy the ServiceNow add-in.

Role required: admin, sn\_outlook\_addin.outlook\_addin\_setup

## About this task

Deploy the ServiceNow add-in to Microsoft Outlook using the instructions in this Microsoft article: [Publish Office Add-ins using Centralized Deployment via the Office 365 admin center](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/centralized-deployment).

**Note:** You must be an Office365 administrator to deploy the ServiceNow add-in.

The ServiceNow add-in is only supported for use with Outlook for Mac and Outlook for Windows \(Requirement set 1.4\).

You can add or remove fields directly on the Incident form for users with the itil role by customizing the Outlook view form layout. For users that do not have the itil role, you can configure a Service Catalog record producer to use for creating new incidents.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  Click **New** on the **Office Manifests** page.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Add-in Name|A user-friendly name for the add-in. For example, if the add-in needs to be deployed only for administrators, you can choose to name it accordingly.|
    |Description|A short description of the add-in. For example, if the add-in is for a help desk, you can write a short description accordingly.|
    |Plugin ID|A unique identification string for the add-in you are deploying. You can change the plugin ID value to a new UUID to allow usage of multiple instances of the add-in.|
    |Version|Version of the plugin execution.|
    |Icon URL|HTTPS URL or relative URL for ServiceNow icon to be displayed in Microsoft Outlook.|
    |Active|Indicates that the add-in is active.|

4.  Click **Submit**.

    **Note:** The Office Controls related list shows the menu and menu items associated with the add-in.

5.  Click **Download Manifest** to download the add-in manifest file and follow the instructions in the Microsoft article for deployment. Microsoft article: [Publish Office Add-ins using Centralized Deployment via the Office 365 admin center](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/centralized-deployment)page.

6.  You can also customize the add-in by clicking **Clone Manifest** from the context menu.

    This option clones the current manifest into a new record that allows customizing the labels, icons, menus, and menu items.

7.  To customize the Incident form for users with the itil role, configure the Incident form layout directly.

    1.  Click the context menu icon \(![Context menu icon.](../image/outlook-context-menu.png)\) on the form and select **View** &gt; **Outlook**.

    2.  Click the context menu again and select **Configure** &gt; **Form Layout**.

    3.  Add or remove fields, as needed.

8.  To customize the Incident form for users that do not have the itil role, use a Service Catalog record producer to configure the Incident form.

    1.  Navigate to **Service Catalog** &gt; **Record Producers**.

    2.  Right-click the record producer to use for creating new incidents and select **Copy sys\_id**.

    3.  Paste the copied sys\_id into the **Value** field of the **Provide sys\_id of the record producer for create incident action from Outlook Add-In** \(**sn\_outlook\_addin.create\_incident\_cat\_item**\) system property.


**Parent Topic:**[Configuring Microsoft Outlook to create incidents and VTB tasks](../concept/create-incident-outlook.md)

