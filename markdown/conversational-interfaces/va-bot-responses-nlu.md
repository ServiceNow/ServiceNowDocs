---
title: \(Legacy\) Virtual Agent Designer bot response channel support for NLU
description: Virtual Agent Designer offers various controls for displaying bot responses in a conversation. Because the bot responses occur in third-party platforms, the format for each output may vary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-bot-responses-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Virtual Agent Designer bot response channel support for NLU

Virtual Agent Designer offers various controls for displaying bot responses in a conversation. Because the bot responses occur in third-party platforms, the format for each output may vary.

The following tables describe channel support for each NLU bot response control.

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Supported|Plain text string only|
|SMS Twilio|Supported|None|
|LINE|Supported|None|
|WhatsApp|Supported|None|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Supported|For screen devices, full support. For nonscreen devices, the header is read.|

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|The maximum image size is determined by the **com.glide.attachment.max\_size** system property. The default value is 1024 MB.|
|Mobile UI|Supported|The maximum image size is determined by the **com.glide.attachment.max\_size** system property. The default value is 1024 MB.|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|For details about the maximum image size allowed, check the Slack documentation.|
|Workplace|Supported|For details about the maximum image size allowed, check the Workplace documentation.|
|Facebook Messenger|Supported|For details about the maximum image size allowed, check the Facebook Messenger documentation.|
|SMS Twilio|Supported|File size limits may vary. For Twilio limitations, check their [Accepted Content Types for Media](https://www.twilio.com/docs/sms/accepted-mime-types).|
|LINE|Supported|File size limits may vary. For details, see the LINE documentation.|
|WhatsApp|Supported|File size limits may vary. For details, see the WhatsApp documentation.|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found an image`. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Supported|The web link appears as a [URL button](https://developers.facebook.com/docs/messenger-platform/send-messages/buttons#url) in the conversation.|
|SMS Twilio|Supported|None|
|LINE|Supported|None|
|WhatsApp|Supported|None|
|Apple Messages for Business|Supported|Any URLs must be added to the allowed domain list \[sys\_cs\_hostname\_allow\_list\] table.|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found a link`. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Supported|None|
|Microsoft Teams|Supported|Since HTML is rendered as an image in Microsoft Teams, other controls are recommended. For example, use images or cards instead of HTML for Microsoft Teams.|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the user receives a message: `We found a link`. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For non-screen devices, the user receives a message if unsupported elements are used: `We found a link`. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Not supported|Not applicable|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Not supported|Not applicable|
|Alexa \(Voice\)|Partial support|Support depends on the type of response. For example, images and links may only be available on devices with screens. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

<table id="table_yqr_3fp_tsb"><thead><tr><th>

Channel

</th><th>

Support

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

Web UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Mobile UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Now Assist panel

</td><td>

Partial support

</td><td>

Record cards and record cards with action only.

</td></tr><tr><td>

Microsoft Teams

</td><td>

Supported

</td><td>

The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Slack

</td><td>

Supported

</td><td>

Conversational Integration with Slack Version 2.0.0 and later.The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Workplace

</td><td>

Partial support

</td><td>

Image card output not available.Facebook apps no longer support vertical list templates. The card layout uses a horizontal, scrollable carousel template effective August 15, 2019. Cards also feature a button template.

</td></tr><tr><td>

Facebook Messenger

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

SMS Twilio

</td><td>

Supported

</td><td>

Records and image cards only.

</td></tr><tr><td>

LINE

</td><td>

Partial support

</td><td>

Records and image cards only.

</td></tr><tr><td>

WhatsApp

</td><td>

Partial support

</td><td>

Records and image cards only.

</td></tr><tr><td>

Apple Messages for Business

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Alexa \(Voice\)

</td><td>

Partial support

</td><td>

Some types of output are only available on devices with screens. For nonscreen devices, the card title is read. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).

</td></tr></tbody>
</table>|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Supported|None|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the table will be read, if possible. For details, see [\(Legacy\) Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-settings-for-alexa.md).|

<table id="table_ttn_s5w_tsb"><thead><tr><th>

Channel

</th><th>

Support

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

Web UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Mobile UI

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Now Assist panel

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Microsoft Teams

</td><td>

Supported

</td><td>

The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Slack

</td><td>

Supported

</td><td>

Conversational Integration with Slack version 2.0.0 and later.The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

</td></tr><tr><td>

Workplace

</td><td>

Supported

</td><td>

None

</td></tr><tr><td>

Facebook Messenger

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

SMS Twilio

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

LINE

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

WhatsApp

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Apple Messages for Business

</td><td>

Not supported

</td><td>

Not applicable

</td></tr><tr><td>

Alexa \(Voice\)

</td><td>

Not supported

</td><td>

Not applicable

</td></tr></tbody>
</table>**Parent Topic:**[\(Legacy\) Virtual Agent Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-reference-nlu.md)

