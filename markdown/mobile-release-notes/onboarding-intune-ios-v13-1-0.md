---
title: ServiceNow Onboarding - Intune for iOS v13.1.0
description: The iOS v13.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v13-1-0.html
release: mobile
topic_type: reference
last_updated: "2021-11-18"
reading_time_minutes: 4
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v13.1.0

The iOS v13.1.0 release provides fixes for the application.

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

 PRB1522083

</td><td>

Users are not notified of search auto-complete changes in VoiceOver

</td><td>

 

</td><td>

1.  Activate VoiceOver.
2.  Open the Now app.
3.  Connect to your instance.
4.  Navigate to the search.

Observe that there is not a spoken indicator for the suggestions when you type something.


 Expected behavior: VoiceOver users must be notified if and when auto-complete suggestions are provided within the search.

 Actual behavior: VoiceOver users are not notified if or when auto-complete suggestions are provided within the search.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1483955

</td><td>

Larger text is not applied to an activity, related list, or filter

</td><td>

 

</td><td>

1.  Install the ServiceNow Agent application on the device.
2.  Navigate to **Settings** &gt; **Accessibility** &gt; **Display &amp; Text size** &gt; **Larger text**.
3.  Keep the toggle in the 'Off' state and slide the slider to 'Max'.
4.  Open the Agent mobile app with a demo account.
5.  Navigate to 'Service agent' and any incident 'Activity stream' and 'Related list'.

Elements under the 'Activity stream' and 'Related list' tab in the 'My incidents' page does not adopt the larger text font.

6.  Navigate to **My work** &gt; **My incidents** &gt; **See all** &gt; **Filter**.

 The 'Filter' screen does not adopt the larger text font.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1511994

</td><td>

Live agent chat in the Now Mobile app shows the Virtual Agent icon for the user icon, even when a live agent is sending the messages

</td><td>

This may be confusing for users as it is impossible to tell if they are communicating with the Virtual Agent or a Live Agent.

</td><td>

1.  In the desktop UI, log in to the instance and impersonate beth.anglin.
2.  Open Agent Workspace Home from the navigator.
3.  In the 'Inbox' tab, set the status as 'Available'.
4.  In the Now Mobile app for iOS, log in to the instance.
5.  In the 'My Items' tab, tap the chat quick action button.
6.  In the desktop UI, accept the incoming chat with beth.anglin and send a message.

 Expected behavior: There should be some indication in the avatar/icon that the user is now talking to a live agent.

 Actual behavior: The same 'now' Virtual Agent icon appears regardless of whether the VA bot is sending messages or a live agent.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1518983

</td><td>

The DateTime UI parameter updates the value in the field on iOS devices

</td><td>

 

</td><td>

1.  Log in into the instance on the desktop.
2.  Create a date/time type field on the incident table.
3.  Populate the value in the field for one of the records.
4.  Create a list applet on the incident table.
5.  Add the **Short description** and **DateTime** field created in step 2 to the applet.
6.  Add the applet to a section in the Agent mobile app.
7.  Create a function to edit the **Short Description** and **DateTime** field.
8.  Log in to the instance on the Agent app using an iOS device.
9.  Navigate to the applet created in step 4.
10. Open any incident record where **DateTime** is not empty.
11. Try updating the value in the **Short description** field.

 Expected behavior: The value in the **DateTime** field should remain as-is.

 Actual behavior: Notice that the value in the **DateTime** field is also updated.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1522079

</td><td>

**Share**, **Edit**, and **Trash** have an icon in their label

</td><td>

 

</td><td>

1.  Open the Now app.
2.  Connect to your instance.
3.  Open an incident.
4.  Click **Attachment**.

Observe that **Edit** has the announcement 'icon edit, button' and **Trash** has the announcement 'trash icon, button'.


 Expected behavior: VoiceOver users do not need to receive an announcement for each object as an icon button.

 Actual behavior: VoiceOver users notice an announcement for each object as an icon button.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1522850

</td><td>

For Virtual Agent on mobile, the second date input does not capture the date

</td><td>

 

</td><td>

1.  Log in to Now Mobile.
2.  Open **Quick Action** &gt; **Chat with Virtual Agent**.
3.  Select the leave of absence topic.

 Expected behavior: Virtual Agent on iOS Now Mobile should be able to accept two date inputs.

 Actual behavior: The topic asks for the leave of absence start date and end date. The start date appears as expected, but the end date does not. It is also not captured in the input variable.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1523908

</td><td>

The 'Price' container within a filter screen is accessible

</td><td>

The 'Price' container receives focus and all content within this container is announced.

</td><td>

1.  Start VoiceOver.
2.  In the mobile app, navigate to the 'Information' tab.
3.  Select any category.
4.  Move input focus to the **Filter** button and select it to invoke the filter.

The count control on this page is the **View count** field, but it is the same control as the price control.

5.  Move input focus to either the **From** or **To** fields.

 Notice that the labels are not associated to the fields.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1535054

</td><td>

Embedded lists are not showing in Rome

</td><td>

 

</td><td>

1.  Log in to a Rome instance in the Agent mobile app.
2.  Navigate to the **My Work** &gt; **All Incidents** &gt; **Open Incident**.

Observe that there is a record in the embedded list.

3.  Download the cache and enter the offline mode.
4.  Open the same incident record.

 Expected behavior: The embedded lists should be visible in offline mode.

 Actual behavior: The embedded lists are not visible in offline mode.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

