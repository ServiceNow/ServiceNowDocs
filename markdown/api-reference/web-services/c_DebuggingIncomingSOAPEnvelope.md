---
title: Debug incoming SOAP envelope
description: To capture incoming SOAP envelope XML in the system log, add the property glide.processor.debug.SOAPProcessor with a value of true.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Debug incoming SOAP envelope

To capture incoming SOAP envelope XML in the system log, add the property **glide.processor.debug.SOAPProcessor** with a value of **true**.

When enabled, this property adds the incoming SOAP envelope in the **Message** field of the system log \(**System Logs** &gt; **All**\). Disable this debugging feature as soon as you are finished so that the log is not overwhelmed with excessive and unnecessary debugging information.

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

