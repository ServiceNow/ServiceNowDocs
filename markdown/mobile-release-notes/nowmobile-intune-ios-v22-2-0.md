---
title: Now Mobile - Intune for iOS v22.2.0
description: The iOS v22.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v22-2-0.html
release: mobile
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 8
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v22.2.0

The iOS v22.2.0 release provides fixes for the application.

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

 PRB2071235

 [KB3150118](https://hi.service-now.com/kb_view.do?sysparm_article=KB3150118)

</td><td>

Camera not visible when scanning Barcode/QR on Legacy SG Form screens on iOS 26

</td><td>

No camera preview appears.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS

 PRB2066528

</td><td>

Silent-push force-logout traps the user in an infinite login/logout loop on the same instance

</td><td>

When a force\_logout silent push is received for an instance, the user is correctly logged out — but if they then log back into that same instance, they are force-logged-out again immediately. There is no way to break the loop from within the app; deleting and re-adding the instance does not help.

</td><td>

1.  Log into a ServiceNow instance in the mobile app.
2.  Trigger a force\_logout silent push targeting that instance \(admin/backend action\).

Observe that the user is force-logged-out as expected, with a message.

3.  Log back into the same instance.

Observe that as soon as the main tab bar appears, the user is force-logged-out again.

4.  Repeat step 3.

 Expected behavior: After the forced logout completes once, the user should be able to log back in and stay logged in normally.

 Actual behavior: The user is forced out again on every subsequent log in to that instance, indefinitely.

</td></tr><tr><td>

Mobile iOS

 PRB2071173

</td><td>

'My Schedule' events disappear and show 'Restricted events' after Start Travel/Start Work writeback

</td><td>

In the Agent Mobile app's 'My Schedule' screen \(Field Service Management, built on the shared native Calendar feature\), completing the 'Start Travel' or **Start Work** UI action on a Work Order Task and immediately navigating back to the schedule causes that day's events to disappear from the list, replaced by a 'Restricted events' header message instead of the normal event count.

</td><td>

1.  Log in to the Agent Mobile app \(Intune build\).
2.  Navigate to **My Work** &gt; **Field Service Management** &gt; **My Schedule**.
3.  Ensure that a day has at least one Work Order Task \(WOT\) scheduled.
4.  Open a WOT from that day.
5.  Select **Start Travel**or **Start Work**.
6.  Immediately navigate back to 'My Schedule'.

 Expected behavior: The day continues to show its scheduled WOT\(s\) and the correct event count.

 Actual behavior: The day's WOT\(s\) disappear from the list; the day header shows 'Restricted events' instead of the event count.

</td></tr><tr><td>

Mobile iOS

 PRB2057165

</td><td>

Inconsistent toast messages during offline ticket creation with and without attachment

</td><td>

The ServiceNow mobile application displays inconsistent user-facing confirmation messages when attaching an attachment record while in offline mode. The actual functionality is consistent \(records are saved to Outbox and sync later\), but the user-facing toast messages differ based on whether an attachment is included.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB2081184

</td><td>

AppletLauncher horizontal card cells appear stretched and distorted when iOS 'Larger Text' is set to a Zoomed \(accessibility\) size

</td><td>

On the ALP Home screen, horizontal cells rendered via CardCollectionViewCell an image looses its aspect ratio and appears vertically squashed/stretched. The label text below it also wraps awkwardly. This occurs specifically when the device's iOS accessibility text size setting is in the Zoomed \(AX\) range rather than Standard.

</td><td>

1.  On device or simulator, Navigate to **Settings** &gt; **Accessibility** &gt; **Display &amp; Text Size** &gt; **Larger Text**.
2.  Enable 'Larger Accessibility Sizes' and drag the slider into the accessibility \(Zoomed\) range, past the Standard maximum.
3.  Open the AppletLauncher screen \(for example, the Home tab\).
4.  Observe the two sections: the top banner section and the News and Announcements section.

 Expected behavior: Text and images should scale proportionally, without image distortion or blank space at the bottom.

 Actual behavior: A blank space appears at the bottom of each banner. The News and Announcements section appears stretched. Compare against the same screen at regular text size.

</td></tr><tr><td>

Mobile iOS

 PRB2082997

</td><td>

NAVA header title ignores server-configurable brandingSettings.header\_label, shows hardcoded Otto/Now Assist name

</td><td>

On iOS 26 \(liquid glass\), the NAVA chat header title is hardcoded to AIAssistantType.name \(either 'Otto' or 'Now Assist'\).

</td><td>

1.  Configure a ServiceNow instance with a custom brandingSettings.header\_label value \(for example, 'Now Support' or 'IT Help'\) via the Virtual Agent branding settings admin UI.
2.  Open the NowMobile iOS app on an iOS 26 device or simulator.
3.  Launch a NAVA chat conversation.
4.  Observe the header title in the navigation bar.

 Expected behavior: The header should display the custom name configured in brandingSettings.header\_label \(for example, 'Now Support'\).

 Actual behavior: The header displays the hardcoded 'Otto' \(or 'Now Assist'\) from AIAssistantType.name, ignoring the server-configured value.

</td></tr><tr><td>

Mobile iOS

 PRB2083148

</td><td>

Input actions \(ellipsis menu\) are not tappable when there is a read-only field in the IFS

</td><td>

Tapping the ellipsis button doesn't open a menu with an action.

</td><td>

1.  Configure a IFS with several fields which the first is a read-only field of string and the last is an input with input actions.
2.  Scroll to the input with the input actions.
3.  Tap the ellipsis of the input from step 2 to open the input actions menu.

 Expected behavior: Tapping the ellipsis button opens the menu with the action.

 Actual behavior: Tapping the ellipsis button doesn't open the menu with the action.

</td></tr><tr><td>

Mobile iOS

 PRB2071746

</td><td>

A numeric field in an input form screen will open a floating numeric keyboard that prevents the user from seeing what is typed

</td><td>

A floating keyboard is misaligned and blocks the field.

</td><td>

1.  With an iPad, using Mobile app, enter any instance with a input form with numerical values.
2.  When a parameter screen shows with a numerical field, tap on it.

 Expected behavior: Keyboard shows from bottom and one can see what is being typed in.

 Actual behavior: A floating keyboard is misaligned and blocks the field.

</td></tr><tr><td>

Mobile iOS

 PRB2072515

</td><td>

Virtual Agent input field renders no text while typing \(input captured but not visible\) in glass-pill layout

</td><td>

When the user types a response, the text doesn't show up in the input field. However, when they select **Send**/**Enter**, the Virtual Agent receives what they typed and the conversation continues normally.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB2073608

</td><td>

The **X** icon for closing pop-up is misaligned on iOS Now Mobile app

</td><td>

The **X** icon for closing the pop-up is not centered.

</td><td>

1.  Log in the Now Mobile App.
2.  Navigate to **Services** &gt; **Business application lifecycle** &gt; **Register a business**.
3.  Scroll down and select **Type of application**.

 Observe in the pop-up window that the **X** icon for closing the pop-up is not centered.

</td></tr><tr><td>

Mobile iOS

 PRB2076244

</td><td>

In NAVA Enhanced chat, selecting **Navigate to internal search results** redirects the user to the Home tab

</td><td>

After upgrading iOS Now mobile to version 22.0.0, selecting the **Navigate to internal search results** icon \(magnifying glass\) does not open the internal search results. It instead redirects to the Home Tab.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB2077947

</td><td>

The last item in a Reference list is hidden behind the footer

</td><td>

The user is unable to select the item because it is hidden behind the footer.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB2079310

</td><td>

The Genius search citation 'View details' sheet is missing a **Title**/**Action** button, and button and description links are unresponsive

</td><td>

When a Genius \(AI-synthesized\) search result contains an actionable citation \(for example, a catalog item\), tapping the citation opens a 'View details' bottom sheet. On iOS this sheet has multiple defects: The citation title and the **Request with form** action button do not render. Where the description text contains a Markdown link with a relative URL, the link renders as literal Markdown syntax instead of a tappable link. Once the button/link render correctly, tapping either dismisses the sheet but performs no navigation.

</td><td>

1.  In Genius search, search 'How do I talk to HR?' \(or any query returning a catalog citation in the Now Assist synthesized answer\).
2.  Select the 'HR Systems Question' citation to open the 'View details' sheet.

Observe that the sheet shows the description but no title and no **Request with form** button.

3.  Select the 'HR Report Question' citation, whose description contains... please use the \[Workday Based Report Request\]​.

 Expected behavior: The sheet shows the citation title and a working**Request with form** button that opens the catalog item. Additionally, any Markdown links in the description render as selectable links that open the linked record.

 Actual behavior: Title and button are missing entirely on iOS \(Android shows both\). Description Markdown links render as raw text on iOS.

</td></tr><tr><td>

Mobile iOS

 PRB2070099

</td><td>

**Add to Calendar** .ics file links download as .bin files and fail to open

</td><td>

On iOS the file download as a .bin and can't be opened unless renamed.

</td><td>

1.  When in the app, scroll to bottom of homepage.
2.  Locate 'Upcoming events' widget.
3.  Select the **Add to calendar** button on any event.

 Expected behavior: Selecting**Add to calendar** in the MyHR Portal \(embedded in the Now Mobile App\) should add the event to the device calendar without error, on both iOS and Android.

 Actual behavior: On iOS the file will download as a .bin and thus can't be opened unless renamed.

</td></tr><tr><td>

Mobile iOS

 PRB2084172

</td><td>

The **Add time card** button doesn't work when tapped in search results

</td><td>

The **Add time card** Input Form does not open.

</td><td>

1.  Navigate to the Search screen from the Dashboard.
2.  Search for an RFST record, for example 'RFST\*' or 'RFS for'.
3.  Search results are displayed successfully.
4.  Open/locate an RFST Search Result Card.
5.  The card displays the **Add Time Card** button.
6.  Tap **Add Time Card**.

 Observe that the **Add Time Card** Input Form does not open.

</td></tr><tr><td>

Mobile iOS

 PRB2082968

</td><td>

Agent App crashes on iPhone after scanning barcode

</td><td>

The Agent application crashed completely after scanning the barcode.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

