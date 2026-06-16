---
title: Salesforce spoke release notes
description: Version history for the Integration Hub Salesforce Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-salesforce-v1.2.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Salesforce spoke release notes

Version history for the Integration Hub Salesforce Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

**Note:**

For users who have installed Salesforce spoke V1, you can't upgrade from Salesforce spoke V1 to Salesforce spoke V1.2 directly. To upgrade, you must uninstall Salesforce spoke V1 and then install Salesforce spoke V1.2.

Salesforce spoke V1 is certified on New York and Salesforce spoke V1.2 is certified on Orlando and Paris.

-   **Version 2.5.0 - June 2026**

    Security patch on non-glide ACLs

-   **Version 2.4.3 - May 2026**

    Fixed: Post-ZP6HF1 platform version, payloads containing % are truncated for Create and Update Record actions, causing missing required fields and resulting in rejected requests by Salesforce

-   **Version 2.4.2 - March 2026**
    -   Fixed:
        -   Redirect URL is not auto-populated during the connection configuration.
        -   KMF module access policy.
-   **Version 2.4.1 - February 2026**

    Fixed: Missing OOB report\_view ACLs for multiple tables

-   **Version 2.4.0 - January 2026**

    Added support for client credential OAuth grant type for connection and credential alias.

-   **Version 2.3.4 - November 2025**
    -   Create "Check Service Cloud Feature" action and deprecate existing "Check Service Cloud Feature \(Metadata\)" action
    -   Mark "Look up SOQL Query" action as active by default
-   **Version 2.3.3 - March 2025**

    Fixed a security bug and implemented additional validation checks to improve security.

-   **Version 2.3.2 - December 2024**

    Added a new action to conform with different Salesforce Portal's config settings.

-   **Version 2.3.1 - November 2024**

    Fixed: Look up Permission Set License for Users Stream.Added: Remove Permission Set License from Users.

-   **Version 2.3.0 - August 2024**
    -   New actions:
        -   Look up users license stream
        -   Look up users based entitlement stream
    -   Modified existing actions: Look up users
-   **Version 2.2.1 - October 2023**

    Fixed: 'licensable' field set to be true in plugin.xml.

-   **Version 2.2.0 - September 2023**
    -   Fixed:
        -   'Get Related Records' Flow Action, the maximum field length on the 'Relationship' field is 40 characters limiting Relationships from Salesforce
        -   Unable to update Order record in Salesforce
        -   Changing all the metadata actions from active true to false and changing name to the standard name
-   **Version 2.1.4 - August 2022**

    Fixed: Patch version of Salesforce Spoke. This version includes a fix to fetch permission set licenses.

-   **Version 2.1.3 - February 2022**

    Changed: Patch release of Salesforce Spoke for IntegrationHub. This version includes a KMF fix and changes to Action names and descriptions.

-   **Version 2.1.1 - December 2021**

    New: Added the Look up Document for Record action.

-   **Version 1.0.0 - October 2020**
    -   Access and manage data in the Account, Contact, Case, Lead, Opportunity, Order, User, and almost any other objects of your Salesforce instance from the ServiceNow instance.
    -   This spoke was built for the Salesforce API version v48.0, but may be compatible with earlier and later versions.

