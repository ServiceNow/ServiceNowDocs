---
title: Supported user input controls for WhatsApp on NextWave
description: User input controls that capture customer responses during Virtual Agent conversations through the WhatsApp Direct Integration channel on the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-user-inputs.html
release: brazil
topic_type: reference
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, user input, Virtual Agent, NextWave, LLM]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Supported user input controls for WhatsApp on NextWave

User input controls that capture customer responses during Virtual Agent conversations through the WhatsApp Direct Integration channel on the NextWave off-Glide architecture.

When a Virtual Agent topic prompts a customer for input through WhatsApp on NextWave, the following controls are available. Several controls use LLM-assisted matching to interpret natural-language customer responses.

|Control|Description|Rendering|LLM-assisted|
|-------|-----------|---------|------------|
|Text input|Captures free-text customer responses. If LLM entity extraction is enabled, the system processes the free-text response to extract relevant entities.|Standard WhatsApp text prompt|Optional \(entity extraction\)|
|Boolean|Captures a yes/no \(true/false\) customer response. Renders as native buttons where the Cloud API supports them, or as LLM-parsed free text otherwise. Ambiguous responses trigger a re-prompt.|Native buttons or text prompt|Yes \(natural-language interpretation\)|
|Static choice|Presents a fixed, predefined list of options. Renders as a native list-picker or button UI. Unstructured text responses are handled through LLM-assisted matching or a re-prompt.|Native list-picker or buttons|Yes \(unstructured text matching\)|
|Dynamic choice|Generates an option list at runtime from a table or reference query. Large option sets are paginated or truncated within WhatsApp Cloud API list-size limits. Empty or failed queries display a fallback message.|Native list-picker|No|
|Carousel|Presents multiple selectable items as distinct browsable cards with images and text. Large item sets are paginated or truncated according to Cloud API limits. Media items follow WhatsApp size and format constraints.|Browsable card set|No|
|Input collector|Uses generative AI to collect and structure user data within a conversation flow. Supports multi-turn exchanges within the same collector. Errors or unparseable responses trigger a fallback.|Conversational text prompts|Yes \(data collection and structuring\)|
|File picker|Prompts the customer to send a file. Supported file types and size limits are governed by WhatsApp Cloud API constraints. Files that do not meet constraints are rejected with a message to the customer.|File-sharing prompt|No|
|Grouped choice|Presents a set of categorized or grouped selectable options. Selections are captured and processed as structured input.|Categorized option list|No|
|Secure text|Requests sensitive information from the customer and masks it appropriately. Sensitive data is captured securely without exposure during input.|Masked text input|No|

