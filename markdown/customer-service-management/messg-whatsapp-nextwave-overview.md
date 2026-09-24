---
title: WhatsApp Direct Integration on NextWave
description: WhatsApp Direct Integration is available on the NextWave off-Glide architecture, providing the same messaging capabilities as the Glide-based implementation with improved performance and scalability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 2
keywords: [WhatsApp, NextWave, off-Glide, omnichannel]
breadcrumb: [Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# WhatsApp Direct Integration on NextWave

WhatsApp Direct Integration is available on the NextWave off-Glide architecture, providing the same messaging capabilities as the Glide-based implementation with improved performance and scalability.

WhatsApp Direct Integration on the NextWave off-Glide architecture enables agents to provide real-time customer support through WhatsApp with rich media, interactive controls, and full Customer Service Management workflow integration. This implementation builds WhatsApp channel support natively on NextWave, achieving functional parity with the existing Glide-based behavior.

Existing customer configurations and interaction history are preserved. The NextWave architecture provides improved performance, scalability, and access to NextWave-specific features while maintaining backward compatibility.

## Supported capabilities

The WhatsApp channel on NextWave supports the following capabilities:

-   Text message exchange: Send and receive text messages between ServiceNow and WhatsApp, with conversation threading and interaction history. See [Exchange text messages through WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-text-messaging.md).
-   Media attachments: Exchange images, documents, and video links between agents and customers. See [Handle media attachments in WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-attachments.md).
-   Rich messaging controls: Request Location \(capture customer location as a map pin\), List Picker \(present selectable options\), and Typing Indicator \(display agent typing status\). See [Use rich messaging controls in WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-rich-controls.md).
-   Audio features: Customers send voice messages that agents play back in the workspace, and agents record and send voice messages where supported. See [Use audio features in WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-audio.md).
-   Bot response controls: Text, LLM-generated text, card, HTML, image, link, multi-response, script, table, and video responses from Virtual Agent conversations. See [Supported bot response controls for WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-bot-controls.md).
-   User input controls: Text input, boolean, static choice, dynamic choice, carousel, input collector, file picker, grouped choice, and secure text controls with LLM-assisted input matching. See [Supported user input controls for WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-user-inputs.md).
-   Account linking: Automatic and manual linking of WhatsApp customers to contact or consumer records. See [Set up account linking for WhatsApp on NextWave](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-whatsapp-nextwave-account-linking.md).

## Personas

The following personas interact with WhatsApp Direct Integration on NextWave:

|Persona|Role|Primary need|
|-------|----|------------|
|Customer|Sends and receives WhatsApp messages, including rich media and audio notes|Conversations feel native to WhatsApp with no missing features or broken media|
|Agent|Views and responds to WhatsApp conversations in the CRM Workspace|Full context \(attachments, location\) visible in the interaction record without switching tools|
|Administrator|Configures the WhatsApp Direct Integration channel|Existing configurations continue to work without manual re-setup after the off-Glide build goes live|

**Related topics**  


[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/messg-integrating-whatsapp-with-csm-whatsapp-cloud.md)

