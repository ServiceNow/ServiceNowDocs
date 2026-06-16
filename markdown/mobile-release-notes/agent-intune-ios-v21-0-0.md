---
title: Mobile Agent - Intune for iOS v21.0.0
description: The iOS v21.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-intune-ios-v21-0-0.html
release: mobile
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - Intune app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - Intune for iOS v21.0.0

The iOS v21.0.0 release provides fixes for the application.

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

 PRB1944698

</td><td>

The bubble buttons appear to overlap in the Now Mobile app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1966767

</td><td>

The Granular Delegation plugin causes dates to appear truncated

</td><td>

With the Granular Delegation plugin installed, when a user looks at the Delegation details on NOW Mobile app, the Start and End Dates are truncated.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1935409

</td><td>

When performing the notification actions **Accept**/**Reject** for the parts sourcing flow, an error is thrown

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1969016

</td><td>

NumberSlider receives gesture callbacks even when not in focus

</td><td>

On the scripted input form screen, the user is not able to select **Choice** if the previous page has slider inputs.

</td><td>

1.  Select a Work Order Task.
2.  Tap the three dots in the top right corner of the screen to open the drop-down menu.
3.  Select **Take questionnaire** &gt; **Test questionnaire** to navigate to the scripted input form screen.
4.  Answer the initial number-based questions and proceed to the second page of the questionnaire.
5.  Attempt to answer the 'Choice' based questions on this page.

 Notice that the screen freezes or becomes unresponsive.

</td></tr><tr><td>

iOS Mobile

 PRB1966026

</td><td>

Selections aren't structured as lists

</td><td>

Several lists in the app aren't tagged as lists. Therefore, screen reader users can't get an overview of the dimension of the selected list and the current position in the list.

</td><td>

1.  Log in to the app.
2.  Turn on VoiceOver Navigate to Incident list: My work &gt; All incidents &gt; See all.
3.  Tap the Filter button and expand the 'Sort by' list.
4.  Use swipe gestures to navigate through the 'Sort by' list items and listen to VoiceOver announcements.

 Notice that VoiceOver announces each option individually \(for example, 'Number \(Ascending\)', 'Number \(Descending\)', 'Created', 'State'\). There's an announcement of total items \(e.g., '4 options'\). but no announcement of current position \(e.g., '1 of 4', '2 of 4'\). Additionally, the user can't determine how many options are available, where they are in the list, or how much more content to explore.

</td></tr><tr><td>

iOS Mobile

 PRB1966016

</td><td>

There are two focus stops on the 'Share Comments' toggle

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1965990

</td><td>

The **Show all** link does not have a role

</td><td>

The **Show all** link has no role. Screen reader users may be unsure if the text is interactive.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1963344

</td><td>

The map fails to show searched items

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1965971

</td><td>

Missing roles in 'Sort By'

</td><td>

On single-select lists or multi-select lists, the screen reader either reads out 'Value \(Selected\) name' or 'Name, Disabled/Selected, double tap to'.

</td><td>

1.  Log in to the ServiceNow Agent app.
2.  Turn on VoiceOver.
3.  Navigate to **My Work** &gt; **All Incidents** &gt; **See All** &gt; **Double Tap Filter** &gt; **Sort By**.
4.  Scroll through the list and note no role is provided for the list items.

Notice that the entries in select lists have no role. Therefore, screen reader users may not know that the entry can be selected. For some of them, the screen reader at least reads out an operating hint.

</td></tr><tr><td>

iOS Mobile

 PRB1961309

</td><td>

Theme coloring issues

</td><td>

Input bar background is always background-primary for light and dark mode

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-intune-available-versions.md)

