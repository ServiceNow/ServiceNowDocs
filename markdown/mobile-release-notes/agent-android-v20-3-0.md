---
title: Mobile Agent for Android v20.3.0
description: The Android v20.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for Android v20.3.0

The Android v20.3.0 release provides fixes for the application.

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

Android Mobile

 PRB1918113

</td><td>

The user is unable to add photos when selecting the **Open Gallery** button from the portal widget using the input type='file'

</td><td>

When a MESP page contains an HTML input with type='file', selecting images via **Open Gallery** produces the error, 'Could not read the file'.

</td><td>

1.  Create a widget with an input field.
2.  Create a portal page to include the widget.
3.  Configure a mobile function to open the MESP portal page in Now Mobile.
4.  In Now Mobile Android, open the MESP page and select **Choose Files** from the HTML input.
5.  Select **Open Gallery** and then select any photo.

 Expected behavior: The selected photo should be shown next to the input field.

 Actual behavior: No photo is selected and there is an error reading, 'Could not read the file'.

</td></tr><tr><td>

Android Mobile

 PRB1913659

</td><td>

Decimal values do not calculate totals on Portuguese-language instances

</td><td>

A field that calculates cost based on quantity and per-unit price does not calculate correctly when the device language is set to Portuguese.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1924628

</td><td>

Incorrect translation of the logout message on French instances

</td><td>

When a French-language session expires, the message, 'You are not logged in, or your session has expired.', is not translated to French.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1905617

</td><td>

The **Create WOT button** is not grayed out when conditions are not met

</td><td>

The **Create WOT** button is not grayed out like it should be.

</td><td>

1.  Provision a base Agent Mobile instance.
2.  Navigate to **More** &gt; **My Work** &gt; **See all**.

 Notice that the Create WOT button is not grayed out.

</td></tr><tr><td>

Android Mobile

 PRB1923551

</td><td>

Infinite 'Loading' state when the user initiates a Virtual Agent conversation

</td><td>

When the user initiates a Live Agent chat from Virtual Agent, then exits it by starting a new conversation, they observe a 'Loading / Routing to live agent' indicator.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](../agent-available-versions.md)

