---
title: GRC: Assignment and Approval Configurations release notes
description: Version history for the GRC: Assignment and Approval Configurations applications on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-assignment-approval-configurations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Assignment and Approval Configurations release notes

Version history for the GRC: Assignment and Approval Configurations applications on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**

    This release adds platform-managed row-level query security to all BCM approval configuration tables, including approval records, rules, configurations, assignments, and levels, ensuring that only authorized users can access specific rows based on parent-table and column-level restrictions. This enhancement improves security by aligning with the platform's standard query-time access enforcement and boosts performance by applying filtering at the database layer for list views, REST queries, related lists, and reports. The upgrade process automatically installs these restrictions while preserving any customer customizations; customers with integrations or scheduled jobs must verify that their integration accounts have appropriate read permissions to avoid reduced query results for unauthorized users.

-   **Version 22.0.0 - March 2026**

    Fixed: Fixed an issue where users could not submit a risk assessment project due to an ACL issue.

-   **Version 21.1.1 - December 2025 \(Zurich\)**

    Fixed: Fixed a security vulnerability bug, found in code scan.

-   **Version 19.1.0 - November 2024**

    GRC: Approver Configurator enables administrators to set up multiple levels of approvals and pick approvers based on business rules.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

