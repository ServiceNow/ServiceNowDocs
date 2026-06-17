---
title: ServiceNow Onboarding - Intune for iOS v11.5.0
description: The iOS v11.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-03-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v11.5.0

The iOS v11.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_szl_gxw_r4b" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1417589

</td><td>

Decimal type field issue in the Now Agent app

</td><td>

The value of the decimal type field is not set properly when users set it in the Now Agent mobile app.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1451083

</td><td>

For Virtual Agent on mobile clients, 'Show Me Everything' and 'Topics/Options' do not support dynamic text font

</td><td>

 

</td><td>

1.  Navigate to **Settings** &gt; **Accessibility** &gt; **Display &amp; Text Size** &gt; **Larger Text** and select a large font.

Notice that the screen refreshes to the new default large text size.

2.  Open 'Mobile Release'.
3.  Start a Virtual Agent chat.

Notice that the chat respects the large text settings.

4.  Select **Show Me Everything**.

 Notice that the button and the list do not respect the settings.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1454258

</td><td>

URL button type URL encoding behavior differences between IOS and Android with dynamic values

</td><td>

When setting up URL type actions to navigate to a webpage, it breaks if it passed a non-encoded special character for the dynamic field for Android. This works in iOS, but will be cut off at the special character. When the character is encoded, it works for Android.

</td><td>

1.  Open a Paris instance.
2.  Create an action function that makes use of a field on the form applet.
3.  For the field you are referencing, make sure to have a special character in it like '\#' when testing in the form applet.

For example, 'Activate Network Monitoring \# Service' is the short\_description value for the record.

4.  Test the action on Android.

Notice that the page is blank when clicked.

5.  Test the action on iOS.

Notice that the page loads with results, but the search text is cut off at the special character.

6.  Navigate back to the instance and replace it with the encoded version of that field.

For example, add a calculated field 'u\_short\_description\_encoded' to return that value and replace 'short\_description' in the action function URL.

7.  Test the action on Android and see that it works as expected.

Results load, and the special character is displayed in the search box.

8.  Test the action on iOS.

 Notice that it works as expected, but the special character does not load in the search box.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1455780

</td><td>

iOS Activity Stream links in field change items are not clickable

</td><td>

 

</td><td>

1.  In the desktop UI, open any incident and set the 'Resolution Notes'.
2.  View the incident in the mobile app and check the 'Activity Stream' tab.
3.  Select the link.

 Expected behavior: A screen is opened in a web view to view the link.

 Actual behavior: Nothing occurs.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1460465

</td><td>

The 'See All' option does not function for some horizontal item streams if a media section is present

</td><td>

The 'See All' link does not work for some horizontal item sections in the Now Mobile app. The link is active for a few seconds, but if the page sits for 5 seconds, the links no longer work. The link works if the section contains no items.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

