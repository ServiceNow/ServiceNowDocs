---
title: Customize user experiences in Guided Application Creator
description: Customize how the application appears in each user experience that you select.If you selected the Mobile Agent mobile app as a user experience for your application, you can customize how the application appears in the mobile app.If you selected the classic ServiceNow AI Platform experience for your application, you can customize how the application appears in the application navigator.
locale: en-US
release: xanadu
product: Guided Application Creator
classification: guided-application-creator
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up an application in Guided Application Creator, Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Customize user experiences in Guided Application Creator

Customize how the application appears in each user experience that you select.

Before you begin:

1.  [Create an application record in Guided Application Creator](gac-create-app-record.md)
2.  [Define roles in Guided Application Creator](gac-create-roles.md)
3.  [Select user experiences in Guided Application Creator](gac-select-ux.md)
4.  [Designate data tables in Guided Application Creator](gac-designate-data-table.md)

![Customize a user experience](../image/GAC-workspace-experience.png)

**Parent Topic:**[Setting up an application in Guided Application Creator](set-up-app.md)

## Customize your application for the Mobile Agent mobile app

If you selected the Mobile Agent mobile app as a user experience for your application, you can customize how the application appears in the mobile app.

### Before you begin

Role required: sn\_g\_app\_creator.app\_creator or admin

**Note:** To edit application properties, a user must have at least one of the following:

-   admin role
-   sn\_g\_app\_creator.app\_creator role \(this role is automatically assigned when the sn\_app\_eng\_studio.user role is granted\)
-   delegated developer with delete permissions
-   delegated admin

### Procedure

1.  Next to **Mobile**, select **Start** to configure application details.

2.  On the form, fill in the fields.

<table id="table_uwx_d3d_vhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App icon

</td><td>

Icon that appears on the application home page in the mobile app.

</td></tr><tr><td>

Available offline

</td><td>

Option to enable users to update application records while in offline mode. This option is available only if the SG Offline Support \(com.glide.sg.offline\) plugin is activated.

 For information on offline mode, see [Updating records without an internet connection](https://www.servicenow.com/docs/access?context=offline-end-user&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

</td></tr><tr><td>

Name

</td><td>

Name of your application as it appears on the application home page. By default, this value is the application name that you created earlier.

</td></tr><tr><td>

Description

</td><td>

Description of your application. By default, this value is the application description that you created earlier.

</td></tr><tr><td>

Tables

</td><td>

Tables that appear as applets in the mobile app. Applets are subsections under your application that categorize the information and business processes in your application.

</td></tr><tr><td>

Roles

</td><td>

User roles that can access your application in the mobile app. By default, these values are the roles that you defined earlier.

</td></tr></tbody>
</table>3.  Select **Create**.


### What to do next

You've finished customizing your application for the Mobile Agent mobile app. If you selected another user experience, customize that user experience next. If you have no more user experiences left to customize, select **Done with apps**.

## Customize your application for the classic ServiceNow AI Platform experience

If you selected the classic ServiceNow AI Platform experience for your application, you can customize how the application appears in the application navigator.

### Before you begin

Role required: sn\_g\_app\_creator.app\_creator or admin

**Note:** To edit application properties, a user must have at least one of the following:

-   admin role
-   sn\_g\_app\_creator.app\_creator role \(this role is automatically assigned when the sn\_app\_eng\_studio.user role is granted\)
-   delegated developer with delete permissions
-   delegated admin

### Procedure

1.  Next to **Classic**, select **Start** to configure application details.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your application as it appears on the application navigator. By default, this value is the application name that you created earlier.|
    |Description|Description of your application. By default, this value is the application description that you created earlier.|
    |Tables|Tables in your application. Application modules are created for each table. By default, these values are the data tables that you designated earlier.|
    |Roles|User roles that can access your application. By default, these values are the roles that you defined earlier.|

3.  Select **Create**.


### What to do next

You've finished customizing your application for the classic ServiceNow AI Platform experience. If you selected another user experience, customize that user experience next. If you have no more user experiences left to customize, select **Done with apps**.

