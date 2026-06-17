---
title: Mobile Onboarding for iOS v10.0.4
description: The iOS v10.0.4 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v10-0-4.html
release: mobile
topic_type: reference
last_updated: "2020-06-18"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v10.0.4

The iOS v10.0.4 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

 PRB1404651

</td><td>

The function action with only 1 UI parameter and eventually 1 writeback parameter in the action item does not work correctly

</td><td>

The function action with only 1 UI parameter and eventually 1 writeback parameter in the action item does not work correctly. The writeback is occurring even before the submit action on the UI parameter.

</td><td>

1.  In Studio, navigate to the action Reassign Incident.
2.  Remove the other two UI parameters \(and hence action parameter mapping\), and only keep Assignment group.
3.  Navigate to the action item Reassign\_Incident \_WB.
4.  In **Item parameters** &gt; **Writeback**, keep 'Reassign\_Incident\_ Assignment\_Group\_IP' and remove the rest.
5.  In the same action item, use type as update, and under Set field values, set the Assignment group parameter and also set the Caller field to any value \(for example, Abel Tuter\).
6.  In the mobile app, navigate to the Active Incidents applet.
7.  Swipe right and find the Reassign function.

On the action screen for Reassign, notice that the success message is shown even though the user hasn't tapped on the **Submit** button.

8.  Cancel and come back to the Applet list.

 Notice that the caller is now updated to Abel Tuter.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1407407

</td><td>

When there is a duplicated applet in icon section in ALP, the app crashes

</td><td>

The crash happens only on iOS 13.

</td><td>

 

</td></tr></tbody>
</table>This version also includes the following updates:

-   Mobile push notification enablement toggle will now appear in the notification preferences section in the settings tab.
-   UI improvements, performance improvements, and other minor bug fixes.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

