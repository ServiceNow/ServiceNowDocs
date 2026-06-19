---
title: Real time anonymization
description: Use the real time anonymization\(RTA\) policy to anonymize data entries in real time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/data-privacy-classic/real-time-anonymization.html
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data privacy, Data Privacy, Platform Privacy]
---

# Real time anonymization

Use the real time anonymization\(RTA\) policy to anonymize data entries in real time.

## Real time anonymization Overview

Users create an RTA policy by selecting real time anonymization in the [Anonymization Policies page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-create-anonymization-policies.md), and then selecting the appropriate data channel. For example you can use Virtual Agent with real time anonymization: create an anonymization policy with the Virtual Agent selected as its **Data Channel**.

Columns from the [target tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/configure-data-discovery-target-table.md) may be selected for RTA, whereupon [active data patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/configure-data-discovery-patterns.md) are used and their policies applied to any valid record entries to the columns targeted for RTA. If an entry matches an active data pattern its associated [anonymization technique](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-create-anonymization-techniques.md) will be used for anonymization.

**Tip:** If you need to change the anonymization technique see [Configure Data Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/configure-data-discovery-patterns.md).

## Real time anonymization failures

If an RTA policy fails, you can review its status with the [Real time anonymization failures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/real-time-anonymization-failures.md) table.

