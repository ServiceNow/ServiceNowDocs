---
title: Enable mobile header color
description: Configure the EnableMobileHeaderColor property so that the header of native mobile screens displays a background color in the ServiceNow mobile apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/enable-mobile-header-color.html
release: brazil
topic_type: task
last_updated: "2026-11-13"
reading_time_minutes: 2
keywords: [mobile header color, EnableMobileHeaderColor, mobile property, header]
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable mobile header color

Configure the **EnableMobileHeaderColor** property so that the header of native mobile screens displays a background color in the ServiceNow mobile apps.

## Before you begin

Role required: admin

## About this task

The **EnableMobileHeaderColor** property controls whether the header of native mobile screens displays a background color. When you set the value to `true`, the header color applies to native mobile client records on all mobile screens, except modals.

**Note:** If this property isn't defined or its value is `false`, the header of native mobile screens doesn't display a background color.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields as required.

<table id="table_hdr_clr_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `EnableMobileHeaderColor` to make this feature configurable.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(\[Omitted image "globe-icon.png"\] Alt text: globe image\) on the instance banner. Then select **Application scope: _application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Display a background color in the header of native mobile screens`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. For this property, select **True/False**.

</td></tr><tr><td>

Value

</td><td>

The following values can be entered:-   To display a background color in the header of your mobile screens, enter `true`. The header color applies to mobile client records on all mobile screens except modals.
-   To display mobile headers without a background color, enter `false`.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is active. If the check box is cleared, the property is inactive.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option isn't selected. To include this property in the **/pre\_auth** API response, select this check box. For more information, see [Adaptive authentication events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/adaptive-authentication-events.md).

 Mobile properties with this check box enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start entering the application name or select the search icon \(\[Omitted image "search-icon.png"\] Alt text: magnifying glass image\). The search dialog box lists the configurations from which you can choose.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start entering the application name or select the search icon \(\[Omitted image "search-icon.png"\] Alt text: magnifying glass image\). The search dialog box lists the applications from which you can choose.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The header of native mobile screens displays a background color. When users switch instances, the app applies the header that matches the property value on the instance they switch to.

## What to do next

After updating this property, the end user must refresh the app to get the latest feature configurations.

**Parent Topic:**[Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-properties.md)

