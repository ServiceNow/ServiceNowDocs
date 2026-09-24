---
title: Default data privacy configurations
description: Data Privacy includes out-of-the-box default configurations that automatically activate for licensed Vault customers, providing immediate value without requiring setup. These configurations enable discovery of existing sensitive data and real-time alerting and user logs for new sensitive data entries in specific fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/default-data-privacy-configurations-overview.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Data Privacy, Platform Privacy]
---

# Default data privacy configurations

Data Privacy includes out-of-the-box default configurations that automatically activate for licensed Vault customers, providing immediate value without requiring setup. These configurations enable discovery of existing sensitive data and real-time alerting and user logs for new sensitive data entries in specific fields.

The Vault by Default initiative solves a critical adoption challenge: licensed Vault customers often delay implementing data privacy protections because the setup process is time-consuming and requires configuration across multiple product modules. By providing intelligent default configurations, customers derive immediate value from Data Privacy upon Store App installation and license activation—before completing any manual setup.

## Default alerting policy

The **default alerting policy** monitors new sensitive data entry in real-time:

-   **When:** Activates automatically upon Data Privacy Store App installation for all licensed Vault customers.
-   **What:** Detects seven sensitive data types: Email, Social Security Numbers, Dates of Birth, and four major credit card types \(VISA, Discover, American Express, Mastercard\).
-   **Where:** Monitors Task table, Work\_notes, and Comments fields.
-   **How:** Generates real-time alerts to the users when the sensitive data is detected, without blocking submission. Alerts and user information are logged for administrators to refer to and take action.
-   **Value:** Provides immediate visibility into sensitive data flows, enabling quick response and proactive user training

## Default discovery job

The **default discovery job** scans existing sensitive data on the instance automatically and sends an email notification to the admin

-   **When:** Runs automatically for trial customers and new and existing licensed ServiceNow Vault customers.
-   **What:** Scans 10,000 random records using predefined data patterns.
-   **Where:** Targets the following tables and respective fields:
    -   Incident \(description, short\_description, comments, work\_notes, close\_notes\)
    -   sc\_req\_item \(via sc\_item\_option\_mtom and question\_answer\)
    -   sc\_task \(comments, work\_notes\)
    -   sn\_customer\_service\_case and interaction \(comments, work\_notes\)
    -   sn\_hr\_core\_case and scoped children \(comments, work\_notes\).
-   **Frequency:** Runs only once.
-   **Value:** Delivers an immediate baseline of sensitive data exposure, establishing the foundation for classification and data governance

## Related topics

For more information on individual default configurations, see:

-   [Default data discovery job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-classic/vault-by-default-discovery-job-overview.md) — Overview of the default discovery job that scans existing sensitive data.
-   [Default alerting policy for sensitive data entry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-classic/default-alerting-policy-overview.md) — Overview of the default alerting policy that monitors new sensitive data entry.

To learn how to work with these configurations, see the task topics within each feature overview.

