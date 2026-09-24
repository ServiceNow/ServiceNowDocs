---
title: Default alerting policy for sensitive data entry
description: The default alerting policy automatically detects sensitive data being entered into unstructured fields in real-time and alerts administrators, providing immediate visibility into sensitive data flows without requiring configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/default-alerting-policy-overview.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 3
breadcrumb: [Default data privacy configurations, Data Privacy, Platform Privacy]
---

# Default alerting policy for sensitive data entry

The default alerting policy automatically detects sensitive data being entered into unstructured fields in real-time and alerts administrators, providing immediate visibility into sensitive data flows without requiring configuration.

The default alerting policy is part of the Vault by Default initiative to provide immediate value to licensed Vault customers upon Data Privacy Store App installation. Unlike discovery jobs that find existing sensitive data, the alerting policy monitors data entry in real-time, alerting administrators the moment sensitive information is entered into monitored fields.

The default alerting policy solves a critical visibility gap: licensed Vault customers have limited insight into what types of sensitive data users are entering in unstructured fields \(comments, notes, free text fields\). By automatically creating and activating an alerting policy upon Store App installation, customers immediately begin receiving alerts about sensitive data flows without any configuration effort.

**Key benefit:** Real-time visibility into sensitive data entry with zero setup.

## Default alerting policy specifications

The default alerting policy includes:

-   **Policy type:** Alerting-only \(does not mask, redact, or anonymize data\)
-   **Activation trigger:** Automatic upon Data Privacy Store App installation
-   **Target tables:** Task table only
-   **Target columns:** Work\_notes, Comments
-   **Sensitive data patterns:** Email, SSN, Date of Birth, Credit Cards \(4 major card types\)
-   **Action type:** Alert \(notification only\)
-   **Alert recipients:** System administrators
-   **User impact:** None—form submission proceeds normally
-   **Scope:** Applied to all users entering data in monitored fields

## Monitored tables and columns

The default alerting policy monitors the following specific locations on the instance:

|Table|Column|Field Purpose|
|-----|------|-------------|
|Task|Work\_notes|Technician or agent notes added during task resolution|
|Task|Comments|General comments field on task records|

These fields are chosen because they are unstructured, free-text fields where users commonly enter narrative information—and where sensitive data is frequently entered by accident.

## Sensitive data patterns detected

The default alerting policy detects the following seven sensitive data types:

-   **Email:** Standard email address format \(e.g., user@example.com\)
-   **Social Security Number:** 9-digit SSN pattern with or without dashes \(e.g., 123-45-6789 or 123456789\)
-   **Date of Birth:** Common date of birth formats \(various date patterns\)
-   **Credit Card - VISA:** VISA card number pattern \(typically 16 digits starting with 4\)
-   **Credit Card - Discover:** Discover card number pattern \(typically 16 digits starting with 6011\)
-   **Credit Card - American Express:** AmEx card pattern \(15 digits starting with 34 or 37\)
-   **Credit Card - Mastercard:** Mastercard pattern \(16 digits starting with 5\)

These patterns are predefined and cannot be modified in the default policy. To alert on different patterns or tables, create a custom alerting policy.

## Alert behavior and user experience

When the alerting policy detects sensitive data:

-   **Alert is generated immediately:** The alert is created and sent to administrators without delay.
-   **User is not blocked:** The user can continue entering data and submit the form normally—the alert does not prevent any action.
-   **Data is not modified:** The sensitive data is not masked, redacted, or altered; it is entered exactly as typed.
-   **Alert includes data type:** Administrators receive a notification indicating which type of sensitive data was detected.
-   **Visibility only:** The primary function is to alert and create an audit trail, not to prevent data entry.

This non-blocking design ensures the user experience is not disrupted while still providing administrators with visibility into sensitive data flows.

## Limitations and considerations

-   **Limited scope:** Policy monitors only Task table Work\_notes and Comments fields; other tables are not included.
-   **Fixed patterns:** The seven predefined patterns cannot be modified in the default policy; create a custom policy for different patterns.
-   **No pattern extension:** Cannot add additional sensitive data types to the default policy; requires custom policy creation.
-   **Alert volume:** High-volume data entry into monitored fields may generate many alerts; consider filtering or escalation rules.
-   **False positives:** Pattern matching may occasionally flag legitimate data that matches the pattern \(e.g., fake credit card numbers used for testing\).
-   **No action enforcement:** Policy alerts but does not prevent, mask, or restrict access to data.
-   **No retroactive detection:** Policy monitors new data entry only; existing data in fields is not retroactively scanned for alerts.

