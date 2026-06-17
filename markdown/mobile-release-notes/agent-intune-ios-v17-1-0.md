---
title: Mobile Agent - Intune for iOS v17.1.0
description: The iOS v17.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-ios-v17-1-0.html
release: mobile
topic_type: reference
last_updated: "2024-01-04"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for iOS v17.1.0

The iOS v17.1.0 release provides fixes for the application.

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

Mobile iOS

 PRB1712551

</td><td>

The app refreshes and crashes when the user performs transactions on WOT related to the FSM Application

</td><td>

The issue is not specific to FSM and can happen in other use cases outside of FSM \(specifically when the tab information is different in user\_client API response vs device local cache\).

</td><td>

1.  Log into an Agent Mobile 16.4.0 instance.
2.  Switch to the 'My Tasks' tab.
3.  Select one of the WOT that has not yet been accepted by the user \(for example, WOT presents the **Accept** button\).
4.  Click **Accept**.

 Expected behavior: Agent Mobile does not refresh back to the Home screen.

 Actual behavior: The page is refreshed to the Home screen or there is an error. If there is an error, navigate **Back** and notice that the page refreshes to the Home screen.

</td></tr><tr><td>

Mobile iOS

 PRB1717876

</td><td>

The user is able to edit and change non-editable fields for members of a crew

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1712303

</td><td>

The screen reader announces static text sections as buttons

</td><td>

Static text should not be announced as a button.

</td><td>

1.  Log into the Now mobile app.
2.  On the home page, navigate to 'Browse all topics'.

 Notice that everything on the screen is selectable but nothing happens.

</td></tr><tr><td>

Mobile iOS

 PRB1718213

 [KB1577613](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1577613)

</td><td>

The embedded list redirects the user to an unrelated saved item when the list is refreshed

</td><td>

The wrong Task SLA is shown in the embedded list.

</td><td>

1.  Log into the Agent Mobile App.
2.  Navigate to **My Work** &gt; **My tasks**.
3.  Open any task.
4.  Navigate to **Related Embedded Screen** &gt; **Task SLA** &gt; **See all**.
5.  Click the **Save Bookmark** button on the top right.
6.  Navigate back to the **My tasks** list screen.
7.  Open any other task.
8.  Navigate to **Related Embedded Screen** &gt; **Task SLA** &gt; **See all**.
9.  Drag down and refresh the Embedded List.

 Expected behavior: The user sees the Task SLA of the current record.

 Actual behavior: The user sees the Task SLA saved in the Bookmark.

</td></tr><tr><td>

Mobile iOS

 PRB1712165

</td><td>

The word 'Notifications' is not translated into Norwegian with the base instance language pack

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1719396

 [KB1579727](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1579727)

</td><td>

Cancelling an attachment upload that is at 100% results in an app crash

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

