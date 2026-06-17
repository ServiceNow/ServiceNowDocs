---
title: Mobile Onboarding for iOS v12.0.0
description: The iOS v12.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-04-15"
reading_time_minutes: 6
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v12.0.0

The iOS v12.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_fpy_l5r_2pb" class="custom-rows"><thead><tr><th class="filter">

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

</td><td>

The system property 'glide.sg. block\_mobile \_attachments\_sharing' does not work on Mobile apps

</td><td>

Setting the system property 'glide.sg.clear\_pasteboard \_when\_backgrounded' to true hides the **Share** button only for images. Users can still see the **Share** button for documents and PDFs.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1456296

</td><td>

Unable to tap into search bar after refreshing

</td><td>

This issue is observed in instances that have search configured.

</td><td>

1.  Open a page that has a search bar.
2.  Pull to refresh.
3.  Tap the search bar.

 Expected behavior: The search bar becomes the first responder.

 Actual behavior: The search bar does not become the first responder.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1476047

</td><td>

VoiceOver does not announce the state as expanded or collapsed for the 'Search' control present in the 'Number' screen

</td><td>

 

</td><td>

1.  Install the ServiceNow Agent app.
2.  Launch the app and tap **Try with a Demo Account**.
3.  Select any incident and open it.
4.  Select the 3-button vertical menu, then tap **Edit**.
5.  Turn on VoiceOver.
6.  Swipe right until a category is selected that has a search component \(for example, Inquiry/Help or Assignment Group\) and double tap.
7.  Swipe right again until the **Search** button is highlighted and double tap it to expand and search.

 Expected behavior: VoiceOver should announce 'Search, button, expanded. Editing'.

 Actual behavior: VoiceOver announces 'Search, button', then 'Editing \(with additional info\)'. VoiceOver should also announce when the search field is collapsed.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1476037

</td><td>

In iOS, selecting 'None' for a UI parameter is accepted as fulfilling the mandatory requirement and allows submission of the function

</td><td>

 

</td><td>

1.  Create a screen UI policy that sets **Assignment Group** and **Assigned To** as mandatory if they are both empty.
2.  Log in to the ServiceNow Agent app.
3.  Open an incident record and choose the **Edit** action.

Notice that **Assignment Group** and **Assigned To**are mandatory.

4.  Select 'None' for both of these fields.
5.  Log in as another user.
6.  Open an incident from the 'Incidents' tab.
7.  Tap the 3 dots and select **Edit**.

You should see **Assignment Group** and **Assigned To** are mandatory.

8.  Select 'None' for either of the fields.

 Expected behavior: On Android, 'None' does not satisfy the 'Mandatory' requirement and does not allow submission.

 Actual behavior: On iOS, 'None' allows submission, regardless of the field being mandatory.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1472549

</td><td>

VoiceOver moves to a hidden element when opening a search screen from the 'Filter' control

</td><td>

 

</td><td>

1.  Launch the Agent app and sign in with an ITIL user account.
2.  Navigate to 'My Work' and tap **See All** next to 'My Incidents'.
3.  Turn on VoiceOver.
4.  Double tap the filter icon.

 Notice that focus is somewhere above the screen, and VoiceOver announces 'double tap to dismiss pop-up button'. There should be no hidden pop-up and the focus should move to 'Cancel' when the screen loads.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1472344

</td><td>

VoiceOver focus takes an extra swipe on the **Location NO WORKSPACE** button

</td><td>

The issue is related to an extra tab stop to the entries within the **Description/Caller**, **Category**, and **Sub-Category** fields.

</td><td>

1.  Launch the Agent app.
2.  Select **Try with a demo account** &gt; **Service Desk Agent** &gt; **Launch Demo**.
3.  Select any incident under 'My Incidents'.
4.  Turn on VoiceOver.
5.  Swipe right to scroll through the **Details** fields.

 Expected behavior: Focus should only be on the field itself.

 Actual behavior: There is an extra tab stop for the entries on the details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1463093

</td><td>

VoiceOver does not announce a confirmation message after activating the 'Cancel' control

</td><td>

