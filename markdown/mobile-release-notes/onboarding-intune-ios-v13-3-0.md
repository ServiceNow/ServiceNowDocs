---
title: ServiceNow Onboarding - Intune for iOS v13.3.0
description: The iOS v13.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v13-3-0.html
release: mobile
topic_type: reference
last_updated: "2022-01-13"
reading_time_minutes: 1
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v13.3.0

The iOS v13.3.0 release provides fixes for the application.

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

 PRB1531695

</td><td>

Focus order of elements on the 'My Requests' page does not follow the visual order

</td><td>

When navigating the 'My Request' page of a record on the Now Mobile application using VoiceOver on iOS, the focus order of the content does not follow the visual order of the elements on the screen.

</td><td>

1.  Using Now Mobile for iOS, log in to an account that has submitted one or more requests.
2.  Open a request and navigate to the 'Updates' tab.
3.  Enable VoiceOver and navigate through the elements on the page.

After navigating from the **Take Photo** option, the navigation moves back to the **Add Comment** element, then proceeds to the next section.


 Expected behavior: The focus order of the elements on the page should follow the visual order.

 Actual behavior: The focus order navigates backwards after the **Take Photo** element.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1525757

</td><td>

Surveys still appear under the 'Pending' tab after submitting them in iOS

</td><td>

Also, when users complete a questionnaire, the WBA response returns with a refreshed item as deleted.

</td><td>

1.  Log in to the Agent application.
2.  Navigate to **Field Service** &gt; **My tasks** &gt; **Open a Work Order task**.
3.  Click the top menu function and **Select Questionnaire**.

Notice two tabs: 'Pending' and 'Completed'.

4.  Select any record from the 'Pending' tab.
5.  Complete the questionnaire and submit it.

 Expected behavior: Once the survey is completed, it should not be displayed under the 'Pending' tab.

 Actual behavior: Completed surveys are still visible in the 'Pending' section and are removed only after you perform a manual refresh.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1548149

</td><td>

When the glide.analytics property is false and users get a notification, they can't open it

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

