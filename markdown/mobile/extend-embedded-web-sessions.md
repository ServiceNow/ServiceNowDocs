---
title: Extend embedded web sessions
description: Extend embedded web sessions to keep mobile users logged in until the mobile OAuth token expires.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Extend embedded web sessions

Extend embedded web sessions to keep mobile users logged in until the mobile OAuth token expires.

## Before you begin

Role required: admin

## About this task

The **extend\_web\_session** mobile property is enabled by default. This property helps make hybrid experiences on ServiceNow® mobile apps seamless. The **extend\_web\_session** property extends an embedded web session so it’s valid for the same amount of time that native mobile apps are valid. Web session timeout is 30 minutes by default. Mobile sessions remain valid for 100 days. To keep mobile users logged in until the mobile OAuth token expires, use the **extend\_web\_session** mobile property to extend the web session timeout. You can turn off this feature by setting the **Value** field for this property to `False`.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields.

<table id="table_f4k_dsx_mzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record.

 Enter `extend_web_session` to enable admins to extend the length of time for mobile embedded web sessions.

 Mobile web sessions have a default timeout value. The **extend\_web\_session** mobile property overrides the default timeout value. End users remain logged in to the embedded web session for as long as the mobile OAuth token is valid.

 **Note:** The record name is case-sensitive and must be entered as `extend_web_session`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied.

 To select a different application scope, select the globe icon \(![Globe](../image/globe-icon.png)\) on the instance banner. Then select **Application scope: _application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. You must select **True/False** for the **extend\_web\_session** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:

 -   To enable extending web sessions to match mobile apps, enter `True`.
-   To keep the 30-minute web session length, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Indicates if the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive Authentication Events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

**Note:** For the **extend\_web\_session** mobile property, which is turned on by default, you can only turn off the extended web session time for users with the mobile app configuration that you specify for this field. If you don’t specify a Mobile App Config, all end-user web sessions are extended in Washington DC family release versions and later.

 To enter a value, either start typing the configuration name or select the search icon \(![Magnifying glass](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose.

 Select one of the following mobile app configs:

-   **Mobile Agent**
-   **Now Mobile**


</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 **Note:** For the **extend\_web\_session** mobile property, which is turned on by default, you can only turn off the extended web session time for users with the mobile application that you specify for this field. If you don’t specify a Mobile Application, all end-user web sessions are extended in Washington DC family release versions and later.

 To enter a value, either start typing the application name or select the search icon \(![Magnifying glass](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose.

 Select one of the following mobile applications:

-   If you selected **Mobile Agent** for the **Mobile App Config**, select **Agent**.
-   If you selected **Now Mobile** for the **Mobile App Config**, select **Request**.


</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

