---
title: Data Privacy release notes
description: The ServiceNow Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Data Privacy release notes

The ServiceNow® Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Xanadu release.

## Data Privacy highlights for the Xanadu release

-   Navigate an improved Data Privacy and Data Discovery UI in Next Experience dashboards.
-   Discover and anonymize sensitive data as it's entered with the real-time anonymization policy.
-   Anonymize and discover journal fields with expanded support and an increased data pattern regular expression limit of up to 1000 characters.

See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

## Important information for upgrading Data Privacy to Xanadu

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

## New in the Xanadu release

-   **[Child job execution](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Run child parallel jobs to optimize the duration of your job executions.

-   **[Encrypt with column level encryption \(CLE\)](https://www.servicenow.com/docs/access?context=data-classification&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    As a security admin, view whether the discovery field is encrypted or can be encrypted.


## UI changes

-   **[Next Experience dashboards](https://www.servicenow.com/docs/access?context=data-discovery&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Data Discovery and Data Privacy Dashboards now use the Next Experience dashboards.


## Changed in this release

-   **[Discover and anonymize journal fields](https://www.servicenow.com/docs/access?context=classifying-data&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Journal fields are now supported for Data Discovery and Data Anonymization with Workspace UI.

-   **[Data pattern regular expression length increased](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    The data pattern regular expression length limit is increased to 1000 characters.

-   **[New base system data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    New base system data patterns are supported. See [Default data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

-   **Indicators for Security Center dependencies**

    Indicators for missing Security Center dependencies have been added.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

