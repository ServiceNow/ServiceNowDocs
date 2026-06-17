---
title: ServiceNow Onboarding - Intune for iOS v13.0.0
description: The iOS v13.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-10-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v13.0.0

The iOS v13.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

 PRB1522575

 [KB0996063](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0996063)

</td><td>

The attachment variable does not upload attachments

</td><td>

In the iOS Now Mobile app, the attachment variable type no longer adds the attachment. The app appears like it's going to attach, but nothing happens. The mandatory flag is not fulfilled and no attachment title displays.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1512451

</td><td>

Impersonation does not work on iOS BlackBerry

</td><td>

 

</td><td>

1.  Download the latest Blackberry release for iOS.
2.  Log in as an admin user.
3.  Navigate to settings and select the profile icon.
4.  Select a user to impersonate.

 Notice that after selecting the user, you still remain the admin user.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1513908

</td><td>

Dependent fields do not work as expected

</td><td>

The **Subcategory** field is not cleared after changing the category in iOS mobile apps.

</td><td>

1.  Install the ITSM Mobile \(com.sn\_itsm\_mobile\) plugin.
2.  Use the iOS Agent mobile app on iOS to log in to the instance.
3.  Click the 'Incidents' applet launcher.
4.  Under the 'All Incidents' section, click the 'Incidents' applet and select any incident record.
5.  Click the top menu **Edit** function and select any value for the **Category** \(for example, Software\) and **Subcategory** \(for example, Email\) UI parameters.
6.  Remove the category by selecting '--none--' or change the category from 'Software' to any other value.

 Expected behavior: **Subcategory** should be reset to 'none' because it is dependent on **Category**, which has been changed.

 Actual behavior: The **Subcategory** value is not reset.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1522846

</td><td>

Unable to send or receive messages on Virtual Agent on BlackBerry

</td><td>

 

</td><td>

1.  Log in to an instance that has Virtual Agent set up.
2.  Open Virtual Agent.
3.  Send a message.
4.  Close Virtual Agent by selecting the **Done** button in the navigation bar.
5.  Open Virtual Agent.
6.  Attempt to send a message.

 The message fails to send and you do not receive a response from the Virtual Agent.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

