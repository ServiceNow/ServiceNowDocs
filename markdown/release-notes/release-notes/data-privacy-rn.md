---
title: Data Privacy release notes
description: The ServiceNow Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Data Privacy release notes

The ServiceNow® Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Zurich release.

## Data Privacy highlights for the Zurich release

-   Use a revamped Data Discovery interface, enhancing your Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first-time users.
-   Target scans on specific table columns for discovery using column-level discovery and expanded support for Field Encryption.
-   Discover PII in Microsoft Excel and CSV files with expanded file support.
-   Generate regex patterns using prompts with the text-to-regex feature, which leverages Now Assist and supports all large language models \(LLMs\) approved by ServiceNow.

See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

**Important:** Data Privacy is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[New Data Discovery experience](https://www.servicenow.com/docs/access?context=data-discovery-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the new Data Discovery experience, which simplifies the experience of discovering and anonymizing PII.

-   **[Column-level discovery](https://www.servicenow.com/docs/access?context=granular-configuration&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Select a specific column of a table for granular scanning during data discovery jobs.

-   **[Anonymization of encrypted field](https://www.servicenow.com/docs/access?context=dps-data-anonymization&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Anonymize encrypted columns to help you achieve compliance with data privacy regulations and defense-in-depth data protection.


## Changed in this release

-   **[Full scan support added](https://www.servicenow.com/docs/access?context=configure-data-discovery-jobs&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://www.servicenow.com/docs/access?context=data-discovery-attachment-scanning&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


## Activation information

Data Privacy is available with activation of the Data Privacy plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://www.servicenow.com/docs/access?context=dps-activate-data-privacy&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

