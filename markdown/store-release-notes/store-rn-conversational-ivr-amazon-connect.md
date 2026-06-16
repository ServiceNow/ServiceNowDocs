---
title: Conversational IVR with Amazon Connect release notes
description: Version history for the Conversational IVR with Amazon Connect application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-conversational-ivr-amazon-connect.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Conversational IVR with Amazon Connect release notes

Version history for the Conversational IVR with Amazon Connect application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.4 - March 2026**
    -   New: Granular Admin Directive changes for va-amazon-connect
    -   Fixed: Fixed a few defects
-   **Version 1.6.3 - August 2025**

    IVR is reading out time by vocalising colons and zeros \(e.g., if the input is 8am it reads in response as, '8:00:00' as 'eight colon o o colon o o'\)

-   **Version 1.6.2 - February 2025**
    -   New: Improved interactive voice response with Now Assist.
    -   Fixed:
        -   Synthesized response is not generating properly in conversational IVR
        -   Adding translations to the store app
-   **Version 1.6.0 - November 2024**

    Updated AWS resources to use latest runtimes.

-   **Version 1.5.0 - February 2024**
    -   Fixed: Random error thrown while configuring Amazon connect information admin page when amazon connect credentials are not configured. va-api-amazon-connect-ivr-test\(softpin/softpin+mfa\) tests are failing due to SoftPIN Verification topic not available on track/nowassist.
    -   Changed: \[AWA Voice Routing\] - Update references of 'sn\_va\_as\_service\_cc\_agent\_mapping' table in VA Amazon Connect Plugin.
-   **Version 1.4.0 - November 2023**

    Minor fixes.

-   **Version 1.2.1 - February 2023**
    -   New:
        -   Use Virtual Agent topics as a conversational-IVR to enable deflection in Phone channels, providing consistent end-user experience.
        -   Enable true-omnichannel flow including routing Phone to VA-IVR.
        -   In case of escalations, route calls smoothly to live agents using AWA via conversational infrastructure.

**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

