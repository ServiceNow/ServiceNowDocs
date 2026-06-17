---
title: Mobile Onboarding for Android v11.0.0
description: The Android v11.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2020-10-22"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v11.0.0

The Android v11.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android \(non-classic\)

 PRB1421354

</td><td>

The signature is not captured after rotating the orientation of the screen

</td><td>

 

</td><td>

1.  In the app, navigate to the **My task** tab.
2.  Open any task, and move the task from any state to 'Close complete' by clicking **Close Complete**.
3.  Click the **Signature** field to enter the signature.
4.  Try changing the screen orientation without clicking anything.

 Notice that the signature just entered disappears after changing the screen orientation.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1424495

</td><td>

The decimal field displays incorrectly on the mobile action function on Android devices

</td><td>

Users are unable to update decimal fields for numbers greater than 7 digits using the mobile action. Long numbers don't appear correctly in the UI parameter in the mobile app. For example, if the value is 1,375,316,476, it shows as 1.375316476E9. Also, the app stops working when trying to edit the value.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1431702

</td><td>

The instance is not redirecting to the SSO login page after the session timeout on Android devices

</td><td>

The SSO redirection is not working on Android devices after the session timeout. After the session times out, the local login page appears on the screen and it is not redirecting to the SSO login page. Users don't have an option to enter the SSO credentials unless they log out from the app completely.

</td><td>

1.  Install the ITSM Mobile plugin.
2.  Create an applet URL with the URL pointing to /sp.
3.  Configure a new navigation tab for the mobile app.
4.  Configure an ALP for the navigation tab with the applet URL created in Step 2.
5.  Make sure that the navigation tab created in Step 3 is the first tab on the mobile app.
6.  Configure SSO for the instance.
7.  Set the session timeout property glide.ui.session\_timeout to 3 minutes.
8.  On the mobile app, log in to the instance using the SSO credentials with an Android device.

The Service Portal page loads \(/sp URL is configured for the ALP\).

9.  Wait for 3 minutes as the session timeout property glide.ui.session \_timeout is set to 3 minutes.
10. Click **Knowledge Base** or **Request Something**.

 Expected behavior: The page should redirect to the SSO login page.

 Actual behavior: The page redirects to SP local login page and is not redirecting to the SSO login page. It loops through the SP login page.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1434387

</td><td>

Field changes in the Activity Stream that include HTML tags are displayed in plain text

</td><td>

Field changes in the Activity Stream that include HTML tags are displayed in plain text. This is inconsistent with the Activity Stream in Desktop UI.

</td><td>

1.  In Desktop UI, open any incident and set the 'Resolution Notes' to the following:

    ```
[code]<a href='http://www.servicenow.com/support/contact-support.html'>
http://www.servicenow.com/support/contact-support.html</a>[/code]
    ```

2.  View the incident in the mobile app and check the **Activity** tab.

 Notice that in Desktop UI, you will see a clickable hyperlink, but in the mobile app, the HTML is displayed as plain text.

</td></tr></tbody>
</table>This version also contains the following updates:

-   Updated designs for Activity Stream screens.
-   Enhanced pull to refresh applet launcher experience by having the clients receive all the latest metadata and allowing to always receive the latest without having to re-login.
-   Added the **Dismiss** button to message banners.
-   Added the Debug mode.
-   Other performance improvements and minor bug fixes.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

