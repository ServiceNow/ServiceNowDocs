---
title: PhishTank integration release notes
description: Version history for the Security Operations PhishTank integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-phish-tank.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# PhishTank integration release notes

Version history for the Security Operations PhishTank integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.0 - August 2024**

    Changed: Migrated enrichment workflows to flow designer.

-   **Version 10.4.2 - February 2023**

    New: Updated to support Security Incident Response workspace.

-   **Version 10.4.0 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.3.3 - February 2021**

    Changed: The PhishTank configuration now requires you to enter the Username \(developer account created in PhishTank\), the API key you obtained from the PhishTank website, and the configuration name.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support Integration capability framework v2.0

-   **Version 1.0.0 - February 2018**
    -   Threat intelligence lookups are run upon incident creation on potential phishing site URLs.
    -   After the application is configured, the workflow launches automatically, and lookup execution and completion status is recorded in work notes on the Security Incident form.
    -   Observables can be looked up manually by adding them to the Security Incident form and launching workflows.
    -   Results are displayed in the Threat Lookup Results tab at the bottom of the Security Incident form.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

