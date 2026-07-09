---
title: Data Privacy release notes
description: The ServiceNow Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Data Privacy release notes

The ServiceNow® Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Yokohama release.

## Data Privacy highlights for the Yokohama release

-   Leverage Data Privacy in Now Assist to discover sensitive data in Now Assist prompts and data send to models.
-   Sanitize sensitive data from Now Assist prompts without impacting response.
-   Discover sensitive data from attachments using enhanced Data Discovery jobs.

See [Platform Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/privacy-landing-page.md) for more information.

**Important:** Data Privacy is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Data Privacy to Yokohama

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

## New in the Yokohama release

-   **[AL/ML Based Data Discovery for Real Time Anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/now-assist-for-data-privacy-landing.md)**

    Use AI/ML data discovery using Named Entity Recognition \(NER\) models to discover sensitive data that does not follow a pattern like name, address, organizations, and more; and run real-time anonymization.

-   **[Configuring Data Privacy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/configure-now-assist-data-privacy.md)**

    Sanitize sensitive data entered in Now Assist prompts to prevent data leakage without impacting the response.

-   **[Discover sensitive data from attachments.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/configure-data-discovery-jobs.md)**

    Discover and report on sensitive data from attachments.


## Activation information

Data Privacy is available with activation of the Data Privacy Plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/dps-activate-data-privacy.md).

**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)

