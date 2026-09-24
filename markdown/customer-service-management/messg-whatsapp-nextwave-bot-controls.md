---
title: Supported bot response controls for WhatsApp on NextWave
description: Bot response controls that Virtual Agent can send to customers through the WhatsApp Direct Integration channel on the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-bot-controls.html
release: brazil
topic_type: reference
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, bot response, Virtual Agent, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Supported bot response controls for WhatsApp on NextWave

Bot response controls that Virtual Agent can send to customers through the WhatsApp Direct Integration channel on the NextWave off-Glide architecture.

When a customer interacts with a Virtual Agent topic through WhatsApp on NextWave, the bot can respond with any of the following controls. Controls that cannot render natively in WhatsApp provide a fallback representation.

|Control|Description|Rendering|Fallback|
|-------|-----------|---------|--------|
|Text|Sends a static or dynamically composed plain text message to the customer. Data pill and variable substitution resolves before sending.|Native WhatsApp text message|None required|
|LLM-generated text|Sends a message generated at runtime by an LLM based on the conversation context. If generation fails or times out, a fallback message is displayed.|Native WhatsApp text message|Fallback text on failure or timeout|
|Card|Presents structured card content to the customer, such as a title, description, and action.|Formatted text representation|Plain text when card cannot render|
|HTML|Sends rich HTML-formatted content to the customer.|Formatted text where supported|Plain text when HTML cannot render|
|Image|Sends an image to the customer through the WhatsApp channel.|Native WhatsApp image|None required|
|Link|Sends a clickable URL to the customer. Clicking the URL opens the intended web page or resource.|Clickable URL in the message|None required|
|Multi-response|Sends a sequence of multiple response segments to the customer. Each segment is delivered in order.|Sequential WhatsApp messages|None required|
|Script|Executes a script to generate the response sent to the customer. The script runs at runtime and produces the message content.|Depends on script output type|Depends on script output type|
|Table|Presents tabular data to the customer.|Formatted text representation|Plain text when table cannot render|
|Video|Sends a video to the customer through the WhatsApp channel.|Native WhatsApp video|None required|

