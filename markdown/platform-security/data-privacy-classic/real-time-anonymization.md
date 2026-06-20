---
title: Real time anonymization
description: Use the real time anonymization\(RTA\) policy to anonymize data entries in real time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/data-privacy-classic/real-time-anonymization.html
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 1
breadcrumb: [Data privacy \(Store\), Data Privacy, Platform Privacy]
---

# Real time anonymization

Use the real time anonymization\(RTA\) policy to anonymize data entries in real time.

Users create an RTA policy through the [Anonymization Policies page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/servicenow-ai-platform-security/dps-create-anonymization-policies.md). Columns from the [target tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-discovery/configure-data-discovery-target-table.md) may be selected for RTA, whereupon [active data patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-discovery/configure-data-discovery-patterns.md) are used and their policies applied to any valid record entries to the columns targeted for RTA. If an entry matches an active data pattern its associated [anonymization technique](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/servicenow-ai-platform-security/dps-create-anonymization-techniques.md) will be used for anonymization.

**Tip:** If you need to change the anonymization technique see [Configure Data Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-discovery/configure-data-discovery-patterns.md).

## Data channels for real time anonymization

A data channel is the channel taken by your data for processing. See [Data channels for real-time anonymization policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-privacy-classic/data-channels-for-rta.md) for more information.

## Real time anonymization failures

If an RTA policy fails, you can review its status with the [Real time anonymization failures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-privacy-classic/real-time-anonymization-failures.md) table.

