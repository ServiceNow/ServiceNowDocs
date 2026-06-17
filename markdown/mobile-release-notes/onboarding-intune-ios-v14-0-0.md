---
title: ServiceNow Onboarding - Intune for iOS v14.0.0
description: The iOS v14.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2022-04-07"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v14.0.0

The iOS v14.0.0 release provides fixes for the application.

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

 PRB1546913

</td><td>

Images do not appear at the top of the screen

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1551265

</td><td>

On some devices, images and videos are not displayed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1534310

</td><td>

UI rule error when opening the parameter screen

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to the 'Services' tab.
3.  Select any option under 'Make a Reservation' \(for example **Desks** or **Meeting Room**\).

 Expected behavior: The parameter screen opens and the user can input values.

 Actual behavior: Frequently, the user sees an error message that says 'UI rule error....'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1547210

</td><td>

The Now Mobile media section headlines do not have headers for VoiceOver access

</td><td>

When Now Mobile media sections are viewed with VoiceOver on iOS, the headlines \(for example, 'Services'\) lack headers. The call out will only say the title 'Services', when it should say 'Services heading' as it does for other sections on the screen. As a result, users may have difficulty skimming and navigating to locations on the screen because the navigation commands used to navigate by heading with screen readers are not available.

</td><td>

1.  Configure the Now Mobile app to connect to the instance.
2.  Set up the VoiceOver functionality on the iOS mobile device.
3.  Ensure that the system application is set to 'ServiceNow NowMobile App – Catalog Screens' and 'Applet Launcher/Service Catalog for Mobile'.
4.  Enter sys\_sg\_section.list in the filter navigator.
5.  In the mobile sections list, click **New**.
6.  In the 'Select' section, enter the pop-up, select the 'Media' section, and click **OK**.
7.  Complete the form with test data \(for example 'Services Media Section' for the title, 'Services' for the headline, and drag a random image attachment to the form\) and select it in the **Image** field.
8.  Save the forms.
9.  Navigate to **System Mobile** &gt; **Applet Launchers/Launcher Screens**.
10. Select **Services** in the list.
11. Click **Insert a New Row** under 'Applet Launcher Sections'/'Launcher section mappings'.
12. Set an order of 5 and the UI section to the value you entered as the title in step 7 and save the record.
13. Log in to the instance in the Now Mobile app and enable VoiceOver in iOS.
14. Select the 'Services' icon.
15. Select the 'Services' text and observe the call out.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1548891

</td><td>

Screen parameters are not submitted in the request body of the 'writeback' action configured for the details screen of the form screen

</td><td>

 

</td><td>

1.  Create a list screen with a screen parameter \(the data item for the screen should use the screen parameter\).
2.  Add a form screen to the list screen.
3.  Add a details screen to the form screen.
4.  Configure a 'writeback' action button to the details screen from the previous step.

 When the 'writeback' action is sent via the /writeback REST API, the request does not include the screen parameter field.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1556279

</td><td>

The **Mark as complete** button is not enabled for HR task type - URL

</td><td>

 

</td><td>

1.  Create an onboarding case for a new hire.
2.  Open the onboarding case in the platform.
3.  Click **Add task** in the related links.
4.  Set HR task type to 'URL', URL to 'Youtube url link', and the short description to 'Watch servicenow demo'.
5.  Assign a task to the new hire.
6.  Log in to the Now Mobile app as the new hire.
7.  Navigate to 'My Requests' and open HR tasks.
8.  Click the URL link.

 Notice that the **Mark as complete** button is not enabled.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

