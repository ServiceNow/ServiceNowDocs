---
title: Exploring Data Privacy for Now Assist
description: Learn more how Data Privacy for Now Assist enhances your ability to protect sensitive data.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Privacy for Now Assist, Data Privacy, Platform Privacy]
---

# Exploring Data Privacy for Now Assist

Learn more how Data Privacy for Now Assist enhances your ability to protect sensitive data.

## Data Privacy for Now Assist overview

Sensitive data such as age, phone number, and other personally identifiable information\(PII\) can be masked so that it does not get processed from generative AI prompts. Placeholder text and anonymized data are sent with the prompt instead, and these values are replaced with the original text after the large language learning module\(LLM\) response has been received. This two-way masking ensures that end users receive accurate responses, but sensitive data is not exposed to the LLM.

There are some considerations for configuring Data Privacy for Now Assist. See [Configuring Data Privacy for Now Assist](configure-now-assist-data-privacy.md) for configuration details.

**Important:**

Data Privacy for Now Assist detects and masks sensitive data based on Regex patterns and does not support contextual\(model-type\) data patterns

