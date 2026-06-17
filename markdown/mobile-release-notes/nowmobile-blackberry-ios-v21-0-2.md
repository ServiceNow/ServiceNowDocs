---
title: Now Mobile for BlackBerry for iOS v21.0.2
description: The iOS v21.0.2 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-ios-v21-0-2.html
release: mobile
topic_type: reference
last_updated: "2026-03-01"
reading_time_minutes: 2
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for iOS v21.0.2

The iOS v21.0.2 release provides fixes for the application.

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

iOS Mobile

 PRB1993847

</td><td>

Category icons on Now Mobile do not load properly on iOS devices

</td><td>

Item icons appear differently than expected.

</td><td>

1.  Log in to a Now Mobile instance.
2.  Navigate to the 'Services' tab.

Note the Item's icons.

3.  Manually refresh by swiping down from the top of the screen.

 Expected behavior: The icons should be the same between step 2 and step 3.

 Actual behavior: Icons are different between step 2 and step 3.

</td></tr><tr><td>

iOS Mobile

 PRB1992112

</td><td>

Catalog icons are not displayed when the short description is long

</td><td>

Catalog icons should be visible.

</td><td>

Pre-requisite: Service Catalog for mobile plugin is installed. 1.  Open the Agent Mobile app.
2.  Select **Services**.
3.  Select any option from **Browse services**.

Observe that Catalog icons are not displayed when the short description is long.

</td></tr><tr><td>

iOS Mobile

 PRB1968714

</td><td>

The **Set to Ready** option is missing for an IGT task in the Guided Task screen

</td><td>

 

</td><td>

1.  Navigate to the 'Standards' tab.
2.  Select any standard present in the list.

This will open request task page.

3.  Select the **Submit** button.
4.  On the Guided Task screen, open the three dots menu icon.
5.  Select **Put on Hold**.

Notice that the state of the task changes to 'On hold'.

6.  Select the three dots menu icon again.
7.  Verify the option 'Set to Ready'.

 Expected behavior: The 'Set to Ready' option should be available in the three dots menu when the task is in an 'On Hold' state.

 Actual behavior: Instead of the 'Set to Ready' option, the menu still shows 'Put on Hold'.

</td></tr><tr><td>

iOS Mobile

 PRB1993847

</td><td>

Category icons on Now Mobile do not load properly on iOS devices

</td><td>

Item icons appear differently than expected.

</td><td>

1.  Log in to a Now Mobile instance.
2.  Navigate to the 'Services' tab.

Note the Item's icons.

3.  Manually refresh by swiping down from the top of the screen.

 Expected behavior: The icons should be the same between step 2 and step 3.

 Actual behavior: Icons are different between step 2 and step 3.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

