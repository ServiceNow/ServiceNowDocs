---
title: Mobile Onboarding for iOS v12.2.0
description: The iOS v12.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v12-2-0.html
release: mobile
topic_type: reference
last_updated: "2021-06-17"
reading_time_minutes: 5
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v12.2.0

The iOS v12.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_bfm_hlj_wpb" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1490941

</td><td>

Cabrillo barcode scanning fails and vertical lines appear after clicking the **Show more** button on the catalog item view and the order confirmation screen title shows the catalog item name

</td><td>

 

</td><td>

1.  Open any catalog item on the Now Mobile app.
2.  Click the **Show more** button.

Vertical lines appear on the left side of the description.

3.  Click the **Order Now** button.

 Instead of showing an order confirmation, the screen title shows the catalog item name.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1498807

 [KB0963014](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963014)

</td><td>

Enabling and disabling notifications in the Agent mobile app causes performance instability in the iOS app

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1498663

</td><td>

Activity Stream on the Agent mobile app does not populate activities correctly when a record has many activities on iOS devices

</td><td>

When users compare the time and updates with the browser version, they notice that they do not display the correct updates at the correct time.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1498475

</td><td>

Unable to upload images in iOS

</td><td>

Users are unable to upload images in iOS while using an attachment type variable.

</td><td>

1.  Navigate to 'Create Incident Record Producer'.
2.  Create a variable under the variables related list with the type set to attachment.
3.  Log in to Now Mobile app and find the 'Create incident' item under 'Services'.
4.  Try adding an image in the attachment variable from step 2 by clicking a photo or attaching it from the device.
5.  Complete the other mandatory variables and try to submit the record.

 Expected behavior: The attachment should appear under the variable and the record should be submitted.

 Actual behavior: The attachment details do not appear under the attachment variable. The form cannot be submitted and shows the error 'Please fix errors and try again'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1497443

 [KB0961831](https://hi.service-now.com/kb_view.do?sysparm_article=KB0961831)

</td><td>

iOS fails to impersonate a user when the 'user' value is null in response

</td><td>

Impersonation does not work in the first attempt on iOS devices.

</td><td>

1.  Navigate to the Agent mobile app.
2.  Log in to the instance.
3.  Try to impersonate an itil\_test user.

 Expected behavior: It should pass in the first attempt.

 Actual behavior: It fails on the first attempt.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1492614

</td><td>

Sending an email to customer support in Virtual Agent Lite has a double slash, which causes performance issues on iOS devices

</td><td>

When users click **Send email to customer support** from Virtual Agent on an iOS device, they see a double slash '//' before the email ID. This causes performance issues and the user is unable to send emails.

</td><td>

1.  Install Virtual Agent Lite \(com.glide.cs.chatbot.lite\) and ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\).
2.  Create a quick action menu to initiate Virtual Agent in the mobile app.
3.  Open Virtual Agent.
4.  Click the three dots at the top.
5.  Select **Send Email to Customer support**.

A window for writing an email opens.


 Expected behavior: The '//' should not appear before the email address.

 Actual behavior: Notice that in the **To** field, it has a double slash.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1489751

</td><td>

Unable to turn on offline mode

</td><td>

Field Service Agent is unable to turn on offline mode.

</td><td>

1.  Navigate to **More** &gt; **Settings** &gt; **Offline** &gt; **Update Cache**.

Notice that the cache downloads, but you are still in online mode.

2.  Put your device on airplane mode.
3.  Turn off your WiFi.
4.  Try to set 'Offline Mode' to true.

 Notice that you are not able to turn on offline mode.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1489210

 [KB0959504](https://hi.service-now.com/kb_view.do?sysparm_article=KB0959504)

</td><td>

Unable to impersonate a user in the mobile app if the user ID contains '\\'

</td><td>

Users observe the error 'Impersonation failed, Please try again'.

</td><td>

1.  Change the user ID of a user to a value that contains '\\'.

For example, change 'abel.tuter' to '\\abel.tuter'.

2.  Log in as an admin on a device with the latest mobile apps.
3.  Impersonate Abel Tuter in the Now Mobile or Agent mobile apps.

Observe the error 'Impersonation failed, Please try again'.


 Expected behavior: You are able to impersonate the user.

 Actual behavior: You are unable to impersonate the user and you receive an error.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1488645

</td><td>

In the case of more than one message, HTML tags are escaped so that the message text incorrectly shows tags and HTML formatting

</td><td>

If there is only one message, the tags are formatted in the message and show the correct string on the banner. If there is more than one message, the message text incorrectly shows the tags and HTML formatting.

</td><td>

Create a business rule to show two messages, or update a scripted action that returns two messages.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1486546

 [KB0959343](https://hi.service-now.com/kb_view.do?sysparm_article=KB0959343)

</td><td>

Videos start from the beginning when the orientation is changed in iOS devices

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1485347

</td><td>

iOS does not output any message and clears the spinner after an attempt to upload fails

</td><td>

On an Android device, the app outputs a generic message like 'Fail to Upload', while iOS doesn't output any message.

</td><td>

1.  Log in to the Now Mobile app.
2.  On the instance, create a business rule to prevent an attachment.
3.  Run the app by navigating to the 'Services' tab and add an attachment \(for example, a file or photo\).

 Due to the business rule, the attachment fails. iOS does not display a message, and clears the spinner.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1482090

</td><td>

On the 'Details' screen, the HTML code is not recognized in the **Additional comments** field

</td><td>

The HTML code is displayed between \[code\]...\[/code\]. On the 'Updates' screen and the desktop, the HTML works as expected.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1439926

</td><td>

Time card editing does not work properly in some regions on iOS devices

</td><td>

When users try to edit a time card from the time sheet, it does not allow them when they have the language and regions set to France or Germany. When they set the language and region back to US or India, this works as expected.

</td><td>

1.  Log in to the Now Mobile app.
2.  Open iOS device settings, navigate to **General** &gt; **Language &amp; Region**, and set the iPhone region to France or Germany.
3.  Navigate to the time sheet ALP.
4.  Open the time sheet and click the time card.
5.  Try to edit the hours in edit mode.

 Expected behavior: Editing should work as expected.

 Actual behavior: The **Edit** button does not respond.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

