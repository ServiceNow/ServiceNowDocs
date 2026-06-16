---
title: Jira Service Management spoke release notes
description: Version history for the Jira Service Management spoke integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-jira-service-mgmt.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Jira Service Management spoke release notes

Version history for the Jira Service Management spoke integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - May 2026**
    -   New:
        -   Actions: Report Personal Data. You are now required by Atlassian to report user personal data usage if you store such details using existing actions of the spoke in your apps. Refer to User privacy guide by Atlassian for more details
        -   Authentication Template for Jira Service Management Cloud. A new authentication template has been introduced for Jira Service Management Cloud customers using 3-Legged OAuth \(3LO\). Refer to the product documentation for more details on how to set up
    -   Changed: Based on guidance for Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps by Atlassian, the way to set up and authenticate the Jira Service Management connection has been changed for Jira Service Management Cloud customers.
    -   Removed: Authentication Template for Jira Service Management Cloud. The previous authentication template for Jira Service Management Cloud has been retired. Refer to the product documentation for more details on how to set up.
-   **Version 1.1.1 - December 2024**

    Fixed: Multi-line field support.

-   **Version 4.4.0 - May 2024**
    -   Due to changes in third-party APIs, we made the following changes:
        -   New: New actions equivalent to the ones that were deprecated
            -   Create Issue \(create\_issue\_4\)
            -   Get Projects \(Metadata\) \(Deprecated\) \(get\_projects\_v3\)
            -   Get Projects \(Metadata\) \(get\_projects\_v4\)
            -   Get Issue Types \(Metadata\) \(get\_issue\_type\_v3\)
            -   Get Creatable Fields \(Metadata\) \(get\_creatable\_fields\_v2\)
        -   Removed: Deprecated actions
            -   Create Issue \(create\_issue\_3\)
            -   Get Projects \(Metadata\) \(get\_projects\_2\)
            -   Get Issue Types \(Metadata\) \(get\_issue\_type\_2\)
            -   Get Creatable Fields \(Metadata\) \(get\_creatable\_fields\)
    -   Fixed: Update Issue action to manage issueLink field correctly
    -   Reference:
        -   Jira APIs \(https://developer.atlassian.com/changelog/\#CHANGE-1304\) have changed.
        -   Jira APIs are moving away to use Project IDs \(in lieu of Project Names\) and Issue Type IDs \(in lieu of Issue Type Names\).
-   **Version 1.1.0 - March 2023**
    -   New: Authentication template for easier spoke setup.
    -   Fixed:
        -   Error while uninstalling the spoke.
        -   Create Customer Request action.
-   **Version 1.0.3 - September 2022**
    -   Fixed:
        -   Improve installation performance of spoke
        -   Look up User Account ID action
-   **Version 1.0.1 - December 2021**

    Changed: Patch release of Jira Service Management Spoke for IntegrationHub. This version updates the Create Customer Request action with "Request Participants" field as non-mandatory.


