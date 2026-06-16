---
title: Planned Work Management release notes
description: Version history for the Planned Work Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-planned-work-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Planned Work Management release notes

Version history for the Planned Work Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.14.0 - June 2026**
    -   New:
        -   Administrators can manage Planned Work Management access using updated, non-Glide query ACLs \(access control lists\).
        -   The system supports query-based access controls for Planned Work Management, enabling more precise control over user permissions and roles during upgrades and new installations.
        -   Changed:
            -   Role assignments in Planned Work Management have been updated to resolve invalid or missing roles in access controls.
            -   ACLs have been reviewed and remediated to ensure all required roles are defined and dependencies are correctly declared, improving access reliability and plugin installation consistency
        -   Fixed:
            -   The planning calendar’s contextual side panel responds without latency.
            -   Calendar events are displayed correctly in the planning calendar when filtered by Work Order.
            -   Planned Work Schedules configured for multiple days of the week generate occurrences correctly after the upgrade.
-   **Version 2.12.3 - April 2026**
    -   Fixed:
        -   Added work notes logging for key user‑initiated actions to improve operational transparency.
        -   Improved Schedule Occurrence generation to ensure subsequent occurrences are created correctly when conditions are applied to a Planned Work Schedule Template.
-   **Version 2.12.0 - March 2026**

    New: Work Order Grouping: Simplified execution by enabling work orders to be grouped using configurable criteria \(such as location or asset attributes\), reducing the number of records technicians need to navigate.

-   **Version 2.11.0 - December 2025**
    -   New:
        -   Extension Point for effective start datesAdded a new option “Calculated” to Start planned schedule field based on enabling the use of the PWMScheduleStartExtensionPoint. This allows the users to add custom logic to compute effective start dates. Access to the plan, schedule, and source records is provided for easy calculation and return of values.
        -   Even load distribution for work order generation - The Generate Work Orders program is now part of the generate\_order\_queue, enabling smoother processing and more evenly distributed workload generation
        -   Task Plan Template support in Planned Work Management plansPlanned Work Management plans can now leverage Task Plan Templates to automatically create related tasks \(such as cases or incidents\). This provides greater flexibility and consistency when defining work plans.
    -   Changed: Refined access control with granular roles for Planned Work Management modulesAccess now requires only the PWM Admin role, improving security and role clarity. The generic admin role is no longer required.
    -   Fixed:
        -   Accurate removal of assets that no longer match plan conditionsThe Update planned work records on demand job now ensures assets that no longer meet planned conditions are removed—aligning with the behavior of “Associate plan with filtered records” and “Associate schedule with filtered records.”
        -   Corrected meter trigger behaviorNo schedule occurrences are created at schedule creation time.Schedule occurrences now correctly store the meter reading at the moment they were generated, rather than inheriting values from the planned work records.
-   **Version 2.9.2 - November 2025**
    -   Fixed:
        -   Resolved forecasting logic issues in Planned Work Management \(PWM\) schedules.
        -   Forecast Range Validation: Work orders are now created only if the schedule occurrence date falls within the configured “Days in Future to Create Work Orders” window, ensuring that neither the “Generate Work Orders” UI action nor the nightly job creates work orders outside this range.
        -   Initial Occurrence Handling: Updated logic to always create the first schedule occurrence \(SO\), even if its work order falls outside the forecast window. The corresponding work order will still be generated only when it reaches the defined forecast period.
        -   Subsequent Occurrences: Fixed an issue where the next schedule occurrence was not being created if its date was beyond the forecast range. The system will now continue creating future Schedules Occurrences while still respecting the forecast limit for work order generation.
        -   These changes improve forecasting consistency, ensure that future schedules remain effective, and prevent unintended work order creation for far-future occurrences.
-   **Version 2.9.0 - August 2025**
    -   New:
        -   Schedule Suppression Extension Point Implementation:
            -   A new extension point has been introduced to offer flexible suppression logic when multiple schedule occurrences overlap.
            -   In the current scenario, when two schedule occurrences for the same asset intersect within a time window and have identical work order tasks, one occurrence can be configured to be suppressed.
            -   The extension point allows customers to customize suppression criteria, such as
                -   Comparing checklist items between work order tasks or considering only asset and time window overlaps.
                -   Suppressing maintenance tasks when a break-fix job exists for the same asset
            -   A sample extension script comparing checklist items between work order tasks is provided to help customers tailor suppression logic as needed.
        -   These improvements make PWM more flexible and support diverse operational workflows.
    -   Changed:
        -   Planned Work Management Enhancements
            -   We have made improvements to Planned Work Management \(PWM\) for condition-based and script-based schedules:
                -   Script and condition based schedule changes
                    -   When a schedule is created, Planned Work Records \(PWRs\) will now be created for all assets matching the Maintenance Plan.
                    -   Scheduled Occurrences \(SOs\) will be created only for the assets that match the schedule's condition at that time.
                    -   When Work Orders \(WOs\) are created, new SOs will not be automatically generated for condition-based schedules.
                    -   When a new asset matches the script or condition, a new SO will be created automatically, and WOs will be generated when the schedule runs.
                    -   When an asset no longer matches the script or condition, its associated WO will be canceled and its SO will be deleted.
                    -   Refresh actions will correctly handle SOs without impacting active WOs that cannot be canceled.
                    -   For script and condition based schedules, the "Associate Schedule with Filtered Records" UI action is no longer shown, and "Associate Plan with Filtered Records" will not affect script and condition based schedules.
    -   Removed: The "Apply to New Matching Records" field on Maintenance Plans has been hidden and now defaults to true to ensure proper schedule refresh behavior.
