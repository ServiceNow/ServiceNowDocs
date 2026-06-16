---
title: GRC: Metrics release notes
description: Version history for the GRC: Metrics application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-metrics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Metrics release notes

Version history for the GRC: Metrics application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Edit CMD formula after execution: Formulas in calculated metric definitions can now be edited after they have been executed. Each edit creates a new formula version with effective dating, enabling full version history and traceability of formula changes over time.
        -   Formula version management: A new formula version table tracks all iterations of a formula, including version numbering, date validations, and M2M record associations. The formula builder UI has been updated to support editing and versioning workflows.
        -   Formula calculation and forecast on versioned formulas: Formula calculations and forecasts now operate against the appropriate formula version, ensuring results align with the correct version of the formula for any given time period.
    -   Changed:
        -   Info message and version date labels updated: Improved clarity of informational messages and version date labels within metric formula workflows.
        -   Calculated metric definition metric updates on entity type changes: When an entity type is added to or removed from an underlying manual metric definition, the associated calculated metric definition metrics are now automatically updated to stay in sync.
        -   This release includes security enhancements that strengthen access controls across the application.
        -   User picker compatibility with field-level security restrictions: User pickers across workspaces have been updated to function correctly with newly introduced restrictions on user profile fields \(email, phone, mobile, home phone\).
        -   Formula migration for seed and demo data: The CMD formula migration process now correctly reads and migrates values to the formula version table for both seed data and demo data environments.
    -   Fixed:
        -   Approval Required field not working on KCI metric definition records: The Approval Required field now functions correctly on KCI metric definition records.
        -   Threshold rating field data model not updating after upgrade: Resolved an issue where the threshold rating field data model was not changing correctly after a platform version upgrade.
        -   Supporting data values not loading: Fixed an issue where GRC Metrics supporting data values were not loading as expected.
        -   Recalculate on CMD not working: The Recalculate action on calculated metric definitions now works as expected.
        -   Metric data not available in database views: Metric data is now correctly surfaced in database views.
        -   Metric activation/deactivation on entity changes: Resolved an issue where metric definition metrics could not be properly activated or deactivated when entities were added or removed from a calculated metric definition.
        -   Threshold condition cache issue: Fixed a caching issue that caused threshold conditions to evaluate incorrectly.
        -   Upgrade and customization compatibility issues: Addressed various issues discovered during upgrade and customization testing.
-   **Version 22.0.1 - March 2026**
    -   Configure thresholds with multiple levels and ranges for granular monitoring.
    -   Duplicate and modify existing thresholds to streamline creation.
    -   Automated actions are immediately triggered when thresholds are breached.
-   **Version 21.1.3 - December 2025 \(Zurich\)**
    -   New:
        -   Rename metric definition names after creation.
        -   Configure Calculated Metric Definition \(CMD\) formula behavior for null or undefined operands based on the operator.
        -   Improved Formula Tree UI, clearly distinguishing between actual and estimated metric data.
        -   Removed unit restrictions for selecting emission factors and metric definitions in CMD.
        -   Enhanced entity-based access control for metric definitions, metrics, data tasks, and metric data.
        -   ESG Management roles now inherit compliance feature roles.
    -   Fixed:
        -   Resolved metric data generation failures that occurred when a definition contained over 5,000 metrics.
        -   Fixed threshold calculation errors that occurred when the previous period value was 0.
        -   CMD metrics now automatically activate or deactivate based on the entity's active status.
-   **Version 21.0.2 - September 2025**

    Fixed: Minor issues related to metrics.

-   **Version 21.0.1 - August 2025**
    -   Enable organizations to provide estimated data using pre-defined methods like average when actual data is not available and replace it with actuals, when available
    -   Enhance data accuracy and governance by adding a review process for automated metric definitions.
-   **Version 20.2.1 - July 2025**

    Fixed: Security fixes.

-   **Version 20.2.0 - June 2025**

    Fixed: Security fixes.

-   **Version 20.1.1 - May 2025**
    -   New: Enhanced user access using entity-based access.
    -   Changed: Enable table audits for metric tables.
    -   Fixed:
        -   Important security fixes.
        -   Minor bug fixes and improvements.
-   **Version 20.0.2 - February 2025**
    -   New:
        -   Review the calculated metric definition data using a formula tree to access detailed information on the operands, metric definitions, metrics, and emission factors.
        -   Import your historical metric data using an import template to update and manage metric data within your organization.
    -   Changed:
        -   Metric data tasks support choice and HTML response formats and table improvements.
        -   Assign data owners dynamically for metrics that are based on configurations.
        -   Enable users to control the scheduling of metric data tasks.
    -   Fixed:
        -   Important security fixes.
        -   Minor bug fixes and improvements.
-   **Version 19.1.5 - December 2024**

    Improved the logic for retrieving emission factors, which applies to the evaluation of the Calculated Metric Definition formula.

-   **Version 19.1.3 - November 2024**
    -   Fixed:
        -   Important security fixes.
        -   Minor bug fixes and improvements.
-   **Version 19.0.5 - August 2024**
    -   New:
        -   Create fiscal calendars to collect metrics from different geographical locations:
            -   Create ad-hoc metric data tasks
                -   Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.
                -   Collect, aggregate, and report data according to your fiscal calendars, which may differ from the Gregorian calendar. Many global organizations have operations in different countries that follow their own fiscal calendars. This feature enables entities in other locations to collect data according to their own fiscal calendars.
            -   Support for multi-level approval of metrics using GRC: Approver Configurator.
    -   Support for improved filters on the metric data table to filter your tasks. The filters help to show only the relevant and open tasks for data owners and approvers.
    -   Improved the following metric related tables: Metric definition, Metric, Metric data, Metric data task, Metric data task url read ACLs to support:
        -   Metric level Approver user or Approver group: This means that the specified user or group designated as the approver can access only the particular metric and the tables specified for which they are the approver.
        -   Multi-level approval: This means that the specified user or group designated as the approver can access only those records in the metric-related tables for which they are the approver.
        -   Enable enterprise owners to access metric records: This means that an enterprise owner can access any metric related record.
