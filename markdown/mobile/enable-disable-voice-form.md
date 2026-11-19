---
title: Enable or disable voice to form
description: Configure whether voice to form is turned on or off for your mobile instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/enable-disable-voice-form.html
release: australia
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 2
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable or disable voice to form

Configure whether voice to form is turned on or off for your mobile instance.

## Before you begin

Role required: admin

**Note:** Voice to form is currently only available on the following iOS devices: iPhone 15 Pro, iPhone 16 and later, iPad mini \(A17 Pro\), or iPad M1 or later. Voice to form requires Apple Intelligence.

## About this task

Voice to form is controlled by a mobile instance property. The `voiceToFormDisabled` property is enabled by default. Toggling the value to `true` disables the feature.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  In the **Mobile Properties** list, select **New**.

3.  On the form, fill in the fields as required.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the mobile property record. Enter `voiceToFormDisabled` to make this feature configurable.|
    |**Application**|Application scope where the mobile property is applied. To select a different application scope, select the globe icon on the instance banner, then select **Application scope**: *application\_scope*.|
    |**Description**|Description of the mobile property. For example: Turns off voice to form for the instance.|
    |**Type**|Data type of the mobile property record. Select **True/False** for the `voiceToFormDisabled` property.|
    |**Value**|Enter one of the following options: to disable voice to form, enter `true`; to keep voice to form enabled \(default\), enter `false`.|
    |**Active**|Whether the mobile property is activated. If the check box is cleared, the mobile property is not activated for use.|
    |**Is Public**|Determines whether the `voiceToFormDisabled` property is included in the API response. Mobile properties with this check box enabled are excluded from the `/user_client` API response.|
    |**Mobile App Config**|Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration; other users experience default behavior. To enter a value, start entering the application name or select the search icon to open the search dialog box.|
    |**Mobile Application**|Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app; other users experience default behavior. To enter a value, start entering the application name or select the search icon to open the search dialog box.|

4.  Select **Submit**.


## Result

When the property is set to `true`, the voice entry point no longer appears on any input form, including forms with client scripts. When the property is `false` or not set, the voice entry point and first-time onboarding tooltip are available on supported input forms.

**Parent Topic:**[Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-properties.md)

