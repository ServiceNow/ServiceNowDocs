---
title: Enable external users to access attachments
description: Enable users who have been assigned the snc\_external role to be able to view, upload, and download attachments on their ServiceNow mobile app.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable external users to access attachments

Enable users who have been assigned the snc\_external role to be able to view, upload, and download attachments on their ServiceNow mobile app.

## Before you begin

Role required: admin

## About this task

When you assign the snc\_external role to users who are external to your organization, they can't access resources with their ServiceNow mobile app unless explicitly enabled. For more information about the snc\_external role, see [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

You can use the mobile property **allow\_snc\_external\_attachment\_access** to remove restrictions on attachments for users assigned the snc\_external role. When the **allow\_snc\_external\_attachment\_access** mobile property is set `true`, external users can use the mobile offline mode and access attachments from the following components and locations:

-   [Activity streams](https://www.servicenow.com/docs/access?context=c_activity-streams&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   [Legacy parameter screen \(UI parameters\), Quebec and earlier](../concept/parameter-input-screen.md)
-   [Input form screen \(sys\_sg\_parameter\_screen table\), Rome and later](../concept/parameter-input-screen.md)
-   [Details screen using the Attachment list](../concept/sg-mobile-attachments.md)
-   [Offline mode](../concept/mobile-offline-mode.md)

The **allow\_snc\_external\_attachment\_access** mobile property is turned off by default and external users can't access attachments.

Mobile properties are configured as records in the sys\_sg\_properties table on the ServiceNow Mobile Platform server. The ServiceNow instance sends the mobile property to mobile apps after authentication. Then the property turns on or turns off a feature on the mobile app.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

3.  On the form, fill in the fields.

<table id="table_ttj_nlq_mtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `allow_snc_external_attachment_access` to make this feature configurable. The **allow\_snc\_external\_attachment\_access** property is turned off by default and you must create it on your instance to configure it. It isn't visible on the instance until you create it.**Note:** The record name is case-sensitive and must be entered as `allow_snc_external_attachment_access`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe UI icon.](../image/globe-icon.png)\) on the instance banner. Then select **Application scope: _application\_scope_**. For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Determines whether users in the snc_external role can access attachments.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **allow\_snc\_external\_attachment\_access** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:-   To enable external users to access attachments, enter `True`.
-   To prevent external users from accessing attachments, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other external users don't have access to this mobile property and instead experience default behavior so they can't access attachments.

 To enter a value, either start typing the configuration name or select the search icon. The search dialog box lists the configurations from which you can choose. Select a configuration in the Mobile app configs dialog box.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other external users don't have access to this mobile property and instead experience default behavior so they can't access attachments.

 To enter a value, either start typing the application name or select the search icon. The search dialog box lists the applications from which you can choose. Select an application in the Mobile Applications dialog box.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must pull to refresh on the launcher screen to get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

