---
title: ServiceNow Onboarding - Intune for iOS v14.4.0
description: The iOS v14.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-08-04"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v14.4.0

The iOS v14.4.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="AllOtherFixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1577633

</td><td>

A preconfigured instance name is duplicated after a successful login

</td><td>

After logging in to a preconfigured instance, an entry for that instance is created on the instance screen. If users delete it, it is recreated after a successful login.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1546920

</td><td>

Selecting the **X** \(**End Conversation**\) icon in the mobile app causes a new conversation to be created in the platform

</td><td>

The **End Conversation** button is clickable while the greeting topic is still in progress. If the user clicks the **X** icon at this stage, the system creates a new conversation instead of closing the current one.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1578550

</td><td>

Unable to create more than one email or phone menu types

</td><td>

It is possible, however, to create multiple link and text menu options.

</td><td>

1.  Log in to the instance.
2.  Navigate to Virtual Agent branding.
3.  Add multiple email or phone menu options.
4.  Log in to an iOS device.
5.  Enter 'VA'.
6.  Click **Menu option**.

Notice that not all menu options are displayed.


 Expected behavior: All menu options from branding appear.

 Actual behavior: Only one email and phone menu option appears.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1574365

</td><td>

Field level functions on boolean fields are not working on iOS

</td><td>

Field level functions defined on True/False fields are not working as expected on iOS devices.

</td><td>

1.  Log in to any Rome or San Diego instance.
2.  Open Now Mobile app in the mobile app builder.
3.  Open any base instance list screen segment like 'My requests' and open an incident.
4.  Configure the form screen's screen segments to contain any boolean field like **Active** or **Knowledge**.
5.  Define a function instance where the location is the field.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1577229

</td><td>

The keyboard does not disappear when navigating back to a string field and tapping **Done** on the Mobile Agent app

</td><td>

The **Submit** button remains greyed out when all required fields are completed. The keyboard does not disappear when going back to a string field and tapping **Done**, unless the current value is modified on the Mobile Agent app.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1582081

</td><td>

Duplicated function instance displays in two media sections, but only one has it configured in the Now Mobile app

</td><td>

When there are two media sections added to the launcher screen and one of them has a function instance that calls a phone number, the function instance displays in both media sections on iOS devices.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1589638

</td><td>

The number for the session count does not match the actual screens opened for an external user

</td><td>

 

</td><td>

1.  Open any mobile app.
2.  Log in to any instance as an external user.
3.  Change tabs and open screens.
4.  Send the app to the background.
5.  Open a browser and log in to the instance as an admin.
6.  Navigate to the User Experience dashboard \(Appsee dashboard\).
7.  Select **iOS**.
8.  Find your user's recent session.

 Expected behavior: There should be screen tags corresponding to the screens that the user opened in the mobile app.

 Actual behavior: There are no screen tags collected for this user session.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

