---
title: Data Privacy release notes
description: The ServiceNow Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Data Privacy release notes

The ServiceNow® Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Zurich release.

## Data Privacy highlights for the Zurich release

-   Use a revamped Data Discovery interface, enhancing your Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first-time users.
-   Target scans on specific table columns for discovery using column-level discovery and expanded support for Field Encryption.
-   Discover PII in Microsoft Excel and CSV files with expanded file support.
-   Generate regex patterns using prompts with the text-to-regex feature, which leverages Now Assist and supports all large language models \(LLMs\) approved by ServiceNow.

See [Platform Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/privacy-landing-page.md) for more information.

**Important:** Data Privacy is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[New Data Discovery experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/data-discovery-landing.md)**

    Use the new Data Discovery experience, which simplifies the experience of discovering and anonymizing PII.

-   **[Column-level discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/granular-configuration.md)**

    Select a specific column of a table for granular scanning during data discovery jobs.

-   **[Anonymization of encrypted field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/dps-data-anonymization.md)**

    Anonymize encrypted columns to help you achieve compliance with data privacy regulations and defense-in-depth data protection.


## Changed in this release

-   **[Full scan support added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/configure-data-discovery-jobs.md)**

    Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/data-discovery-attachment-scanning.md)**

    Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/configure-data-discovery-patterns.md)**

    Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


-   **Key word matching**

    As part of key word matching when discovering sensitive data using regex, more precise data pattern matching has been implemented, using full strings of text. This may require customers to add more specific variants of keywords to achieve the same level of discovery precision as prior platform releases


## Activation information

Data Privacy is available with activation of the Data Privacy plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/dps-activate-data-privacy.md).

**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-security-rn-landing.md)

