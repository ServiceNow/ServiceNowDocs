---
title: Mobile Agent for iOS v21.5.0
description: The iOS v21.5.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-ios-v21-5-0.html
release: mobile
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v21.5.0

The iOS v21.5.0 release provides fixes for the application.

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

 PRB2033864

</td><td>

Smart assessment attachment upload fails on first attempt and an unanswered question error appears on **Submit** in the Now Mobile app

</td><td>

Two issues occur when completing smart assessments on NOW Mobile: Unanswered question error on submit even after all questions are answered - no indication of which question is missing. Attachment upload fails on first attempt, requiring re-upload before submission succeeds.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2034884

</td><td>

Captured image attachments saved in Display P3 color space cause color shift in non-color-managed viewers

</td><td>

Images captured via the iOS app's camera/scan flow are uploaded in the Display P3 wide-gamut color space instead of standard sRGB. The pixel data is intact and renders correctly in color-managed viewers \(web browser, sys\_attachment preview\), but applications that are not color-managed misinterpret the embedded P3 ICC profile as sRGB, producing a visible color shift \(oversaturation / reddish-teal cast\).

</td><td>

1.  On a wide-gamut iPhone, open the NOW Mobile Agent app \(or any flow using the attachment upload / scan documents path\).
2.  Capture or scan a document/photo with the camera.
3.  Select a document type and complete the upload to the instance.
4.  Download the uploaded attachment from the sys\_attachment table and inspect its color profile \(for example, 'sips -g profile &lt;file&gt;' on macOS\).

Notice that the image is saved in Display P3 \(wide gamut\) when it should be displayed in sRGB.

5.  Open the uploaded image in a non-color-managed viewer.

 Expected behavior: The colors match what was captured.

 Actual behavior: The colors are shifted/oversaturated.

</td></tr><tr><td>

iOS Mobile

 PRB2020083

</td><td>

Mobile Questionnaires Details Text under the Question is cut off

</td><td>

When filling in a questionnaire on Mobile Agent app, the 'Details' text under the question is cut off. However, after the completed questionnaire is completed, the 'Details' text shows the full text.

</td><td>

1.  Create a survey question with the below options:
    -   Type: String
    -   String option: Single line wide.
    -   Details: หากข้อใดไม่มีข้อมูล สามารถใส่ - ได้.
2.  Log in to the Mobile Agent App.
3.  Navigate to **My Work**.
4.  Search any WOT.
5.  Select **Take questionnaire** to observe the issue.

 Notice that the details text is cut off.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-available-versions.md)

