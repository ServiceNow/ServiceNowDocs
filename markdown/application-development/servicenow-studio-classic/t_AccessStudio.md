---
title: Legacy - Access ServiceNow Studio
description: Application developers access ServiceNow Studio to create, import, or open applications.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Access ServiceNow Studio

Application developers access ServiceNow Studio to create, import, or open applications.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin

## Procedure

1.  Select the path available to your role.

    |User role|Action to open Studio|
    |---------|---------------------|
    |admin|Navigate to **All** &gt; **System Applications** &gt; **Studio**.|

    The Studio opens in a new browser tab and displays the Select Application modal dialog.

    ![The Select Application modal dialog with options to create application, import from source control or open an existing application.](../image/select-app.png)

2.  To create an application, click **Create Application**.

    The system displays a list of application creation options.

3.  To import an existing application from source control, click **Import From Source Control** list.

    Studio opens **Import From Source Control**page.

4.  To view an existing application, click the application name from the **Applications** list.

    The list also includes any store applications or scoped applications installed via plugins that are customized.

    **Note:** In a few scenarios for scoped applications installed via plugins, the **Name** field in the Store Applications \(sys\_store\_app\) table doesn't match the plugin name. To make sure you are choosing the correct application, search the Select Store Application list picker with the **Name** of the application mentioned in the sys\_store\_app. For example: The plugin **Agile - Scaled Agile Framework - Essential SAFe** creates the sys\_store\_app record with the name "SAFe". Therefore you would search the Select Store Application list picker with the word "SAFe".

5.  To open an installed store application so you can create your company's application-customization for it, click **Select Store application** and select the store application from the list picker display.

    ![Select store application dialog](../image/select-store-app-to-customize.png)

    Studio opens the selected application.

    **Note:** The linked icon ![Linked icon](../image/local-changes-linked.png) indicates that there are uncommitted local changes in the application. The property is ignored for your company applications in development. The **Can Edit Application in Studio** property for a store application determines if the application can be edited in Studio. If set to false, you see a warning that you cannot edit the application in Studio. But you can open the application in Studio to use Source Control features or to publish its customizations to the application repository. The default is true for new applications. The application's owner can change the property value before releasing a new version.


**Parent Topic:**[Legacy - ServiceNow Studio](../concept/c_ServiceNowStudio.md)

