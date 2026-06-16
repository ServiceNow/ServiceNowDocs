---
title: Planned Maintenance Management release notes
description: Version history for the Planned Maintenance Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-planned-maintenance-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Planned Maintenance Management release notes

Version history for the Planned Maintenance Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.14.0 - June 2026**
    -   New:
        -   Administrators can manage Planned Maintenance access using updated, non-Glide query ACLs \(access control lists\).
        -   The system supports new query-based access controls for Planned Maintenance, enabling more precise control over user permissions and roles during upgrades and new installations.
    -   Changed:
        -   Role assignments in Planned Maintenance have been updated to resolve invalid or missing roles in access controls.
        -   ACLs have been reviewed and remediated to ensure all required roles are defined and dependencies are correctly declared, improving access reliability and plugin installation consistency.
-   **Version 2.12.0 - March 2026**

    Fixed: Improved PMM performance by ensuring even load distribution for batch cleanup events.

-   **Version 2.11.1 - February 2026**

    Changed: Access Control Update: System properties that were accessible only by admin and maintusers, due to having empty read or write roles, have been updated to include the plan\_maint\_adminrole. Now, users with the plan\_maint\_adminrole can access and manage these properties without needing full admin rights.

-   **Version 2.11.0 - December 2025**
    -   We’ve made Planned Maintenance easier to manage, more secure, and more role-driven.
    -   New: Introduced the plan\_maint\_adminrole for all Planned Maintenance modules and application menus.
    -   Improved:
        -   Access to Planned Maintenance features is now role-based rather than restricted to system admins, enabling broader operational usage while maintaining security.
        -   Dictionary configurations are updated to ensure that the fields are appropriately set as read-only where required, resulting in a more consistent and predictable user interface experience.
    -   Fixed:
        -   Reviewed the client-side logic for key Planned Maintenance tables and fields.
        -   Fixed inconsistencies where certain fields appeared editable in the user interface even though they should have been protected.
-   **Version 2.9.0 - August 2025**
    -   New: Added a new "Migrate Plans" action to conveniently migrate Planned Maintenance plans to Planned Work Management, allowing users to multi-select and migrate plans in bulk. After migration, the Planned Maintenance Management \(PMM\) plan will be deactivated, and the corresponding Schedule Occurrence will be created in Planned Work Management \(PWM\).
    -   Changed: Additionally, assets that no longer meet the conditions of a Maintenance Plan will now be automatically removed from the Maintenance Plan Records. This improves data accuracy and eliminates the need for manual updates.
-   **Version 2.7.0 - February 2025**
    -   New:
        -   Allow customers to migrate maintenance plans to work plan. Migration can be done at plan level.
        -   Bulk migration is not in scope for this version.
    -   Fixed: Generate work orders using run on demand option for condition and script based schedules.
-   **Version 2.4.3 - October 2024**

    Fixed: Generate work orders using run on demand option for condition and script based schedules.

-   **Version 2.4.0 - August 2024**
    -   New: Code changes to support work configurations
    -   Fixed: Issues with run on demand action
-   **Version 2.1.0 - February 2024**

    Fixed: Issues related to running on demand feature.

-   **Version 1.2.3 - December 2023**
    -   Fixed:
        -   Resolved the issue with Run on-demand when a date was selected.
        -   Modifications made to the nightly job to support the generation of future-dated work orders in the planned work management application.
-   **Version 1.2.2 - September 2023**
    -   Fixed:
        -   Performance issues while generating work orders
        -   Generate work order using Run on Demand action
-   **Version 1.2.1 - August 2023**

    Introduced a new role for accessing planned work management entities.

-   **Version 1.0.7 - April 2023**
    -   Fixed:
        -   Honor product model value to filter work plan records.
        -   Create correct number of schedule occurrences for based on configured value.
-   **Version 1.0.5 - March 2023**
    -   Fixed:
        -   Optimal creation of business rules on plans to address performance issues.
        -   Allow schedules to be created for table names more than 40 characters long.
        -   Restrict changes to the next run value before work order creation when source values are changed.
-   **Version 1.0.4 - February 2023**

    The plugin was available as a family plugin until the Tokyo release and as a store app from the Utah release.


