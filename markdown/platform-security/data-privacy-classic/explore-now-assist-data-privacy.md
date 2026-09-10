---
title: Exploring Data Privacy for ServiceNow Otto
description: Learn more how Data Privacy for ServiceNow Otto enhances your ability to protect sensitive data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/explore-now-assist-data-privacy.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Privacy for ServiceNow Otto, Data Privacy, Platform Privacy]
---

# Exploring Data Privacy for ServiceNow Otto

Learn more how Data Privacy for ServiceNow Otto enhances your ability to protect sensitive data.

## Data Privacy for ServiceNow Otto overview

Personally identifiable information \(PII\) can be masked so that it does not get processed from generative AI prompts. Placeholder text and anonymized data are sent with the prompt instead. These values are replaced with the original text after the large language learning module \(LLM\) response has been received. This two-way masking ensures that end users receive accurate responses, but sensitive data is not exposed to the LLM.

There are some considerations for configuring Data Privacy for ServiceNow Otto. See [Configuring Data Privacy for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/configure-now-assist-data-privacy.md) for configuration details.

**Important:**

Data Privacy for ServiceNow Otto detects and masks sensitive data based on Regex patterns and does not support contextual\(model-type\) data patterns

