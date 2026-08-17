---
title: WhatsApp Cloud API provider properties
description: Use provider properties to customize the behavior of the Conversational Integration with Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/whatsapp-cloud-api-provider-properties.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-07-16"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# WhatsApp Cloud API provider properties

Use provider properties to customize the behavior of the Conversational Integration with Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application.

|Property|Description|Default value|
|--------|-----------|-------------|
|**time\_format**|Controls the time format used in WhatsApp messages. Accepted values are `12` \(12-hour clock with a.m./p.m., for example 2:30 p.m.\) or `24` \(24-hour clock, for example 14:30\).|24|
|**date\_format**|Controls the date format used in WhatsApp messages. Supported formats: `MM/DD/YYYY`, `DD/MM/YYYY`, `YYYY-MM-DD`.|DD/MM/YYYY|
|**supports\_audio\_rich\_control**|Enables audio component rendering for audio file attachments. When this property is disabled, an audio attachment falls back to a link instead of an inline audio player.|True|

**Parent Topic:**[Configure Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/messg-direct-whatsapp-configure.md)

**Related topics**  


[Configure WhatsApp Cloud API provider properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-whatsapp-cloud-api-provider-properties.md)

