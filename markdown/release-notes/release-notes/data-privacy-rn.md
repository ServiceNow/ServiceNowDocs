---
title: Data Privacy release notes
description: The ServiceNow Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Data Privacy release notes

The ServiceNow® Data Privacy application enables you to classify sensitive data, remove personally identifiable information \(PII\) from user data in a production instance, and anonymize data in production and non-production instances. Data Privacy was enhanced and updated in the Australia release.

## Data Privacy highlights for the Australia release

-   Discover and block sensitive data from user inputs to prevent it from entering the platform, alert users when sensitive data is entered to raise awareness, and leverage sensitive data logs to understand where and who is entering sensitive data.
-   Scan and quarantine attachments that contain sensitive data to restrict their access and downloading.
-   Define conditions for the anonymization of sensitive data to meet business specific requirements. Use the enhanced data anonymization dashboard to obtain insights and metrics about data protection and anonymization for executive reporting.

See [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US) for more information.

**Important:** Data Privacy is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Real-time alerting and blocking of sensitive data](https://www.servicenow.com/docs/access?context=real-time-protection&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Analyze user input in real time at the field level to identify sensitive data and alert users about potential sensitive data entry. You can also choose to block users from saving this information.

-   **[Data logs for real-time sensitive data](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Leverage real-time alerting and blocking capabilities to obtain insights into where sensitive data is being entered into the instance and by which users.

-   **[Real-time sensitive data-scanning for attachments](https://www.servicenow.com/docs/access?context=attachment-quarantine-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Scan attachments for sensitive data during user uploads into fields. If sensitive data is detected, the attachment is quarantined. This restricts the access and download of the file to the original document owner and authorized users until the admin reviews the files.

-   **[New Named Entity Recognition \(NER\) model data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Employ new AI/ML-based model data patterns \(Address, City, State, Country, Job Position, and Salary\) to detect and anonymize sensitive data.

-   **[Anonymization support for catalog variables](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Anonymize sensitive data in catalog items \(including record producers\) using anonymization jobs \(in production and during cloning\).

-   **[New base system Regular Expression \(RegEx\) data patterns](https://www.servicenow.com/docs/access?context=dds-review-discovery-findings&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Employ new base system regular expression data patterns to detect and anonymize sensitive data in line with global compliance requirements.

-   **[Enhanced anonymization reporting](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Demonstrate defensible compliance to regulators, auditors and internal teams using the new anonymization dashboard to provide quantitative insights into anonymization and data protection operations.


## UI changes

-   Use the [improved anonymization dashboard](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=australia&pubname=australia-platform-security&ft:locale=en-US) to get more details about anonymization. For example, what data was anonymized and how \(real-time or through anonymization jobs\).
-   Use the new [real-time protection module](https://www.servicenow.com/docs/access?context=real-time-protection&version=australia&pubname=australia-platform-security&ft:locale=en-US) to configure real-time alerting and your blocking policies. You can also view real-time sensitive data logs.

## Changed in this release

-   **New experience**
    -   [Optional condition filter](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&version=australia&pubname=australia-platform-security&ft:locale=en-US) when running anonymization jobs to fine tune the scope of data to be anonymized.
    -   [Specific anonymization policy](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US) for catalog variables to anonymize sensitive data in catalog requests.

## Activation information

Data Privacy is available with activation of the Data Privacy plugin \(`sn_dp_store_app`\). For details, see [Activate data privacy](https://www.servicenow.com/docs/access?context=dps-activate-data-privacy&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

