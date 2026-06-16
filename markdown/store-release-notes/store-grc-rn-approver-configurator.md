---
title: GRC: Approver Configurator release notes
description: Version history for the GRC: Approver Configurator application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-approver-configurator.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Approver Configurator release notes

Version history for the GRC: Approver Configurator application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**

    This release adds platform-managed row-level query security to all BCM approval configuration tables, including approval records, rules, configurations, assignments, and levels, ensuring that only authorized users can access specific rows based on parent-table and column-level restrictions. This enhancement improves security by aligning with the platform's standard query-time access enforcement and boosts performance by applying filtering at the database layer for list views, REST queries, related lists, and reports. The upgrade process automatically installs these restrictions while preserving any customer customizations; customers with integrations or scheduled jobs must verify that their integration accounts have appropriate read permissions to avoid reduced query results for unauthorized users.

-   **Version 22.0.0 - March 2026**

    Fixed: Fixed an issue where users could not submit a risk assessment project due to an ACL issue.

-   **Version 21.1.1 - December 2025 \(Zurich\)**

    Fixed: Fixed a security vulnerability bug, found in code scan.

-   **Version 21.0.1 - August 2025**

    New: Support to select multiple groups on an "Approval rule" record in GRC Approver Configurator

-   **Version 20.0.1 - February 2025**

    Fixed: Approvals were not getting generated for Plans \(sn\_bcp\_plan\) within the BCM Workspace.

-   **Version 19.0.1 - August 2024**

    Fixed: sn\_grc\_appr.approver role won't be accounted for in IRM or any licensing. With this fix, users assigned this role will not be charged for IRM licenses.

-   **Version 18.1.0 - June 2024**

    New: The app is made non-licensable.

-   **Version 18.0.0 - February 2024**

    New: Added dynamic approval for policy, policy exception, and policy redlining.

-   **Version 3.0.1 - August 2023**

    Fixed: The "Approvers from" field on the GRC Approval Rule \[sn\_grc\_appr\_approval\_rule\] record is getting cleared out when the "Approver type" is not "Approver from source".

-   **Version 2.2.0 - May 2023**

    New: Added a new security role to secure scripting fields in approval configurator.

-   **Version 2.0.1 - February 2023**
    -   New: Make the approver configurator a standalone app so customers can install
    -   Changed: App packaging to new parent pom to remove duplicated content
    -   Fixed:
        -   Security issue for glide scope evaluator
        -   License role entry for approver configurator app in role table
-   **Version 1.0.1 - November 2021**

    GRC: Approver Configurator enables administrators to set up multiple levels of approvals and pick approvers based on business rules


