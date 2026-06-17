---
title: ServiceNow Onboarding - Intune for Android v13.2.0
description: The Android v13.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-12-16"
reading_time_minutes: 5
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v13.2.0

The Android v13.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android \(non-classic\)

 PRB1441814

</td><td>

No confirmation message appears after creating a ticket

</td><td>

Users are unable to identify that the ticket has been created.

</td><td>

1.  Install the ServiceNow Agent application on the device.
2.  Enable Talkback and open the app.

The log in screen appears.

3.  Log in to the instance and try with a demo account.
4.  Navigate to **Service Desk Agent** &gt; **Launch Demo**.
5.  Navigate to **My Incidents** &gt; **More** &gt; **New control** using the swipe gesture and activate it.
6.  Complete the required fields and activate the **Submit** control.

 Expected behavior: A confirmation message should appear after creating a ticket and TalkBack should announce the information about the incident.

 Actual behavior: Notice that an incorrect confirmation message appears. It says there are '2 new message'. The same issue is observed with a keyboard and after editing a ticket.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1350437

</td><td>

Exception during user log out

</td><td>

Users observe the message 'Exception while decoding JWT - Invalid JWT serialization'.

</td><td>

1.  Launch the Requestor Mobile app.
2.  Log in to the instance.
3.  Keep the app open and make it idle for some time \(less than a minute\).
4.  Navigate to 'Articles ALP' or perform any operation.
5.  Leave the app idle for some time \(around 2 to 3 minutes\).
6.  Click **Log out**.

 Notice that you experience some delay during logging out and during that time, the exception is shown.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1536243

</td><td>

Unable to access Virtual Agent topics on the Now Mobile app for Android

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1536063

</td><td>

The search filter items' boundary line is cut off from the right side

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  On the services screen, try searching with an admin.

 Observe that on the results page, the boundary line for the people group is cut off and not fully displayed.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1532687

</td><td>

Virtual Agent Chat in the Now Mobile app does not handle carriage return properly

</td><td>

A new line does not work properly and it stays in the same line.

</td><td>

1.  Open the instance.
2.  Navigate to 'Service'.
3.  Click **+** and select **Chat with VA**.
4.  Click **Select Everything**.
5.  Select **Test SNC Demo topic**.

Notice that the message is displayed in the same line in the mobile app, but displayed properly on a desktop.


 Expected behavior: Anything after '\\n' should be in the new line.

 Actual behavior: The mobile app does not show the new line and message is displayed in the same line.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1529303

</td><td>

Fields are reset when submitting a catalog item

</td><td>

Not selecting any values in the choice variable is redirecting the user to the services applet launcher page instead of the catalog item form.​ All the values completed in the form are cleared and the user has to complete the form again.​

</td><td>

1.  Log in to the instance on the Now Mobile app.
2.  Click the 'Services' tab.
3.  Select the 'Create Incident' record producer.
4.  Complete the description.
5.  Click **Urgency**.
6.  Do not select any value, and click **X**.

 Expected behavior: The user should be redirected back to the record producer form.

 Actual behavior: Notice that the user is taken back to the 'Services' applet launcher screen instead of the record producer form.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1528949

</td><td>

On devices with Android OS 9.0 and above, actionable push notifications are not automatically dismissed after adding an inline message

</td><td>

The notification persists after adding an inline reply or message in the notification. Push actions that do not need an inline reply dismiss automatically after the action is taken.

</td><td>

1.  Log in to the instance as an admin.
2.  Create a WOT and assign it to a user.
3.  As the user, receive a push notification with the **Accept/Reject** action.
4.  Select **Reject**, add inline reply text, and submit

 Expected behavior: The notification should be dismissed.

 Actual behavior: The notification remains. The **Approve** action does not need an inline message as part of the push action submission, so the notification automatically dismisses.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1528227

 [KB0997168](https://hi.service-now.com/kb_view.do?sysparm_article=KB0997168)

</td><td>

A blank area is displayed under a media section that shows an image

</td><td>

An unexpected blank area is displayed under the media section that shows an image when using an Android app. The blank area is not displayed on iOS.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1523744

 [KB1000141](https://hi.service-now.com/kb_view.do?sysparm_article=KB1000141)

</td><td>

The option \(phone/emails\) menu does not retrieve a unique value

</td><td>

Since the introduction of the options menu within Virtual Agent, the branding menu items are not displayed correctly if users have the same type \(phone, email\) as the menu item. This issue only occurs on Virtual Agent within the mobile app.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1522436

 [KB0997615](https://hi.service-now.com/kb_view.do?sysparm_article=KB0997615)

</td><td>

A request for a PIN is prompted when the orientation of a device is changed in the mobile app

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1536421

</td><td>

The theme is not updated when switching instances

</td><td>

The new theme does not appear unless the app is swipe-closed and relaunched after logging in.

</td><td>

1.  Log in to an instance with a mobile theme set up.

Observe that the theme colors are applied.

2.  Log out of the instance.
3.  Log in to a different instance \(with no theme, or a different theme\).

Observe that the theme from the first instance is still used.


 Expected behavior: When logging out of an instance and into another, the current instance's theme should be used.

 Actual behavior: When logging out of an instance and into another, the first instance's theme is used for the second instance.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

