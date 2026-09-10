---
title: Business Location release notes
description: Version history for the Business Location application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-business-location.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Customer Service Management version history release notes, ServiceNow Store version history release notes]
---

# Business Location release notes

Version history for the Business Location application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.7.3 - September 2026**
    -   New:
        -   New location-scoped contributor roles: Location Account Contributor and Location Consumer Contributor — Allows to create cases for customers supported by your business organization and allows them to track and manage cases created by them for the customers associated with your organization.
        -   Outage banner on BLSP:A banner on the Business Location Service Portal \(BLSP\) notifies business locations of an active outage affecting them.
        -   Restricted Customer Access now controls visibility:A new Restricted Customer Access field on customer criteria extends existing criteria — such as location-based criteria — to control not only workflow actions \(case\) but also visibility. When enabled, staff can see only the customer and consumer records that meet the configured criteria, rather than all customer records in the instance. This applies to both service personas and sales personas.
        -   Task assignment access for Business Location staff:Business location staff with the Location Project Stakeholder or Location Manager Project Stakeholder role gain read and write access to the Assignment group field, and read access to the Priority field, on business location project tasks. Assigned to write access, which already existed for these roles, is unchanged.
        -   Upgrade migration for existing Location Manager Contributor users:For upgrade customers, a one-time scheduled script removes the Account Contributor and Consumer Contributor roles from users who hold the Location Manager Contributor role. These roles previously granted blanket, instance-wide access to all accounts and consumers, which bypassed location-based access restrictions entirely. After an administrator runs the script, affected users receive the new Location Account Contributor and Location Consumer Contributor roles instead. A revert script is also available, but reverting disables Restricted Customer Access for the instance.
        -   Proactive Customer Service extended to business organizations:Proactive Customer Service and major case management now extend to business \(service\) organizations, alongside the existing support for accounts and consumers. When a network alert affects install base items belonging to a business organization's locations, the system can propose a major case and build a recipient list of the affected business locations. If the major case manager accepts the proposal, they can create a child case for each affected business location, so all affected locations are tracked and updated under a single major case.
-   **Version 5.6.1 - August 2026**
    -   New: The staff at External Organizations \(formerly External Business Locations\) can now view, update, and close customer cases in the classic environment, just like the staff at Internal Organizations \(formerly Internal Business Locations\).
    -   Fixed: Made minor defect fixes and security fixes for this release.
-   **Version 5.5.0 - June 2026**
    -   New:
        -   Introduced Business Organization Self Contributor \(BOSC\) persona, enabling frontline and location-based workers to securely raise and track cases for their assigned sold products and install base items.
        -   Introduced the Organization Hierarchy Contributor persona, enabling service organization staff to view and act on cases, install-base records, and related entities across an organizational branch rather than a single organization.
    -   Fixed: Minor fixes
-   **Version 5.2.0 - April 2026**

    Changed: Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform.Please refer to ServiceNow Documentation for the label changes.Eg: "Service Organization" is renamed to "Organization Core", "Service Organization Criteria" is renamed to "Organization Criteria".

-   **Version 5.0.2 - March 2026**
    -   New: The new granular business organization admin role \(sn\_bus\_loc.business\_org\_admin\) provides CRUD access to all Service Model Foundation tables.
    -   Fixed:
        -   Resolved accessibility issues on the Business Location Service Portal.
        -   Fixed an error that occurred when creating cases from Interactions.
-   **Version 4.2.0 - December 2025**

    Changed: Decoupling of the Business Location Store app from the Case Type Connector plugin, allowing the BL Store app to function independently while keeping the Case Type plugin optional for clients needing the Services Offered feature.

-   **Version 4.1.0 - August 2025**

    New: Introduced the Business functions offered field to capture the type of business function associated to a particular business location.

-   **Version 2.1.0 - May 2025**

    New: Support for Hiding Business Location 360 on workspace based on configuration.

-   **Version 2.0.0 - February 2025**

    Business Location enables support for businesses that interact with customers through physical channels such as stores, branches, franchises, and dealerships. Besides supporting customers, business locations can also support other service organizations.


**Parent Topic:**[ServiceNow Store - Customer Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