As a result, users do not get the information about the action performed by activating the **Clear** button.

</td><td>

1.  Launch the Agent app.
2.  Select **Try with a demo account** &gt; **Service Desk** &gt; **Agent Launch Demo**.
3.  Next to 'My Incidents', tap **See All**.
4.  Turn on VoiceOver.
5.  Double tap the filter icon.
6.  Enter any search criteria.

This activates the **Clear** button.

7.  Double tap the **Cancel** button.

 Expected behavior: VoiceOver should announce 'Cleared Successfully'.

 Actual behavior: The entries you made will clear and the **Clear** button becomes inactive, but no status message is read by VoiceOver.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1462803

</td><td>

VoiceOver does not announce the count or position of search results that appear after entering text in the **Search** edit field

</td><td>

 

</td><td>

1.  Install the ServiceNow Agent app.
2.  Launch 'Try with a Demo'.
3.  Select **Service Desk Agent**, then select **Launch Demo**.
4.  Turn on VoiceOver.
5.  Tap the 3-button menu and select **Create an Incident**.
6.  Swipe left until 'Required Field Caller button' is announced and highlighted, and double tap.
7.  Enter a search parameter and double tap **Search**.
8.  Swipe left until the focus is on the results list and swipe left to highlight each returned item.

 VoiceOver announces each selection as you swipe through the results, but the number and position are not announced.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1458374

</td><td>

Item view shows a duplicate 'requested for'

</td><td>

When using the item view, in the 'My To-Dos' section, users observe a duplicated entry for 'requested for'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1477830

</td><td>

The **Close** button on the order confirmation page is not responsive

</td><td>

 

</td><td>

1.  Log in on Now Mobile app as an ITIL user.
2.  Under Browse Service, click **Hardware** and select any item.
3.  Select details like quantity or color, and include an attachment picture.
4.  Select **Order Now** &gt; **Checkout**.
5.  After the order is placed, verify that the 'Thank you! Your Request has been submitted' message is displayed.
6.  Tap the **Close** button, which should navigate the user back to the Services page.

 The **Close** button doesn't respond.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1479273

</td><td>

Luminosity contrast ratio for arrow is 1.9:1, which is less than 3:1

</td><td>

 

</td><td>

1.  Access the Agent Mobile app on iOS.
2.  Log in to the instance.
3.  Navigate to the settings.

 Expected behavior: The luminosity contrast ratio for the settings arrow is less than 3:1.

 Actual behavior: The luminosity contrast ratio for the settings arrow contrast ratio is 1.9:1.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1482685

</td><td>

'You do not have any notifications at this time' is not translated in iOS

</td><td>

The 'You do not have any notifications at this time' message is not translated in iOS for the Now Mobile and Agent Mobile apps.

</td><td>

1.  Change the iOS device language to Spanish.
2.  Log in to the Mobile Agent app on any instance.
3.  Tap **More** in the bottom right.
4.  Select **Notifications**.

 Expected behavior: The 'You do not have any notifications at this time' text should be in Spanish. This works correctly in the Android apps.

 Actual behavior: The 'You do not have any notifications at this time' text is still in English.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1363425

</td><td>

When accessing a certain instances from off the corporate network, an error page shows in HTML

</td><td>

When a user signs in to the app in their office on the corporate network, it works as expected. If the user leaves the office and opens the app again, an error appears.

</td><td>

1.  Sign in to a Now Mobile app on network.
2.  Disconnect from the corporate network.
3.  Access the app again.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1485296

</td><td>

Mobile iOS Intune authentication does not work with an Edge browser

</td><td>

The 'IntuneMAM Configurator' script is not applied to Intune builds, causing Intune apps to not work properly.

</td><td>

1.  Log in to any Intune app \(NowMobile Intune, Agent Intune, or Onboarding Intune\).
2.  Make sure Edge is the browser set for authentication.
3.  Attempt to log in.

 Expected behavior: Edge should redirect to the app and show the homepage.

 Actual behavior: Edge does not redirect to the mobile app after the login flow is completed, and shows a black screen or launches in the device web browser.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1486387

</td><td>

Verify scroll on the popular articles UI

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

