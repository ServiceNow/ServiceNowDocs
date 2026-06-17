---
title: ServiceNow Onboarding - Intune for iOS v13.5.0
description: The iOS v13.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v13-5-0.html
release: mobile
topic_type: reference
last_updated: "2022-03-03"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v13.5.0

The iOS v13.5.0 release provides fixes for the application.

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

 PRB1544506

 [KB1000434](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1000434)

</td><td>

Survey header is missing after selecting a choice

</td><td>

This issue is only observed on iOS devices.

</td><td>

1.  Create a survey on the platform.
2.  Add a choice component to the survey.
3.  Save and publish the survey.
4.  Create a mobile web screen named 'Survey Test'.
5.  Add the mobile web screen to a screen tab.
6.  Associate the screen tab to a navigation tab of Now Mobile.
7.  Access the survey on Now Mobile.

It shows the 'Survey Test' in the header area.

8.  Select a choice.

 Expected behavior: It should still show the 'Survey Test' in the header area.

 Actual behavior: The header area is empty.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1547159

</td><td>

The phone type menu item \(Contact Support\) is not visible under the chat applet on Now Mobile if the phone number includes a space

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1554685

</td><td>

Time cards do not allow decimal numbers based on region settings

</td><td>

 

</td><td>

1.  Navigate to **IOS settings** &gt; **General** &gt; **Language &amp; Region** &gt; **Region** and set the region to 'Czechia'.
2.  Log in to a Rome instance with the Now Mobile app and the Mobile time sheets application installed.
3.  Navigate to time sheets.
4.  Open any existing time sheet record.
5.  Edit the time card and try to enter the values.

Observe the keyboard, which shows ',' per the region settings.

6.  Choose a day and enter a decimal number \(for example, 2,4\) and select **Done**.

Observe that it clears the value.


 Expected behavior: The value should be saved in the 'Time Card' day.

 Actual behavior: The value disappears after saving the record.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1542705

</td><td>

Icon color discrepancy in list view for Mobile Card Builder

</td><td>

 

</td><td>

1.  Log in to the instance on the Agent mobile app.
2.  Navigate to **My work** &gt; **INC List 2**.

 Observe the icon color of the buttons in each card.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

