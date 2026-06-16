---
title: Vonage spoke release notes
description: Version history for the Integration Hub Vonage spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-vonage.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Vonage spoke release notes

Version history for the Integration Hub Vonage spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**

    Fixed: Streamline ACLs.

-   **Version 2.0.0 - April 2026**
    -   New:
        -   Added support for RCS messaging with new actions for text, media, and cards.
        -   Introduced new NCCO action types including Notify, Wait, Transfer, and Connect.
        -   Added new Update Application action for enhanced application management.
        -   Introduced Event Source and Event Definitions for WhatsApp and RCS.
        -   Enabled new Webhook support compatible with current version standards.
        -   Added utility script for Event Source Hash authentication.
    -   Changed:
        -   Refactored JWT token generation to support all actions consistently.
        -   Enhanced NCCO talk, conversation, and record actions for improved functionality.
        -   Updated authentication templates and alias handling for better connection management.
        -   Revamped SMS, Number, Call, and WhatsApp management categories with improved action structures.
        -   Applied label updates and incorporated review feedback across actions.
    -   Removed: Deprecated legacy actions across SMS, Number, Call, and WhatsApp management categories as part of revamp.
    -   Fixed: Resolved issues in Webhook handling and Crypto module compatibility.
-   **Version 1.2.0 - December 2025**

    Added 8 new external triggers for Vonage webhooks across Voice, SMS, and Messages APIs Voice \(Answer Webhook\): New triggers for Ringing, Answered, and Completed call states SMS Webhook: Added triggers for Delivered and Failed delivery status Message Webhook: Added triggers for Submitted, Delivered, and Undeliverable message events Implemented webhook endpoints to receive Vonage callbacks and map incoming status values to corresponding triggers Added basic validation and ensured 2xx responses for reliable Vonage webhook delivery.

-   **Version 1.1.5 - July 2025**

    Fixed: Webhook callback URL encoding.

-   **Version 1.1.4 - October 2024**

    Fix for usage of deprecated 3DES algorithm.

-   **Version 1.1.3 - June 2023**

    Fixed: Issue with Get Account Balance action.

-   **Version 1.1.2 - September 2022**

    Fixed: Improve installation performance of spoke.

-   **Version 1.1.1 - December 2021**

    New: Patch release of Vonage Spoke for IntegrationHub. This version adds support to process the response from Vonage Voice webhook sub-flow and a cosmetic fix at action - Play DTMF tone into Call.

-   **Version 1.1.0 - October 2021**

    Fixed: Security bug.

-   **Version 1.0.1 - July 2021**

    Patch release of the Vonage spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields and Rome compatibility.

-   **Version 1.0.0 - August 2020**

    Provides actions to automate the management of call, SMS, and WhatsApp in Vonage.


