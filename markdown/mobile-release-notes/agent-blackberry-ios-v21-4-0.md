---
title: Mobile Agent - BlackBerry for iOS v21.4.0
description: The iOS v21.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-blackberry-ios-v21-4-0.html
release: mobile
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for iOS v21.4.0

The iOS v21.4.0 release provides fixes for the application.

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

 PRB1996628

</td><td>

Crash in Firebase in CalendarStore

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2004945

</td><td>

Users can't be mentioned in Japanese

</td><td>

Users can't be mentioned in the Activity Stream in Japanese in Now Mobile.

</td><td>

1.  Install the Japanese keyboard in iOS by opening **Settings** &gt; **Keyboard** &gt; **Keyboards** &gt; **Add New Keyboard** and add 'Japanese - Romaji' keyboard.
2.  Create a user in the instance with first name 'テスト' \(test\) and family name 'ユーザー' \(user\).
3.  Create an incident with admin user.
4.  Log in to Now Mobile with admin user.
5.  Open the incident created in step 3.
6.  Select 'Updates' tab and 'Add Comment'.
7.  Select the 'Japanese - Romaji' keyboard \(日本語ローマ字\).
8.  Type '@' and select '@'.
9.  Type 'tesuto' and select 'テスト'.

 Expected behavior: 'テスト ユーザー' user is displayed.

 Actual behavior: No user is displayed but if you delete the last character \(ト\) the user is displayed.

</td></tr><tr><td>

iOS Mobile

 PRB2003734

</td><td>

Smart routing of List, Form, and KB links to apps doesn't work

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2016497

</td><td>

Searching for key words returns a blank page

</td><td>

While searching for key words in the Now mobile app, a blank page is returned instead of 'No results found' being displayed.

</td><td>

Pre-requisites: Create a new search configuration under the 'Homepage' Launcher screen header using the base instance NowMobile App Search Configurations, with the search engine set to 'Zing' and the following Application Search Sources added: Incidents, Knowledge.

 1.  Open the Now Mobile app on an iOS device.
2.  Tap the search icon and enter keywords such as thing, cookie, or post.
3.  If there are no perfect matches, then it should show as 'No results found'.
4.  It is showing as 'No results found' in Android correctly but in iOS it is displaying a blank page.

 Expected behavior: When no results match the searched keyword, the message 'No results found' should be displayed.

 Actual behavior: On iOS, a blank page is displayed instead of the 'No results found' message.

</td></tr><tr><td>

iOS Mobile

 PRB1949448

</td><td>

Focus does not start at the beginning of the page when selecting a location

</td><td>

When user selects location card, the focus does not consistently start at the top of the page.

</td><td>

1.  Navigate to the 'Asset' tab and select **Location audits** &gt; **More options** &gt; **New Location Audit** and select a location.
2.  Navigate to the list of locations and submit a location.
3.  Select a location card.
4.  Navigate back to the 'Location audits' page and select the location card again.

 Expected behavior: Focus starts at the beginning of page.

 Actual behavior: Notice that the focus startslocation is inconsistent.

</td></tr><tr><td>

iOS Mobile

 PRB2018049

</td><td>

The Question Circle icon not displaying in iOS correctly

</td><td>

The mobile screen tab is configured to use the 'Question circle' icon, but it displays a different icon.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-blackberry-available-versions.md)

