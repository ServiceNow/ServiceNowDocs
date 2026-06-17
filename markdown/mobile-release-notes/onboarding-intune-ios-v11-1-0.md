---
title: ServiceNow Onboarding - Intune for iOS v11.1.0
description: The iOS v11.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2020-11-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v11.1.0

The iOS v11.1.0 release provides fixes for the application.

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

 PRB1423934

</td><td>

Mobile deep linking does not work

</td><td>

Deep links tapped outside of the app are not redirecting to the actual app.

</td><td>

1.  Log in to the mobile request app as an ITIL user.
2.  Email the device a deep link.
3.  Tap the link.

 Expected behavior: The deep link should open in the app.

 Actual behavior: It attempts to open in the web.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1439722

</td><td>

On clicking the **Show Me Everything** button, instead of displaying the topic names, sys IDs are displayed, along with the **See all** option

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1423568

</td><td>

Dynamic deep links not redirecting to records as expected

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1418078

 [KB0853424](https://support.servicenow.com/kb_view.do?sysparm_article=KB0853424)

</td><td>

The HTML field in the mobile form screen adds an extra scrollbar or creates empty space when the inner content is resized

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1441815

</td><td>

When performing the swipe action, the message '500 - Internal server error' appears in the instance

</td><td>

 

</td><td>

1.  Configure a swipe action that triggers an action on the list screen directly.
2.  Log in to the instance via the mobile app.
3.  Navigate to the list screen applet and try out the swipe action.

 Expected behavior: The swipe action should work on the selected record.

 Actual behavior: The message '500 - Internal server error' is shown.

 **Note:** If you configure a swipe button that opens a new page and the submission happens in the new page, this issue will not happen.

</td></tr></tbody>
</table>This version also contains other performance improvements and minor bug fixes.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

