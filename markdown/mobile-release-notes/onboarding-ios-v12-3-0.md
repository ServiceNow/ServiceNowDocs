---
title: Mobile Onboarding for iOS v12.3.0
description: The iOS v12.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-07-22"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v12.3.0

The iOS v12.3.0 release provides fixes for the application.

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

 PRB1497816

</td><td>

VoiceOver does not announce the name for 'Caller' or the role for the 'Location-NO WORKSPACE' controls

</td><td>

This issue occurs for similar controls throughout the application.

</td><td>

1.  Install the ServiceNow Agent application on the device.
2.  Enable VoiceOver and open the Agent app.
3.  Log in to the app.
4.  Navigate to the 'Major incident' tab and activate it.

The 'EUSE Mobile' screen appears.

5.  Navigate to the 'My incident' control and activate it.
6.  On the 'My incident' screen, Activate the **...** button.
7.  Navigate to the **New** button and activate it.
8.  Complete the mandatory fields and activate the **Submit** button.

The incident is created.

9.  Navigate to the 'EUSE Mobile' tab and activate it.
10. Navigate to the **My Group's incident** button and activate it.
11. Navigate to the created incident and activate it.
12. Activate any ticket that appears.
13. Navigate to 'Call' control and the 'Location-NO WORKSPACE' control using swipe gestures.

 Expected behavior: VoiceOver announces the name for the 'Caller' control or the role for the 'Location-NO WORKSPACE' control.

 Actual behavior: VoiceOver does not announce the name for the 'Caller' control or the role for the 'Location-NO WORKSPACE' control.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1463093

</td><td>

VoiceOver does not announce a confirmation message after activating the 'Cancel' control

</td><td>

As a result, users do not receive the information about the action performed by activating the **Clear** button.

</td><td>

1.  Launch the Agent app.
2.  Select **Try with a demo account** &gt; **Service Desk** &gt; **Agent Launch Demo**.
3.  Next to 'My Incidents', select **See All**.
4.  Turn on VoiceOver.
5.  Double tap the filter icon.
6.  Enter any search criteria.

This activates the **Clear** button.

7.  Double tap the **Cancel** button.

 Expected behavior: VoiceOver should announce 'Cleared successfully'.

 Actual behavior: The entries you made are cleared and the **Clear** button becomes inactive, but no status message is read by VoiceOver.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1472419

</td><td>

While chatting with a live agent, the chat font on the mobile application is lighter than other fonts

</td><td>

When Virtual Agent opens on the mobile app and a chat with a live agent starts, the chat's font color is light.

</td><td>

1.  Navigate to Virtual Agent on the mobile app.
2.  Start a chat with a live agent.

 Observe the font of the chat in comparison to other chat fonts.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1497693

 [KB0962876](https://hi.service-now.com/kb_view.do?sysparm_article=KB0962876)

</td><td>

The Agent mobile app does not clear the **Assigned to** field when reassigning an incident if the assignment group dictionary reference qualifier condition uses 'contains'

</td><td>

When attempting to use the base instance 'Reassign' option to reassign an incident to a different assignment group on the iOS Agent mobile app, the **Assigned to** field is not cleared if the assignment group dictionary reference qualifier condition uses a 'contains' condition.

</td><td>

1.  Log in to a base instance.
2.  Open the dictionary record for the **Assignment group** field on the task table and update the reference qualifier condition to 'Type contains Catalog', for example.
3.  Log in to the Agent mobile app on an iOS device and open any incident record where the **Assignment group** and **Assigned to** fields are populated.
4.  Click the **…** option and choose 'Reassign'.
5.  In the **Assignment group** field, choose another group.

 Notice that the **Assigned to** field is not cleared.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1498921

</td><td>

Mobile Publishing iOS splash screen icons are stretched

</td><td>

If users upload high-quality icons, they may appear pixelated on an iOS device.

</td><td>

1.  Download the Mobile Publishing scoped app.
2.  Submit a Mobile Publishing application request for iOS with high-quality images.

 Expected behavior: The icons should appear in focus.

 Actual behavior: Notice that the splash screen is stretched to fit the screen horizontally.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1504770

</td><td>

Voiceover does not properly announce the confirmation message after activating the **Clear** control

</td><td>

On iOS devices, users do not receive proper feedback about the action performed by activating the **Clear** button.

</td><td>

1.  Enable VoiceOver on the iOS device.
2.  Launch the Agent app.
3.  Select **Try with a demo account**.
4.  Select **Service Desk Agent**.
5.  Select **Launch Demo**.
6.  Next to 'My Incidents', select **See All**.
7.  Double tap the filter icon.
8.  Enter any search criteria.
9.  Double tap the **Clear** button.

 Expected behavior: VoiceOver announces 'Cleared Successfully', as it does on Android devices.

 Actual behavior: The entries you made are cleared, and the **Clear** button becomes inactive. VoiceOver announces 'Clear'.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