-   **Version 2.7.0 - February 2025**
    -   New:
        -   Allow customers to migrate maintenance plans to work plan. Migration can be done at plan level.
        -   Bulk migration is not in scope for this version.
    -   Fixed: Maintenance due date calculation for monthly and annual trigger types
-   **Version 2.4.3 - October 2024**
    -   Fixed:
        -   Filter on FSM Planning Calendar
        -   Issues around Plan Effectivity
        -   Fixed Schedule Occurrence generation
        -   Install base plan PWRs
        -   Meter based schedules
-   **Version 2.4.0 - August 2024**
    -   New: Changes to support work configuration
    -   Fixed:
        -   Creation of additional schedule occurrences by scheduled job
        -   Additional schedule occurrence created for current date/time when a schedule created with trigger type 'Multiple days of the week'
        -   One less schedule occurrence is created for schedule with end type as 'Frequency'
        -   Schedule occurrences are not generated for forecasting enabled plans through nightly job / UI action
        -   Schedule occurrences are skipped when clicked on associate schedule occurrence with filtered records for weekly trigger type with repeat every as 1, lead time as 1
        -   When work order is cancelled last completion date on planned work record is not filled
        -   Unable to generate work orders using 'execute now' or 'run on demand'
        -   Update of 'Days in future to create work orders' is not updating the schedule occurrences until effective start is changed
-   **Version 2.1.0 - February 2024**
    -   New:
        -   Filter component within maintenance calendar
        -   Support creation of schedule occurrences considering past dates
        -   Support last and first day of the month as request due and earliest start respectively
    -   Fixed:
        -   Generate future work orders when forecasting is enabled
        -   Sync schedule changes with schedule occurrences
-   **Version 1.3.2 - December 2023**
    -   Fixed:
        -   Generate future work orders when the forecast is enabled.
        -   Performance fixes.
-   **Version 1.3.1 - September 2023**
    -   Fixed:
        -   Suppress schedule occurrences
        -   Search in calendar
        -   Right click actions
        -   Populating CI on planned work records
        -   Populating right table for Install base plans
-   **Version 1.3.0 - August 2023**
    -   New
        -   Calendar to view schedule occurrences and work orders
        -   Partially or fully suppress schedule occurrences falling within an overlapping time period, based on similar work order tasks
        -   Classify plans as OEM or AEM
-   **Version 1.2.3 - April 2023**
    -   Fixed:
        -   Honor product model value to filter work plan records.
        -   Create correct number of schedule occurrences for based on configured value.
        -   Update install base information on Work orders.
        -   Retain the correct install base table on work plan.
        -   Proper creation of dependent schedules.
-   **Version 1.2.2 - March 2023**
    -   Fixed:
        -   Skip creating duplicate schedule occurrences for fixed end-date schedules using the Run on-demand option.
        -   Update the Install base field for Install Base type plans.
        -   Update correct Next run time during preserve calculated interval is false.
        -   Update work notes.
        -   Create plan work records for future effective date plans.
-   **Version 1.2.1 - February 2023**
    -   New:
        -   Workspace for maintenance administrators to define and manage plans and schedules
        -   Dashboard for administrators to track key metrics
        -   Introduction of schedule occurrences to track maintenance cycles
        -   Track work orders linked to each maintenance cycle
        -   Allow users to update work notes against plans and schedules
        -   Support creation of maintenance plans for Install base product models
-   **Version 1.1.0 - November 2022**
    -   New:
        -   Script include fetch historical data for planned work entities
        -   Allow other scoped applications to access planned work entities
        -   Preserve calculated interval for annual and monthly triggers
-   **Version 1.0.0 - August 2022**
    -   The Planned Work Management application helps manage the planned work activities like maintenance, inspections, audits, etc., with recurring schedules at regular intervals. Planned Work Management is built on top of the Planned Maintenance application and provides the following changes:
        -   Create flexible schedules and templates for planned work orders.
        -   Create maintenance plans that support multiple assets at a single location.
        -   Adjust future work orders automatically in case of exceptions, such as late completion of work and cancellation.
        -   Enable organisations to forecast planned work orders to better plan their resource coverage and required parts.

**Parent Topic:**[ServiceNow Store - Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)

