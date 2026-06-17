---
title: Mobile Agent - BlackBerry for Android v20.0.0
description: The Android v20.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-06-05"
reading_time_minutes: 9
breadcrumb: [Mobile Agent - BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent - BlackBerry for Android v20.0.0

The Android v20.0.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.fulfiller). Users can launch a demo to try the ServiceNow Agent app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android

 PRB1891024

</td><td>

Mobile UX analytics data collection fails due to a change in the certification authority

</td><td>

Validation fails and data isn’t sent when the certification authority changes.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1866637

</td><td>

A custom map's single input doesn't display in full-screen mode

</td><td>

When a custom map input is a single visible input, an input form screen should display in full-screen mode.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1868822

</td><td>

CabrilloBackPressHandler.flowEnded\(\) can inadvertently back the user out of the entire application

</td><td>

When a catalog item is submitted and the **Close** button is selected, the app crashes and sends the user back to the Android home screen.

</td><td>

1.  Log in to the Agent app.
2.  Select the Home-web tab.
3.  Select the Marketing channel and select **Raise Request**.
4.  Select the catalog items \(for example, 'MySales \(SFDC\) functional...'\) and follow the screen instructions to submit the catalog item.
5.  Select the **Close** button.

 Expected behavior: The catalog item page is closed and sends the user back to the previous screen.

 Actual behavior: The app is closed/crashed and sends the user back to the Android home screen.

</td></tr><tr><td>

Mobile Android

 PRB1774419

</td><td>

Issue with the auto-fill multi-select input parameter

</td><td>

When only a single value is set for the **LIST** field, the parameter screen auto-fills the input as expected and displays the selected value. However, when multiple values are selected, the parameter screen does not auto-fill and does not display the selected value.

</td><td>

1.  Create a field description as string and test as List type.
2.  Log in to now agent.
3.  Navigate to problem Launcher.
4.  Select any problem and select the three dots on top to edit it.

 Notice that when multiple values are selected, the parameter screen does not auto-fill and does not display the selected value.

</td></tr><tr><td>

Mobile Android

 PRB1869910

</td><td>

A web view session automatically logs out after switching tabs when the mobile web screen is configured as the home tab

</td><td>

 

</td><td>

1.  Launch the app and log in.
2.  Wait for the page \(Home tab\) to load.
3.  Navigate to the Notification tab

Notice that WebView session is out of sync in the logcat in the error flow.

Switch back to the Webpage tab.

4.  Select **Check Your Ticket**.

 Notice that the SSO page does not open.

</td></tr><tr><td>

Mobile Android

 PRB1859107

</td><td>

When the user submits a case they land on the case creation page

</td><td>

The user should land on the Catalog Item page.

</td><td>

In Android navigate to **Create case** &gt; **Submit** &gt; **Close**.

 Observe that the user lands on the case creation form instead of the Catalog item page.

</td></tr><tr><td>

Mobile Android

 PRB1868910

</td><td>

The parameter screen ignores device rotation settings

</td><td>

When the barcode scanner screen is opened but the scanner doesn't appear, the current logic switches the device to rotate based on the device sensors \(auto-rotate\). This behavior can occur on any instance in either a fulfiller or requester app where the configuration for the parameter scanning screen \(single or multiple\) is set to not open when shown.

</td><td>

1.  On the device, turn off auto- rotation so the device is locked in portrait mode.
2.  Open the app and navigate to the parameter screen with the scanner page.
3.  Rotate the phone.

 Expected behavior: The app should respect the hardware settings.

 Actual behavior: The scanner screen embedded in the parameter screen rotates.

</td></tr><tr><td>

Mobile Android

 PRB1861694

</td><td>

The wrong word is used as the Finnish translation of the date range indicator 'at'

</td><td>

When the system language and the preferred language of the Agent app is Finnish \(Suomi\), the word 'kohteessa' is used instead of 'klo' as a translation of the date range indicator 'at'.

</td><td>

1.  Change the system language and the preferred language of the Agent app to Finnish \(Suomi\).
2.  Log in to the app.
3.  Open the second tab 'My work'.
4.  Select the **+** icon and then select **Date Input Test**.
5.  An input form screen with a date field is shown.
6.  Select any date and time from the date picker.

 1.  Expected behavior: The string says '&lt;date value&gt; klo &lt;date value&gt;'.
2.  Actual behavior: The string says '&lt;date value&gt; kohteessa &lt;date value&gt;'.

</td></tr><tr><td>

Mobile Android

 PRB1876265

</td><td>

Genius results view does not render HTML

</td><td>

Genius results that include HTML are not properly rendered. Instead, the entirety of the raw text is shown, including HTML tags.

</td><td>

1.  Log in as an admin.
2.  In the navigation search bar, enter 'Link for replacing my laptop'.
3.  Select **Show more** on the card.
4.  Select the link on the card.

 Expected behavior: The genius result should contain a selectable hyperlink to the appropriate request.

 Actual behavior: The URL for what should be a hyperlink shows up inside an HTML tag. For example, the raw HTML is shown rather than being rendered.

</td></tr><tr><td>

Mobile Android

 PRB1864255

</td><td>

The notification category list appears blank

</td><td>

A default theme with a white text color is applied, which appears blank against a white background.

</td><td>

Navigate to **More** &gt; **Settings** &gt; **Preferences** &gt; **Notifications**.

 Observe that the notification category titles are blank.

</td></tr><tr><td>

Mobile Android

 PRB1875307

</td><td>

The user is navigated to an empty list screen after an offline action

</td><td>

While offline, when using the legacy parameters screen to perform an action on an asset via swipe action, the user is navigated back to a blank screen \(an empty list screen\). If the user taps **Back**, they see another blank screen \(another empty list screen\). If they tap **Back** once more, they are sent to the home screen. If they tap back through those list screens, they see the lists populated with records, including an offline update for the action they made.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1890267

