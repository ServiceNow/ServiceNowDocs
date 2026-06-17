---
title: Mobile Agent for iOS v19.5.0
description: The iOS v19.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v19.5.0

The iOS v19.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_uw1_y14_31c" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS

 PRB1872661

</td><td>

Genius result view does not render HTML

</td><td>

Genius results that include HTML are not rendered properly. Instead, the entirety of the text is shown, including HTML tags.

</td><td>

1.  Log in to the Agent app.
2.  Navigate to the Home tab.
3.  In the navigation search bar, type in 'Link for replacing my laptop'.

 Expected behavior: The genius result should contain a selectable hyperlink to the appropriate request.

 Actual behavior: The URL for what should be a hyperlink shows up inside an HTML tag \(the raw HTML is shown rather than being rendered\).

</td></tr><tr><td>

Mobile iOS

 PRB1874645

</td><td>

frED external links don't load properly for iOS Mobile users

</td><td>

The user gets stuck in a loading loop upon selecting a frED link.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1875859

</td><td>

RecordCardNDS link does not work for mobile

</td><td>

When the user attempts to open a JSON record card after submitting a request on Virtual Agent \(VA\), an 'Error loading URL' screen appears.

</td><td>

1.  Log in to Now Mobile 19.5 or later.
2.  Open VA and enter 'Request Miro'.
3.  Follow the flow to submit a Miro request.
4.  After submission, VA sends a JSON record card summarizing the request.
5.  Select the card.

 Expected behavior: The record opens in a native screen.

 Actual behavior: An 'Error loading URL' screen appears.

</td></tr><tr><td>

Mobile iOS

 PRB1865433

</td><td>

When the user scrolls up/back in chat history, the screen automatically scrolls to the bottom of the page when a new message comes in

</td><td>

When a response comes through for an utterance, the 'New messages' button doesn't display. Instead, the screen is automatically scrolled to the bottom of the page. If the user scrolls up, auto-scroll-to-bottom should be disabled until they've either selected the scroll-to-bottom button or they've manually scrolled to the bottom.

</td><td>

1.  Create an admin user for testing.
2.  Load NAVA.
3.  Type in an utterance and send.
4.  Before the response comes in, scroll up to view previous responses.

 Observe that when the user scrolls up/back in chat history, scroll moves to the bottom of the page when new message comes in.

</td></tr><tr><td>

Mobile iOS

 PRB1874458

</td><td>

Issues with update choice picker in Virtual Agent \(VA\)

</td><td>

Various styling issues appear.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1884160

</td><td>

Now Assist requests are not completed upon submission

</td><td>

A request does not complete and a 'Problem on my side' error appears.

</td><td>

1.  Now Assist search for 'Order laptop'.
2.  Order a development laptop.
3.  Submit.

 Expected behavior: The request should complete upon submission and provide an RITM number.

 Actual behavior: The request does not complete and a 'Problem on my side' error appears.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

