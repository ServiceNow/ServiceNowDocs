---
title: Customer Service Case Types release notes
description: Version history for the Customer Service Case Types application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-customer-service-case-types.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Customer Service Case Types release notes

Version history for the Customer Service Case Types application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.3.1 - May 2026**
    -   Changed:
        -   Enabled granular viewer and admin roles for Case Type features, improving access control and administrative flexibility.
        -   Security enhancements to query access controls for CSM Case Types.
        -   Enabled launching the service selector directly from the Agent Workspace L1 tab to streamline case creation.
-   **Version 4.0.1 - March 2026**
    -   Feature &amp; ContextToday, customers must manually enable the Create Case and New list view Declarative Actions \(DAs\) across multiple entry points to use the Service Selector experience. This feature enables those DAs out of the box for new customers, while still providing an option to turn the experience on or off.
    -   What’s Changed
        -   CTS-based Create Case and New DAs are enabled by default for z-boot customers so the Service Selector is available OOB.
        -   A system property \(sn\_csm\_case\_types.enable\_service\_selector\) is introduced to control whether this experience is enabled.
        -   When enabled, legacy UI actions are hidden to avoid duplicate case-creation entry points.
        -   For upgrade customers, a fix script ensures existing behavior is preserved unless CTS DAs are already active.
    -   Upgrade Impact
        -   No breaking changes.
        -   Existing UI actions remain available for upgrade customers unless CTS is explicitly enabled.
-   **Version 3.0.2 - December 2025**
    -   New:
        -   Case Type Selector UI changes for the new Service Recommendation for interactions feature.
        -   Added Granular admin roles.
    -   Changed:
        -   Internal name from sn\_case\_type is set to "strict\_read\_only"
        -   Case type from sn\_case\_type\_selection is set to "client\_script\_modifiable"
    -   Fixed: Contains minor security defect fixes.
-   **Version 3.0.1 - August 2025**

    The Customer Service Case Types application enables customers to manage complex case processes by defining new case types. A case type represents an individual business process and is a collection of diverse inputs and tasks that an agent performs to resolve customer requests.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

