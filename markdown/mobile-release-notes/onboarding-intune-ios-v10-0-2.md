---
title: ServiceNow Onboarding - Intune for iOS v10.0.2
description: The iOS v10.0.2 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v10-0-2.html
release: mobile
topic_type: reference
last_updated: "2020-05-21"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v10.0.2

The iOS v10.0.2 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding-intune/id1494184220). Users can launch a demo to try the ServiceNow Onboarding - Intune app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1397392

</td><td>

The 'Upload images' and 'Signature' parameters on a form are not translated

</td><td>

 

</td><td>

1.  Ensure ITSM Mobile is active.
2.  Navigate to **System Mobile** &gt; **Functions**, and create a new function record:
    -   Name: Create new Incident
    -   Type: Action Item
    -   Context: Global
    -   Action item: create a new action item from the reference pop-up window:
        -   Name: Set Incident Active
        -   Table: Incident
        -   Set field values: Active is True
    -   Allow images upload: true
3.  If needed, switch to the ITSM Mobile application workspace from the drop-down list.
4.  Submit the function.
5.  Navigate to **System Mobile** &gt; **Applet Launchers**, and open the 'Incidents' launcher.
6.  Open the **Body** tab, and under the Quick Actions list, double-click 'Insert a new row...'.
7.  Click the magnifying glass to open the reference pop-up and click **New** to create a new function instance:
    -   Name: Create New Incident
    -   Parent: use the modal pop-up to define a reference to the 'Incidents' Applet Launcher \[sys\_sg\_applet\_launcher\]
    -   Parent Table: Incident
    -   Function: Create New Incident
    -   Label: Click here
    -   Location: Quick Action
    -   Icon: anything would work
8.  Ensure the new function instance is linked to the Applet Launcher.
9.  Activate any language plugin.
10. In Agent mobile, log in as the ITIL user, and change the language from the login page to the language plugin you just activated.
11. Tap Quick Action at the bottom-right corner of the screen.

 Notice that in the form that appears, the parameter 'Upload Images' is not translated. The same can be seen for the 'Signature' parameter if 'Show signature field' is checked as true in the function record.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1399396

</td><td>

Navigating to the list from the report in ALP is not working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1401255

</td><td>

The redirection push notification does not work if the app is blurred when backgrounded

</td><td>

 

</td><td>

1.  Set glide.sg.blur\_ui\_when\_ backgrounded to true on the instance.
2.  Send a push notification that will direct the user to somewhere in the app.

 Notice that when the user taps the push notification, it will foreground the app but will not direct the user to anywhere.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1403756

</td><td>

Push notifications of one instance are getting triggered on another instance if users log out immediately and log in again on mobile apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Request - iOS

 PRB1399752

</td><td>

The current date/time does not show up in the date field until the date picker is changed

</td><td>

The date field is not populated with the current date/time after opening and closing the date picker. The date/time shows up in the date field only after the date picker is changed.

</td><td>

1.  Open a date time picker in an iOS app.
2.  Close the picker in order to choose the current date and time.

 Expected behavior: The current date/time is set in the date field.

 Actual behavior: Nothing happens. However, if you choose a time or date other than what is currently in the picker, the date/time is set in the date field.

</td></tr></tbody>
</table>This version also improves user experience when opening a single parameter, and includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

