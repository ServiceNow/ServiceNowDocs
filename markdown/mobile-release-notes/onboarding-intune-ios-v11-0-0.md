---
title: ServiceNow Onboarding - Intune for iOS v11.0.0
description: The iOS v11.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2020-10-22"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v11.0.0

The iOS v11.0.0 release provides fixes for the application.

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

 PRB1431037

</td><td>

The landscape orientation crashes the app in iOS 14 when an ALP screen is visible

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1421259

</td><td>

In the form with the embedded list screen segment, when performing the delete action on the list screen, the item is not removed automatically

</td><td>

 

</td><td>

1.  Open the mobile app and log in to the instance.
2.  Tap the **Mobile Regression** tab, and scroll to the 'Simple Applets' section.
3.  Tap the 'MAP' applet.
4.  Tap the item card, and then tap '...'.
5.  In the pop-up list, tap 'Incidents - List'.
6.  Swipe right on the list and tap '...' to delete this record.

 Expected behavior: The item should be removed from the list automatically.

 Actual behavior: The item is not removed from the list until you manually refresh the form.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1430845

</td><td>

Issues with the **Hide when empty** field on the UI Section form

</td><td>

 

</td><td>

1.  Navigate to Mobile Studio and open any Application Launcher.
2.  Open any UI Section.
3.  Remove all the applets if they are present in the UI Section.
4.  Select the 'Hide when empty' checkbox.
5.  Observe the behavior in Mobile.

Notice that the UI Section is not visible.

6.  Add some applets in the UI Section.
7.  Observe the behavior in Mobile.

Notice that the UI Section is not visible.

8.  Remove all the applets present in the UI Section again.
9.  Uncheck the 'Hide when empty' checkbox.
10. Observe the behavior in Mobile.

Notice that the UI Section is not visible.

11. Add some applets in the UI Section.
12. Observe the behavior in Mobile.

 Notice that the UI Section is visible with applets. The 'Hide when empty' checkbox has a faulty and improper behavior in iOS.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1424207

</td><td>

Cabrillo API attachment issues on iPhone

</td><td>

The cabrillo.attachments. viewFile\(\) function is not working as expected in iOS devices.

</td><td>

1.  Create a widget that has a button **Download PDF** using cabrillo. attachments.viewFile.
2.  Add the above widget to a page.
3.  Create a URL type of applet which redirects to the above page.
4.  Log in to the instance from an iPhone.
5.  Navigate to the URL applet.

This will redirect to a portal page.

6.  Click the button **Download PDF**.

 This will work for the first time, but the button won't work from the second click.

</td></tr></tbody>
</table>This version also contains the following updates:

-   Updated designs for Activity Stream screens.
-   Enhanced pull to refresh applet launcher experience by having the clients receive all the latest metadata and allowing to always receive the latest without having to re-login.
-   Added the **Dismiss** button to message banners.
-   Added the Debug mode.
-   Other performance improvements and minor bug fixes.

**Note:** iOS 13 will be the minimum supported version.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

