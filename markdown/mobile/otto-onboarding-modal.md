---
title: Otto onboarding modal
description: Configure the ottoOnboardingModalEnabled mobile property to turn the Otto onboarding modal on or off in the ServiceNow mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/otto-onboarding-modal.html
release: australia
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 2
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Otto onboarding modal

Configure the `ottoOnboardingModalEnabled` mobile property to turn the Otto onboarding modal on or off in the ServiceNow mobile app.

## Before you begin

Role required: admin

**Note:** This property is available beginning in mobile client release 22.1.0.

## About this task

The Otto onboarding modal introduces users to Otto the first time they access the mobile app. The `ottoOnboardingModalEnabled` property is enabled by default, and the modal appears only once per user. Set the property to `false` to prevent the onboarding modal from appearing.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  In the **Mobile Properties** list, select **New**.

3.  On the form, fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the mobile property record. Enter `ottoOnboardingModalEnabled` to make this feature configurable.|
    |**Application**|Application scope where the mobile property is applied. To select a different application scope, select the globe icon on the instance banner, then select **Application scope: _application\_scope_**.|
    |**Description**|Description of the mobile property. For example: `Turns off the Otto onboarding modal in the mobile app.`|
    |**Type**|Data type of the mobile property record. Select `True/False` for the `ottoOnboardingModalEnabled` property.|
    |**Value**|Enter one of the following values: `true` to show the Otto onboarding modal \(default\), or `false` to turn off the Otto onboarding modal.|
    |**Active**|Whether the mobile property is activated. If the check box is cleared, the mobile property is not activated for use.|
    |**Is Public**|Determines whether the `ottoOnboardingModalEnabled` property is included in the API response. Mobile properties with this check box enabled are excluded from the `/user_client` API response.|
    |**Mobile App Config**|Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users experience default behavior. To enter a value, start entering the application name or select the search icon to open the search dialog box.|
    |**Mobile Application**|Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users experience default behavior. To enter a value, start entering the application name or select the search icon to open the search dialog box.|

4.  Select **Submit**.


## What to do next

After updating this property, the end user must refresh the app to get the latest feature configurations.

**Parent Topic:**[Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-properties.md)

