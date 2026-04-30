---
title: About Security Control Lists in TISC
description: Security Control Lists \(SCLs\) are predefined classification list that helps the Threat Intelligence Analysts determine how observables should be treated within the application and across security tools.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# About Security Control Lists in TISC

Security Control Lists \(SCLs\) are predefined classification list that helps the Threat Intelligence Analysts determine how observables should be treated within the application and across security tools.

Threat Intelligence Analysts can categorize the observables by adding them to specific security control lists such as allow list, deny list, or watch list.

The categorization of observables into security control lists enables automated decision-making and filtering throughout the TISC.

The following lists describes the various methods for using the SCLs categorization to filter observables:

-   Applying inbound filtering rules to filter out observables based on security control lists, typically against the allow list.
-   Exporting data from the observable lists of the threat intelligence library.
-   Sending observables for blocking or unblocking in firewall tools that are integrated with TISC.
-   Sending observables to monitor SIEM integrated applications with TISC, specifically against the watch list category.
-   Using automation flows and email notifications such as not notifying the analysts during ingestion if the observable is in the deny list.
-   Filtering based on these fields when using the TISC API for integration.

