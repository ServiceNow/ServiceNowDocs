---
title: Dial pad for voice calls
description: The dial pad on the voice call widget lets users send digits during a connected voice call. Use it to answer an automated prompt or enter a PIN.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/portal-phone-widget-dial-pad.html
release: brazil
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 2
keywords: [dial pad, DTMF, voice call widget, WebRTC, IVR, portal]
breadcrumb: [Voice call widget, Configure voice, Configure omnichannel, Configure, Customer Service Management]
---

# Dial pad for voice calls

The dial pad on the voice call widget lets users send digits during a connected voice call. Use it to answer an automated prompt or enter a PIN.

During a voice call placed from the portal or Engagement Messenger, users can select digits on the dial pad to respond to automated prompts. Prompts include choosing a menu option or entering a PIN to authenticate. The dial pad control appears in the call controls while a call is connected.

\[Omitted image "webrtc-dial-pad.png"\] Alt text: Dial pad showing a 12-key keypad and a display area for entered digits.

## Dial pad features

The dial pad includes the following features:

-   The dial pad is available only during a connected voice call.
-   The keypad has 12 keys: the digits 0 through 9, an asterisk, and a number sign. Keys 2 through 9 and key 0 also show letters.
-   While the dial pad is open, users can press keys on their keyboard instead of selecting them on screen.
-   Digits are sent one at a time, in the order they are pressed, as each digit is selected. There's no **Enter** button.
-   The display area of the dial pad shows the digits as they are pressed. This area is read-only, so users can't type into it or edit its contents, and it shows the 20 most recent digits.
-   If the same call is open in more than one browser tab, each tab's dial pad shows only the digits entered in that tab. All digits are sent to the call. For example, a user presses 1 in the first tab, 2 in the second tab, and 3 in the first tab. All three digits are sent, but the first tab shows only 1 and 3, and the second tab shows only 2.
-   The digits clear when a call ends and when a new call starts.
-   The dial pad doesn't place outgoing calls. Users can't enter a phone number on the dial pad and start a call from it.

**Related topics**  


[Enable WebRTC for Voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget.md)

[Guest user support for portal voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget-guest-users.md)

