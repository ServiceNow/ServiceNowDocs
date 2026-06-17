---
title: ServiceNow Onboarding - Intune for iOS v15.3.0
description: The iOS v15.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2023-01-05"
reading_time_minutes: 4
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v15.3.0

The iOS v15.3.0 release provides fixes for the application.

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

PRB1624982

 [KB1209442](https://hi.service-now.com/kb_view.do?sysparm_article=KB1209442)

</td><td>

The HTML field doesn't show on the Details Screen if there are multiple calculated fields on the Details Screen

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

PRB1621945

</td><td>

Every time a function registered in the List screen in iOS is refreshed, it appears and disappears repeatedly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1611520

 [KB1182159](https://hi.service-now.com/kb_view.do?sysparm_article=KB1182159)

</td><td>

UI Rule does not apply on refresh of the record screen

</td><td>

The background color of the number on the record screen header card disappears.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1611186

</td><td>

The 'Mark as complete' button is not enabled after playing a video in a 'View Video' HR Task

</td><td>

This issue occurs in iOS version 15.1 and older versions of the Now Mobile app.

</td><td>

1.  Create an onboarding case for a new hire.
2.  Open the onboarding case in platform.
3.  Click **Add task** in related links.
4.  Select HR task type as 'View Video', URL as a Youtube URL link, and short description as 'Overview of platform architecture'.
5.  Assign the task to a new hire.
6.  Log in to Now mobile with the new hire login and password.
7.  Navigate to **My Requests** and open HR task.
8.  Refresh the task and click on the video.

 Notice that the 'Mark as complete' button is not enabled.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1609269

</td><td>

Global search sometimes results in an incomplete result set

</td><td>

The search query for paginated results does not include search sources provided in the search results for the previous page.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1608713

</td><td>

Clicking on the Genius card results in the Virtual Agent on the iOS NOW mobile app showing a security constraints message

</td><td>

 

</td><td>

1.  Enable AI search for the instance.
2.  Navigate to **AI Search** **AI search status** **Request AI Search**.
3.  Once the AI search is enabled at the instance level, enable it at the portal level for the SP portal.
    1.  Navigate to **Service Portal** &gt; **Portals** and open a portal record.
    2.  On the form, select Enable AI Search.
4.  Navigate to the chat in the mobile instance and activate it.
5.  Navigate to the sys\_property: com.glide.cs.click\_metrics.ai\_search and set it to 'true'.
6.  Log in to the instance on NOW Mobile app using an iOS device.
7.  Click on the 'chat' quick action on the top-right corner.
8.  Click on **Start conversation**.
9.  Type **create an incident** in the chat window.
10. The Create Incident genius card result appears.
11. Click on the link.

 Actual behavior: Security constraints message appears on the screen.

 Expected behavior: The catalog item appears on the page.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1607749

</td><td>

An incorrect font style is displayed instead of the Highlighted Value font style

</td><td>

 

</td><td>

1.  Create an HR task with a due date.
2.  Log in as the task assignee.
3.  Click **My Task** from the home page.

Notice that the overdue text is slightly bold and does not match the font in Figma.


</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1607670

</td><td>

Checklist items are not wrapped in mobile app

</td><td>

When viewing checklists on a record screen in the mobile app, the test does not wrap and instead cut off.

</td><td>

1.  Navigate to a San Diego instance with ITSM mobile agent installed.
2.  Navigate to **Incident form** &gt; **Configure Layout** &gt; **Add checklist to the form**.
3.  Open an incident record that will be assigned to your test user in the mobile app.
4.  Add long strings of text as items to the checklist on the record and save the record.
5.  Open the incident record screen \(My incident\) and navigate to the Details screen.
6.  Add a new screen checklist type field and click **Save**.
7.  Log in to the mobile app and open up the incident record

 Expected behavior: The text wrap is visible.

 Actual behavior: Text doesn't wrap and therefore, it is cut off.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1603902

</td><td>

iOS Department category on the filter. end of search list is bad or does not show

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1599175

 [KB1164769](https://hi.service-now.com/kb_view.do?sysparm_article=KB1164769)

</td><td>

Messages are not getting translated in the Now mobile app when the iOS device's language is set to Japanese

</td><td>

Messages not getting translated include, 'Are you sure you want to cancel the conversation' and 'No chat agents currently available'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1571874

</td><td>

Clicking View in the info messages in Now mobile does show the entire text

</td><td>

In Now mobile, when a long info message is displayed, there is a View link to view the entire message. However, clicking View doesn't actually do anything.

</td><td>

1.  Login to any San Diego base instance.
2.  Log in to the Now mobile app in the San Diego instance and go to the Services tab.
3.  Search for any catalog item and open it. \(In this case, it is Executive Desktop\).
4.  Change the value of the Operating system variable. This will display an info message at the top go the screen.

Notice that the full message is not displayed but rather presented with a View link. When you click on **View**, nothing happens.


</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1545016

</td><td>

Notification text is not entirely displayed on iPhone

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1449441

</td><td>

In the iOS Mobile Apps, a second scroll bar can appear in the HTML fields

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

