---
title: Password Reset integration with Okta release notes
description: Version history for the Password Reset integration with Okta on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-password-reset-okta.html
release: store
topic_type: reference
last_updated: "2023-04-06"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Password Reset integration with Okta release notes

Version history for the Password Reset integration with Okta on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.2 - April 2023**

    Improved installation performance.

-   **Version 1.1.1 - June 2022**
    -   Fixed: Patch release of Password Reset Integration with Okta. This version includes the below changes:
        -   Added a fix script to populate base alias in credential store type.
        -   Fix for an issue with Password Expiration Subflow.
        -   Fix for User Name input that doesn't contain any pill dropped in the "Get Password Expiration Details" subflow.
-   **Version 1.1.0 - March 2022**

    New: This version includes new configuration options with a new subflow and action to support password expiration notifications.

-   **Version 1.0.2 - February 2022**

    Changed: Patch release of Password Reset integration with Okta. This version updates the dependency on Okta Spoke to the latest version.

-   **Version 1.0.1 - March 2021**
    -   New:
        -   The Password Reset with Okta application expands ServiceNow's Password Reset framework to natively support Okta. Customers no longer need to rely on the extensibility of Password Reset and manually build Okta into their processes. Administrators can now quickly and easily create new processes for Okta to allow users and service agents to unlock users and reset and change passwords, right from ServiceNow.
        -   This application leverages all the existing Password Reset capabilities including supporting multiple verification methods, enabling password policies and password strength requirements, and enabling administrators to control feature availability.

