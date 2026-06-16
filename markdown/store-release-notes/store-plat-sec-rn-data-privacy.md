---
title: Data Privacy release notes
description: Version history for the Data Privacy application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-plat-sec-rn-data-privacy.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ServiceNow AI Platform Security release notes, ServiceNow Store release notes]
---

# Data Privacy release notes

Version history for the Data Privacy application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.1.1 - March 2026**
    -   Real-time alerting and blocking of sensitive data: Analyze user input in real time at the field level to identify sensitive data and alert users about potential sensitive data entry. You can also choose to block users from saving this information.
    -   Data logs for real-time sensitive data: Leverage real-time alerting and blocking capabilities to obtain insights into where sensitive data is being entered into the instance and by which users during interactive sessions.
    -   Real-time sensitive data-scanning for attachments: Scan attachments for sensitive data during user uploads into fields. If sensitive data is detected, the attachment is quarantined. This restricts the access and download of the file to the original document owner and authorized users until the admin reviews the files.
    -   Anonymization support for catalog variables: Anonymize sensitive data in catalog items \(including record producers\) using anonymization jobs \(in production and during cloning\).
    -   Condition-based data anonymization: Optional condition filter when running anonymization jobs to fine tune the scope of data to be anonymized
    -   Enhanced anonymization reporting: Demonstrate defensible compliance to regulators, auditors and internal teams using the new anonymization dashboard to provide quantitative insights into anonymization and data protection operations.
-   **Version 7.0.1 - February 2026**
    -   Detect and mask sensitive data during agent and requester conversations using Data Privacy for Virtual Agent
    -   AI/ML based data patterns for intelligent anonymization of sensitive data that is already on the platform
    -   Recurring data anonymization jobs
    -   Error logging to track and triage errors from anonymization jobs
    -   Anonymization of encrypted fields
-   **Version 6.0.1 - February 2026**

    View anonymized journal fields in Classic UI

-   **Version 7.0.0 - August 2025**
    -   Detect and mask sensitive data during agent and requester conversations using Data Privacy for Virtual Agent
    -   AI/ML based data patterns for intelligent anonymization of sensitive data that is already on the platform
    -   Recurring data anonymization jobs
    -   Error logging to track and triage errors from anonymization jobs
    -   Anonymization of encrypted fields
-   **Version 6.0.0 - February 2025**

    View anonymized journal fields in Classic UI.

-   **Version 5.0.1 - August 2024**

    Data Privacy for real time, support for journal fields.

-   **Version 3.0.1 - February 2024**
    -   Data pattern anonymization
    -   Real time Anonymization APIs support
-   **Version 2.0.0 - November 2023**

    New: Ability to pick groups for user data anonymization to support Right to be forgotten use case.

-   **Version 1.0.0 - February 2023**

    Provides organizations the ability to classify and anonymize sensitive data in production and sub-production environments based on various global, regional, and industry data privacy regulations.


