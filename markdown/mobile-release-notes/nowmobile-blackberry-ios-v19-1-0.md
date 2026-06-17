---
title: Now Mobile for BlackBerry for iOS v19.1.0
description: The iOS v19.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-01-02"
reading_time_minutes: 3
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for iOS v19.1.0

The iOS v19.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_uw1_y14_31c" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS

 PRB1804331

</td><td>

A 'No data available' error appears on iOS devices

</td><td>

On app launch, the user observes the message, 'No data available please pull down to refresh'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1830036

</td><td>

The user is unable to log in to an instance when glide.sg.device\_ encryption\_enabled is set to true on an iOS device without a set passcode

</td><td>

The glide.sg.device\_ encryption\_enabled system property is used to enforce device encryption and requires that a device passcode is configured. However, setting this property to true prevents the instance from being logged into on iOS devices without a set passcode.

</td><td>

1.  Set the glide.sg.device\_ encryption\_enabled to true.
2.  Disable biometrics and passcode on an iOS device.
3.  Log in to the instance on Now Mobile.

 Expected behavior: There is an error message that shows a passcode requirement.

 Actual behavior: The app goes back to the instance selection page without any errors. If the user ends the app and reopens it from the home screen, it shows a blank screen.

</td></tr><tr><td>

Mobile iOS

 PRB1831810

</td><td>

A mobile publishing prefilled instance is missing if the optional instance nickname is not set

</td><td>

The instance selection page is shown instead of a prefilled instance.

</td><td>

1.  Submit an iOS mobile publishing app \(private or public\) with a prefilled instance URL, leaving the instance nickname empty.
2.  Open the iOS app for the first time.

 Expected behavior: A prefilled instance with an instance nickname populated from the instance URL should be present as the first item in the instance list.This matches the behavior when adding an instance manually.

 Actual behavior: The instance selection page is shown.

</td></tr><tr><td>

Mobile iOS

 PRB1756073

</td><td>

The user is not redirected to the barcode scanner screen

</td><td>

Jump-to-screen functionality after a successful action completion doesn't work as expected.

</td><td>

1.  Log in to the Mobile Agent app.
2.  Navigate to **Barcode scanner screen** &gt; **Scan Barcode** &gt; **Record screen**.
3.  Select the 'Foot' function configured to update one of the fields.
4.  Submit.

 Expected behavior: The user is redirected to the barcode scanner screen.

 Actual behavior: The user stays on the record screen.

</td></tr><tr><td>

Mobile iOS

 PRB1827058

</td><td>

The user is unable to select two buttons in the chat header when the choices are visible on a topic in Now Mobile

</td><td>

From Now Mobile, using the Virtual Agent Topics, if the choices are populated on the input box, the quick function instances are not selectable.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1822584

</td><td>

The Home page loads twice when a deep link is selected

</td><td>

Selecting a deep link that leads to a launcher screen displays the launcher screen twice if the mobile app is already located at the specified launcher tab.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1822582

</td><td>

The app crashes when closing and opening the app multiple times

</td><td>

The Agent app crashes when the user repeatedly closes the app, locks and unlocks the phone, and re-opens the app.

</td><td>

1.  Open the ServiceNow Agent app v18.4.0.
2.  Close the application in mobile.
3.  Lock the phone screen and then unlock it.
4.  Open the ServiceNow Agent app.
5.  Perform the above steps continuously in the same order.

 Observe an app crash.

</td></tr><tr><td>

Mobile iOS

 PRB1822270

</td><td>

A parameterized screen that uses the old parameters screen with an empty date parameter doesn't distinguish between the 'Favorites' / 'Saved by' parameters

</td><td>

Failure to decode the SGForm due to an empty date parameter which doesn't add the required 'Value' key in the encoded object.

</td><td>

1.  Configure parametrized screen with old parameters with a string and date parameters without default values.
2.  Open the parameters screen.
3.  Write 'STR1' in the string input and leave the date parameter empty.
4.  Select **Submit** / **Search** to open the screen.
5.  Save the screen in favorites.
6.  Navigate back and re-open the parameters screen.
7.  Write 'STR2' in the string input and leave the date parameter empty.
8.  Select **Submit** / **Search** to open the screen.

 Expected behavior: The screen should not be saved as the parameter values are different from the saved one.

 Actual behavior: The screen is already saved.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](../nowmobile-blackberry-available-versions.md)

