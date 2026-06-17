---
title: Mobile Agent - BlackBerry for iOS v17.2.0
description: The iOS v17.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for iOS v17.2.0

The iOS v17.2.0 release provides fixes for the application.

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

 PRB1717876

</td><td>

The user can edit non-editable fields for members of a crew

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

 

</td></tr><tr><td>

Mobile iOS

 PRB1723622

</td><td>

There is an issue when changing the screen orientation in the Now Mobile app

</td><td>

 

</td><td>

1.  Log in to Now Mobile.
2.  Navigate to My Onboarding.
3.  Click **Open tasks**.
4.  Under **Timeline**, click **Initial check-in**.
5.  Under **My tasks** click **Please fill out this survey**.

Notice that the To-do Screen is opened.

6.  Click **Learn more**.
7.  Switch to landscape mode and change it back.

 Notice that the screen flickers.

</td></tr><tr><td>

Mobile iOS

 PRB1727022

</td><td>

There is an issue with the images in the Icon Section Destination

</td><td>

The images in the quick links \(on the Icon destination screen\) display incorrectly.

</td><td>

1.  Open the Now Mobile app version in a base instance.
2.  Navigate to the Home tab and notice the images under 'Quick links'.

 Notice that the images don't display correctly.

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

 PRB1732502

</td><td>

When approving a record using E-signature and Okta verify, the record does not update

</td><td>

 

</td><td>

1.  Log in to iOS Mobile Agent.
2.  Navigate to **My Work** &gt; **Approval**.
3.  Select the approval assigned to the user.
4.  Click **Approve**.
5.  When prompted, input the login credentials again \(the E-signature part\).

 Observe that the user is sent back to the Approval screen and the approval does not go through.

</td></tr><tr><td>

Mobile iOS

 PRB1726489

</td><td>

A session doesn't start correctly when the SDK was started and reset with the same API Key within a short time interval \(milliseconds\)

</td><td>

Reproduction is not reliable. It depends on the order and time interval between API call responses in the iOS app.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](../agent-blackberry-available-versions.md)

