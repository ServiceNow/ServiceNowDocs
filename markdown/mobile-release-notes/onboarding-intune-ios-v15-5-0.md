---
title: ServiceNow Onboarding - Intune for iOS v15.5.0
description: The iOS v15.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2023-03-02"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v15.5.0

The iOS v15.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## New feature

Users can launch a demo to try the Mobile Onboarding - Intune app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS

 PRB1635847

</td><td>

An 'Invalid URL' error is thrown when the user clicks into a URL function that has dynamic substitution parameters

</td><td>

The 'Invalid URL' message is thrown when the function has 'type' set to 'url' and the URL has substitution parameters. When those parameters are removed, the function works on iOS.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1638646

</td><td>

If the user enables the 'Show signature' field when creating a Mobile Function, the action item is executed regardless of the answer to the confirmation message

</td><td>

The signature field is enabled even if the user selects **Cancel** in the confirmation message.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1633084

</td><td>

The 'Reservation sensitivity' description/textView is not read by Voiceover

</td><td>

The content in the **Reservation sensitivity** field is not read by Voiceover.

</td><td>

1.  Tap the '…' menu button in the navigation bar \(top right\).
2.  Tap **Make a reservation** from the menu.
3.  Tap **Desks**.
4.  Tap **Browse All**.
5.  Tap **Next** without changing anything.
6.  Select any Desk \(for example, 'A1.0308'\).
7.  Tap the **Next** Button.
8.  Turn VoiceOver On.
9.  Select \(One tap\) the 'Reservation sensitivity' Cell.

 Expected behavior: The user hears, the message 'Reservation sensitivity, Subject appears on your calendar and is viewable by all unless set to private, Normal, Button'.

 Actual behavior: The user hears, 'Reservation sensitivity, Normal, Button' \(without the two line description\).

</td></tr><tr><td>

Mobile iOS

 PRB1618804

</td><td>

A search list ignores the previous selections after the user makes another search

</td><td>

SGSearchPickerViewController resets the list of selected items \(selectedModelIndexes\) every time a new search is performed.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1634046

</td><td>

The app crashes when the user clicks the Camera icon on the home page and captures an image

</td><td>

 

</td><td>

1.  Log in to Now Mobile.
2.  On the Home page, click the Camera icon and capture an image.

 Observe that the App crashes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

