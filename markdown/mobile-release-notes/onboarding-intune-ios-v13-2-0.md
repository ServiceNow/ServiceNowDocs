---
title: ServiceNow Onboarding - Intune for iOS v13.2.0
description: The iOS v13.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-12-16"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v13.2.0

The iOS v13.2.0 release provides fixes for the application.

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

 PRB1472706

 [KB0952195](https://hi.service-now.com/kb_view.do?sysparm_article=KB0952195)

</td><td>

The system property 'glide.sg.block\_mobile \_attachments\_sharing' does not work on mobile apps

</td><td>

Setting the system property 'glide.sg.clear\_pasteboard\_ when\_backgrounded' to true hides the **Share** button only for images. Users can still see the **Share** button for documents and PDFs.

</td><td>

1.  Create an incident on the standard platform.
2.  Update an image, a doc, and a pef file as attachments to the incident.
3.  Access the incident on the Now Mobile app.
4.  Click to view the attachment on the activity screen.

Notice the **Share** button.

5.  Set the system property glide.sg.block\_ mobile\_attachments\_sharing to true.
6.  Wait to flush the instance cache to not affect connected users.
7.  Access the incident on the Now Mobile app.
8.  View the attachment on the activity screen again.

 The attachment sharing button is still available.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1492373

</td><td>

The UI parameter screen actions are not translated

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Select the Japanese language.
3.  On the homepage, click **Requests**.
4.  Click the **Add comment card** action.

 The UI parameter screen is not translated.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1524110

</td><td>

VoiceOver does not announce the new number of filtered services displayed

</td><td>

After activating the **Apply** button to apply a filter, the list of services shown on the screen may update to show different services. Currently, the only way users are aware of this new content is through exploratory touch and the standard swipe gesture navigation.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1525653

</td><td>

The Now Mobile app **Comment** button and decorative icon are indicated as a heading

</td><td>

Within the Now Mobile app, the decorative initial icon and **Comment** button text elements are unnecessarily implemented as a heading.

</td><td>

1.  On an iOS mobile device, activate VoiceOver as a user without an image.
2.  Open any ticket and navigate to the comments screen.
3.  Scroll through the UI.

 Notice that the lettered icon for the user is on the list and described as a heading. Also notice that the **Comment** field itself is described as a heading.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1532800

</td><td>

Empty state text does not wrap in mobile apps for iPhones

</td><td>

When there is a long empty state text \(max value 100 characters\) for a list applet, it does not wrap properly on iPhones. An iPad is large enough, and this works properly for Android.

</td><td>

1.  Create an applet with a data item that returns no records.
2.  Integrate into any specific applet launcher.
3.  Set the empty state for the list applet to something long \(max value\) and save.
4.  Authenticate in one of the mobile apps where the applet is loaded on an iPhone.
5.  Navigate to the applet and open it.

 Notice that the empty text extends across the width of the screen and does not wrap.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1533911

</td><td>

Unable to update the label for support options

</td><td>

Updating the label value for default mobile branding is not reflected in mobile.

</td><td>

1.  Log in to any Quebec instance.
2.  Navigate to **Collaboration** &gt; **Branding** and **Chat** &gt; **Menu items**.
3.  Change the label against the chat menu item.
4.  Log in to the Now Mobile application.
5.  Open Virtual Agent and click the chat options.

 Notice that the label updated in step 3 is not reflected.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1536432

</td><td>

The chat icon button does not have an accessible name or label

</td><td>

 

</td><td>

1.  Launch Now Mobile and log in with a demo account.
2.  When the welcome screen loads, launch VoiceOver.
3.  Swipe right to access the Mobile VA **Chat** button.

 Expected behavior: VoiceOver should announce something like 'Chat' and then 'Button'.

 Actual behavior: VoiceOver reads 'Button'.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