</td><td>

In Now Support, a deep link to a case that was created during an impersonation fails to load a valid page

</td><td>

The created case shows details about the logged in user/base user instead of the impersonated user, and user isn’t able to view the case.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1865339

</td><td>

Default list and form screens open instead of URLs with base instance configuration

</td><td>

A fix for URL transformation inadvertently brings in default list and form screen builders when a URL matches a well-known platform list or record URL.

</td><td>

1.  Add a link to a standard form or list URL such as incident\_list or incident.do?sys\_id=\{sys\_id\} using a link URL function.
2.  Open the link in the app.

 Expected behavior: The URL opens in an internal web browser.

 Actual behavior: A default native list or form screen is opened.

</td></tr><tr><td>

Mobile Android

 PRB1879313

</td><td>

Location tracking frequency is converted to 0 if the value is less than 60 seconds

</td><td>

The location tracking frequency should be five seconds but it is instead set to 0.

</td><td>

1.  Log in to the Agent app.
2.  Navigate to settings and enable manual location tracking.
3.  Check the tracking coordinates on sys\_mobile\_devices table on the column 'Location timestamp'.

 Expected behavior: The location tracking frequency should be 5 seconds.

 Actual behavior: The location tracking frequency is set to 0.

</td></tr><tr><td>

Mobile Android

 PRB1887024

</td><td>

An unexpected option is available in a single-select bottom sheet

</td><td>

Three options appear, one of which is 'Archive folder'.

</td><td>

1.  Select the quick action button to launch chat.
2.  Start a new conversation.
3.  Select **Show me everything**.
4.  Select **See all** on the line with IT Topics.
5.  Select **Email Retention Policy**.
6.  When prompted, select Archive folder and wait for a number of Virtual Agent responses to come in.

 Expected behavior: When the next bottom sheet shows, there should be two options \(no **Archive folder**\).

 Actual behavior: When the next bottom sheet shows, there are three options, one of which is **Archive folder**.

</td></tr><tr><td>

Mobile Android

 PRB1847355

</td><td>

A mobile web screen inside a record screen performs a refresh when scrolling up on Android devices

</td><td>

Mobile web screens, when configured as a record screen segment within record screens, cause Android devices to refresh the Mobile web screen destination URL when scrolling up.

</td><td>

1.  Open ITSM Mobile Agent. Create a Mobile web screen \(sys\_sg\_browser\_screen\) with the URL set to /now/sow/list.
2.  Add the same Mobile web screen to any record screen \(sys\_sg\_form\_screen\) via the 'Record screen segments' Related List.
3.  Log in to Now Agent via an Android device.
4.  Perform global search for any table corresponding to the record screen and open that record.
5.  Select the Mobile web screen tab.
6.  Scroll to the bottom and scroll up.

Expected behavior: The page scrolls up. Actual behavior: The page performs a pull-down refresh.

</td></tr><tr><td>

Mobile Android

 PRB1888119

</td><td>

In Virtual Agent, topic source links are redirected to a 'Record not found' page on mobile

</td><td>

When the user receives the a response and tries to open a topic-related source link, they are redirected to a 'Record not found' page.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1853769

</td><td>

Attachments are missing in questionnaires if the user saves the input form first and submits it later

</td><td>

The filled data and attachment should be present in a submitted questionnaire, but they are missing from the questionnaire upon submission.

</td><td>

1.  Log in to the instance.
2.  Open WOT.
3.  Open the questionnaire form, fill in the details, and select an attachment.
4.  Without selecting **Submit**, press the **Back** button.
5.  Wait for a message that says something like 'The form is saved locally'.
6.  Select a questionnaire.

Observe that the form is loaded with the previously filled data and attachment.

7.  Select **Submit**.

 Expected behavior: The filled data and attachment should be present in a submitted questionnaire.

 Actual behavior: The attachment is missing.

</td></tr><tr><td>

Mobile Android

 PRB1848008

</td><td>

There is a delay when the Next button is activated/deactivated on an input form screen allows the bypass of a required field validation

</td><td>

When a required field on input form screen is populated and then cleared there is a delay before the **Next** button on the page is deactivated. Due to this delay it is possible for the user to quickly select the **Next** button and navigate to the next page. This means it will then be possible for the record to be saved with a null value in the field that was configured to be required.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1872812

</td><td>

Connection timeout when connecting to an instance

</td><td>

When connecting to an instance, an exception occurs after 10 seconds.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1890812

</td><td>

The Virtual Agent bot display name does not appear correctly for all message types

</td><td>

 

</td><td>

1.  Navigate to the Home launcher.
2.  Select the chat icon located in the lower right.

Observe that the Virtual Agent avatar icon name is 'Virtual Agent @'.

3.  Select **Start a new conversation**.
4.  Type 'I need a laptop'.
5.  Select \(catalog\) Loaner laptop.

 Expected behavior: 'Virtual Agent @' appears for all messages.

 Actual behavior: Virtual Agent has changed its name to 'Virtual Agent'.

</td></tr><tr><td>

Mobile Android

 PRB1881465

</td><td>

The scanner fails to display the tracking number field

</td><td>

The tracking number field does not display.

</td><td>

1.  Log in to the Agent app.
2.  Select Outbound under the Warehouse section of Asset tab.
3.  Enter any number or text on the **Space** field under the 'Prepare for Outbound' screen and select **Next** while the keyboard remains open.

 Expected behavior: The tracking number field should be displayed.

 Actual behavior: The tracking number field does not display.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Mobile Agent - BlackBerry app version history](../agent-blackberry-available-versions.md)

