---
title: Mastercard Spoke release notes
description: Version history for the Mastercard Spoke application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-mastercard-spoke.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Mastercard Spoke release notes

Version history for the Mastercard Spoke application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.1 - December 2025**
    -   New: First Party Trust Evidence Support: Added support for acknowledging first party trust evidence input flag when creating second first chargeback \(CB\), aligning with Mastercard API updates from October 2024 to properly handle First Party Trust \(FPT\) scenarios.
    -   Changed: Take Action on Existing Claim Enhancements: Improved validation and processing for taking action on existing claims with Enhanced validation logic for conditional mandatory fields.
        -   Translation Updates: Updated translations for the store app across all supported languages to ensure consistent localization.
    -   Fixed: ACL Failures: Fixed Access Control List \(ACL\) failures by removing problematic test code that was causing authorization issues.
-   **Version 4.0.0 - August 2025**
    -   New:
        -   Added spoke for health check of Mastercard server
        -   Added spokes for case filing
    -   Changed:
        -   Deprecated Lookup chargeback documents spoke and built them as request builder and response parser to support tokenization
        -   Added PageCount output variable for queue response parser spoke
    -   Fixed: Removed caseId getting passed in request payload in Take action on case spoke
-   **Version 3.0.0 - May 2025**

    The Mastercard spoke allows ServiceNow to connect with Mastercard's REST APIs, providing customers quick access to payment, security, data, and loyalty services. Customers can use the spoke to search transactions, create claims and chargebacks, and perform other functions with improved security. It also enables them to resolve disputes, access data, and utilize other features. By integrating with the ServiceNow platform and other spokes, customers can create more complex workflows to fit their needs.

-   **Version 2.0.3 - February 2025**

    The Mastercard spoke allows ServiceNow to connect with Mastercard's REST APIs, providing customers quick access to payment, security, data, and loyalty services. Customers can use the spoke to search transactions, create claims and chargebacks, and perform other functions with improved security. It also enables them to resolve disputes, access data, and utilize other features. By integrating with the ServiceNow platform and other spokes, customers can create more complex workflows to fit their needs.


