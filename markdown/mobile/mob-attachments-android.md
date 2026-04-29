---
title: Configure different mobile attachment capabilities on Android devices based on user roles
description: Use a combination of system properties and mobile properties to enable different users on Android devices to share, download, or view attachments in external applications based on roles.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure different mobile attachment capabilities on Android devices based on user roles

Use a combination of system properties and mobile properties to enable different users on Android devices to share, download, or view attachments in external applications based on roles.

## Before you begin

Role required: admin

Make sure to select **Global** as the application scope.

Identify 2 groups of users:

<table id="table_sf3_lwf_kfc"><thead><tr><th>

Group A: users that CAN:

</th><th>

Group B: users that CAN'T:

</th></tr></thead><tbody><tr><td>

-   Share and download attachments
-   View attachments in external applications

</td><td>

-   Share and download attachments
-   View attachments in external applications

</td></tr></tbody>
</table>## About this task

After you identify the two groups of users, assign different roles to each group of users. You can assign more than one role to each group of users. For information about creating and assigning roles to users, see [Create a role](https://www.servicenow.com/docs/access?context=t_CreateARole&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** This feature is available on Android clients, version 19.5.1 and later.

## Procedure

1.  Set the system property **glide.sg.block\_mobile\_attachments\_external\_viewing** to `true`.

    For more information, see [Control whether users can view attachments in external applications on Android devices](vu-attach-extapp-android.md).

2.  Set the system property **glide.sg.block\_mobile\_attachments\_sharing** to `true`.

    For more information, see [Block users from downloading or sharing attachments](block-users-download-shar-attach.md).

3.  On your ServiceNow® instance, navigate to **All** &gt; **sys\_sg\_properties\_list.do**.

    The Mobile Properties list appears.

4.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

5.  On the form, fill in the fields.

<table id="table_blt_ryf_kfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `exemptedRoles-glide.sg.block_mobile_attachments_sharing` to enable sharing/downloading attachments and viewing attachments externally as a configurable feature. You must create it to configure it.**Note:** The record name is case-sensitive and must be entered as `exemptedRoles-glide.sg.block_mobile_attachments_sharing`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the Overflows Menu \(![Overflows menu image](../image/button-more-android.png)\) on the instance banner. Then select **Scope selectors &gt; Application scope:_application\_scope_**.

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Enables sharing/downloading/viewing attachments.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **exemptedRoles-glide.sg.block\_mobile\_attachments\_sharing** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter the name of role or roles you created for Group A \(users who CAN share/download attachments and who CAN view attachments in external applications\). If you need to specify multiple roles, enter them in a comma-separated list.

 For example: `role1, role2, role3`

</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the pre-auth property is included in the API response.

 By default, this option is not selected. If you want this property included in the /pre-auth API response, select this checkbox. For more information, see [Adaptive authentication events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the /user\_client API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration that you want to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the configuration name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose. Select a configuration for **Mobile App Config**.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application that you want to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose. Select an application for **Mobile Application**.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The Mobile Properties New record form clears.

7.  In the cleared Mobile Properties New record form, fill in the fields.

<table id="table_o2p_5cg_kfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `exemptedRoles-glide.sg.block_mobile_attachments_external_viewing` to enable sharing/downloading attachments and viewing attachments externally as a configurable feature. You must create it to configure it.

 **Note:** The record name is case-sensitive and must be entered as `exemptedRoles-glide.sg.block_mobile_attachments_external_viewing`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the Overflows Menu \(![Overflows menu image](../image/button-more-android.png)\) on the instance banner. Then select **Scope selectors &gt; Application scope:_application\_scope_**.

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Enables sharing/downloading/viewing attachments in external applications.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **exemptedRoles-glide.sg.block\_mobile\_attachments\_external\_viewing** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter the name of the role or roles you created for Group B \(users who CAN'T share/download attachments and who CAN'T view attachments in external applications\). If you need to specify multiple roles, enter them in a comma-separated list.

 For example: `role1, role2, role3`

</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the pre-auth property is included in the API response.

 By default, this option is not selected. If you want this property included in the /pre-auth API response, select this checkbox. For more information, see [Adaptive authentication events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the /user\_client API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration that you want to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the configuration name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose. Select a configuration for **Mobile App Config**.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application that you want to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose. Select an application for **Mobile Application**.

</td></tr></tbody>
</table>8.  Select **Submit**.


## What to do next

After updating these properties, the end user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

