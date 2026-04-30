---
title: Public URLs
description: On-premise customers should ensure that the URLs are accessible from the Internet for the Notify-Twilio driver to work correctly.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Public URLs

On-premise customers should ensure that the URLs are accessible from the Internet for the Notify-Twilio driver to work correctly.

The Notify-Twilio drivers \(both new and old\) require that specific URLs on the instance be accessible from the Internet by the Twilio server without authentication. If the instance is within a private network, you need to either port forward or set up a reverse proxy.

For the Notify-Twilio driver, the URLs are:

-   /NotifyTwilioCallProcessor.do
-   /NotifyTwilioCallStatusProcessor.do
-   /NotifyTwilioSMSProcessor.do
-   /NotifyTwilioDialStatusProcessor.do
-   /NotifyTwilioEventProcessor.do
-   /NotifyTwilioDialProcessor.do
-   /NotifyTwilioRecordingProcessor.do

For the Notify-Twilio Direct driver, the URLs are:

-   /api/sn\_twilio\_direct/twilio\_callbacks/process/twiml/\{callback\_name\}
-   /api/sn\_twilio\_direct/twilio\_callbacks/process/xml/\{callback\_name\}

**Note:** The **glide.notify.endpoint** property needs to be set to an Internet visible name because the instance name inside a private network can be different from the Internet domain.

**Parent Topic:**[Notify reference](notify-reference-section.md)

