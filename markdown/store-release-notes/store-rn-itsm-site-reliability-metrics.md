---
title: Site Reliability Metrics release notes
description: Version history for the Site Reliability Metrics on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-site-reliability-metrics.html
release: store
topic_type: reference
last_updated: "2023-11-02"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Site Reliability Metrics release notes

Version history for the Site Reliability Metrics on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.7 - November 2023**

    Fixed: Non-functional issue to resolve warnings logged during activation of this application.

-   **Version 2.1.5 - May 2023**

    New: Updated backend functionalities.

-   **Version 2.1.4 - February 2023**

    Added support for the Utah release.

-   **Version 2.1.4 - January 2023**

    Added support for the Utah release.

-   **Version 2.1.3 - March 2022**

    New: Added support for the San Diego release.

-   **Version 2.1.2 - July 2021**
    -   New: Additional Integration Support \(New Relic and Datadog\) Lookback Capability Additional Error Budget Policy Actions \(On-Call, Slack, and Microsoft Teams\) Updated Change Approval Policy Support for Dynamic CI groups
    -   Known Errors: Reliability indicator data is not automatically saved on a switch to the Error Budget Policy tab without saving
    -   Service Level Indicator field overview:
        -   Describing the SLI with an easily identifiable text phrase Setting SLI type from the list \(options: latency, saturation, error, and availability\)
        -   The Service field is read-only to give SRE context
        -   The Name field is one of the most critical fields when it comes to setup.
        -   This name is the unique identifier that must match the SLI name exactly
        -   The Source field should point at the integration for this SLI
        -   The expression represents that SLI property set in the APM tool
-   **Version 2.0.4 - April 2021**

    New: Site Reliability Metrics \(SRM\) is an application that captures application performance signals from APM tools, typically referred to as Service Level Indicators \(SLIs\). The SRM application then allows for the creation of Service Level Objectives \(SLOs\), Error Budgets \(EB\) and policy based actions.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