-   **Version 18.1.1 - June 2024**

    Changed: Updated the UX add-on event mappings of declarative actions with Form controller.

-   **Version 18.0.2 - February 2024**
    -   New: The sn\_grc\_metric\_md\_import table is added to the GRC: Metrics application.
    -   Changed:
        -   Attributes modified in the sn\_grc\_metric\_base\_definition table
            -   The mandatory attribute has been removed from the Description column in the sn\_grc\_metric\_base\_definition table.
            -   The formula\_internal column has been made read-only.
        -   In the sn\_grc\_metric\_composite\_definition table, the formula\_internal field has been set to read-only
    -   Removed:
        -   The metric\_status field has been removed from the sn\_grc\_metric\_base\_definition table.
        -   The metric\_status field has been removed from the sn\_grc\_metric\_metric table.
        -   The rollup\_formula field has been removed from the sn\_grc\_metric\_composite\_definition table.
-   **Version 17.0.1 - August 2023**
    -   New:
        -   Set up percentage-based thresholds for metric data.
        -   Use the new role sn\_grc\_metric.developer to edit the script in automated metric definition.
    -   Changed:
        -   Utilize the simpler layout of the metric definition forms for easier viewing of information on the form.
        -   Workspace record page template upgrade.
        -   Updated the reference qualifier from sn\_grc\_metric.manager role on the Metric definition 'Approver' field to sn\_grc\_metric.reader role.
        -   Maintaining threshold rating at metric data.
    -   Fixed: The following two fields have been deprecated from the sn\_grc\_metric\_base\_definition, sn\_grc\_metric\_metric tables.
    -   Removed:
        -   latest\_data
        -   previous\_data
-   **Version 16.1.2 - May 2023**
    -   New:
        -   'Metric data by entity' feature is introduced to help report metric data across entity hierarchy.
        -   'Time dimension' table is introduced to support dynamic rollup across different time dimensions and entity hierarchy.
    -   Changed:
        -   Ability to switch collection method of metric definitions from manual to automatic and vice versa.
        -   Calculated metric definition logic is modified to process changes/historical data collected in child metric data.
    -   Fixed: Cascade delete on 'Latest data' and 'Previous data' columns of Metric and Metric definition tables are removed.
    -   Removed: The sn\_grc\_metric\_composite\_data table is deprecated. The calculated metric definition data is now stored in sn\_grc\_metric\_collector\_data table.
-   **Version 16.0.5 - February 2023**
    -   New:
        -   Ability to upload historical data for metrics to maintain a record of your complete data
        -   Ability to set the due date on metric data tasks using theDue date offsetfield in the manual metric definition form. This feature enables you to set the due date for metric data tasks.
        -   New reader role \(sn\_grc\_metric.reader\) added to grant read only access to metric tables
    -   Changed: sn\_grc\_metric.user now inherits the reader role and will grant create and edit access on metric tables
-   **Version 15.1.4 - December 2022**

    Fixed: Metric data table dependency version updated to 15.1.0

-   **Version 15.1.3 - November 2022**

    New:

    -   Aggregates the entity-level data on the calculated metric definitions.
    -   Enabled multi-select data tasks to approve metric data tasks.
    -   The data owner metric task entry page supports inline editing of qualitative and quantitative metrics.
    -   The data task page in the data owner view displays the trend of the last 3 periods and allows addition of URL links.
-   **Version 15.0.4 - August 2022**
    -   New:
        -   Added scenario analysis for important business services
        -   Added feature to analyze impact tolerance and important for business services
        -   Added new and improved relationships in the Business Service form
        -   Added self-attestation for operational resilience status
-   **Version 14.2.4 - May 2022**
    -   New:
        -   Added import tool for bulk data upload
        -   Added integration mapping tables to support bulk data upload and configuration
        -   Added external source for the automated metric definition
    -   Fixed:
        -   In manual metric definition, approvers are now added to the allowed users or allowed groups by selecting the confidentiality flag.
        -   Confidential feature for ESG reporting and disclosure manager
-   **Version 14.1.1 - March 2022**
    -   New:
        -   Overview page for Metric Definition and Metrics
        -   Support for the scripted metric definition
        -   Groups, sub-groups, and labels for Metrics
        -   Level 1 \(Amber Level\) and Level 2 \(Red Level\) metric thresholds on the metric definition
        -   Target values for each period in Metrics
        -   Domain area field to differentiate metrics
        -   Metric class to identify KRI, KCI, and KPIs
    -   Changed:
        -   Enabled the override functionality in the Metric data task
        -   Added the start date along with the interval end date in Metric definition data/metric data
        -   Add tags on Metrics to support disclosures
-   **Version 13.2.3 - December 2021**
    -   New:
        -   Added support for localization and internationalization.
        -   Added report for qualitative metrics on disclosures.
    -   Fixed: Fixed redirect for programs/projects to correct the UI page.
-   **Version 13.0.2 - November 2021**

    GRC: Metrics helps you define metrics that will enable other applications to assess, compare, track, and report performance.


