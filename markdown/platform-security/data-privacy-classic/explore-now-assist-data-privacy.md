---
title: Data Privacy for ServiceNow Otto
description: Data Privacy for ServiceNow Otto masks sensitive data in AI calls \(prompts, skills, and agentic executions\) to protect them from exposure to the large language models, including third-party \(3P\) models. This does not include MoveWorks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/explore-now-assist-data-privacy.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Data Privacy for ServiceNow Otto, Data Privacy, Platform Privacy]
---

# Data Privacy for ServiceNow Otto

Data Privacy for ServiceNow Otto masks sensitive data in AI calls \(prompts, skills, and agentic executions\) to protect them from exposure to the large language models, including third-party \(3P\) models. This does not include MoveWorks.

## How data masking works

Sensitive data can be masked so that it is not sent to large language models \(LLMs\) during AI calls. Placeholder text and anonymized data are sent with the calls instead. These values are replaced with the original text after the LLM response has been received. This two-way masking helps ensure that end users receive accurate responses, but sensitive data is not exposed to the LLMs.

Data Privacy protects ServiceNow Otto calls by anonymizing sensitive data before it reaches LLMs. Protection works in two ways:

-   Regular expression \(regex\)-based detection — Pattern matching configured on any base system data patterns or custom regular expression \(regex\) data patterns that you create. This is a base system capability and does not require a ServiceNow Vault license.
-   Named Entity Recognition \(NER\) — A machine-learning service that detects entities like person names, companies, gender, and locations. It also detects other types of sensitive data that regex patterns alone cannot reliably find. This requires a ServiceNow Vault license.

There are some considerations for configuring Data Privacy for ServiceNow Otto. See [Configure Data Privacy for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-classic/configure-now-assist-data-privacy.md) for configuration details.

Check your entitlements to determine whether you have access to NER data pattern detection and masking during AI calls and executions.

**Warning:**

-   A Vault license is not required to configure Regular Expression \(regex\) data patterns for detecting and masking structured sensitive data during AI calls. For example, when the Gen AI Controller makes calls to any LLM. If you see any Licensing and Start Trial messages in the UI, ignore them and proceed with configuring the policy.
-   A valid ServiceNow Vault license is required to configure Named Entity Recognition \(NER\) contextual data patterns for detecting and masking unstructured sensitive data during AI calls and executions.

