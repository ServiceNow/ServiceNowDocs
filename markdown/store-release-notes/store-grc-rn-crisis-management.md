---
title: GRC: Crisis Management release notes
description: Version history for the GRC: Crisis Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-crisis-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Crisis Management release notes

Version history for the GRC: Crisis Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.2 - June 2026 \(Australia\)**
    -   New:
        -   Import and export of event tasks is now supported. Users can import event tasks from Excel files.
        -   Users can now quickly add recovery tasks from plan and recovery strategy pages. A new quick insert action is available on the Recovery tasks related list, allowing users to create recovery tasks directly from both plan and recovery strategy records.
        -   A dedicated Recovery tasks form screen is now available.
    -   Fixed:
        -   PDF generation no longer blocks event state changes. PDF creation has been moved to an asynchronous process, allowing state changes to proceed without delay
        -   Task creation performance has been improved by moving dependency checks to event processing.
        -   The calculation of task timing and order has been updated for better performance.
-   **Version 9.1.5 - March 2026 \(Zurich\)**

    Security fix in MRA record addition: Post this fix, the user will be able create new rows in the related list table.

-   **Version 9.1.4 - December 2025 \(Zurich\)**
    -   New:
        -   Cross plan task dependency
            -   Recovery tasks inside Business Continuity Plan \(BCP\) can now be linked to tasks from other plans, provided they belong to a direct upstream plan. These will be carried across to event tasks.
            -   A new “Associated Plans” tab has been introduced to easily view and manage these cross-plan connections
        -   Phases
            -   Introduced phases to categorize tasks across different stages of a recovery event, such as Preparation, Recovery, Validation, and Return to Normal, for clearer progress visibility
            -   Shipped some out of box phases: Preparation, Recovery, Recovery Validation, Return to Normal, Return to Normal Validation, Post-incident review
        -   Asset recovery level
            -   A new option which allows users to mark impacted assets as Partially Recovered or Recovered upon task completion
        -   Include in Actual Crisis or Exercise
            -   Users can now specify whether a task should be included in an actual crisis or exercise scenario
        -   Exclude from Time Calculation
            -   A new option lets users mark tasks that should not be factored into overall time calculations
        -   Automated Planned Time Calculation
            -   Event tasks now include Planned Start and Planned End fields that are automatically calculated based on the recovery event’s expected start time, as well as the duration and dependencies of predecessor tasks
        -   Gantt view
            -   The hierarchy view now features an integrated Gantt chart, providing a visual timeline of task durations and dependencies. Tasks are color-coded to indicate their status, such as Completed, In Progress, and more
    -   Changed:
        -   Plan Retrieval for Recovery Events
            -   Updated how plans are brought into a recovery event. Previously, all plans related to the target plan were automatically included. With the introduction of a clearer upstream/downstream hierarchy, recovery events will now exclude upstream plans
        -   Recovery assets
            -   Recovery assets are now linked to their corresponding BIA records, enabling automatic retrieval of key data such as RTO, RPO, and Recovery Tier
    -   Fixed:
        -   Action Items updates
            -   Action items are now deleted when the associated event is deleted. Any SAE linked to those action items will be automatically canceled
            -   Updated validation logic for action items
            -   Users can now view SAE assessments even if they are not linked to an action item
        -   Archived plans updates
            -   Archived plans will no longer appear in the selection modal when adding related plans
            -   Within an exercise or event, archived plans will no longer be available in the selection modal, preventing users from adding them directly
            -   When using “Add all plans related to asset”, primary archived plans will not be pulled in. However, related archived plans will still be included, since they may be dependencies of active plans required for the event to run successfully. If customers do not want these archived downstream plans included, they will need to adjust the relationship
        -   Fixed issue where Activated Plans would get permanently stuck in Open status if recovery event was of type 'Actual'
-   **Version 9.0.4 - August 2025**
    -   New:
        -   Avoid duplicate event tasks by grouping similar event tasks
        -   Manage action items for ad-hoc tasks and threat assessments
-   **Version 8.1.2 - June 2025**

    Fixed: PDF generation is not working correctly when Hungarian characters are used.

-   **Version 8.1.1 - May 2025**
    -   New: Progress bar added for update dependencies in events
    -   Fixed:
    -   -   Dependencies are missing from the list for the recovery task
-   Element definition filter is not working in planning and event
-   **Version 8.0.3 - February 2025**
    -   New:
        -   Added wbs order for event tasks
        -   Added related assets from related plans
        -   When a plan is added to event, customer should be able to see all the activated plans associated to the tasks for n levels.
        -   Added gantt UI for hierarchical view for event tasks
    -   Fixed: Fixed security gap for html messages
-   **Version 7.1.1 - November 2024**

    Changed: Review sandbox access for client callable scripts.

-   **Version 7.0.1 - August 2024**
    -   Changed:
        -   Added and updated roll-up of total time taken and total effort for completing the tasks from tasks to plans to assets
        -   Added "Open" state for activated plan, when event is started plan is moved to "Open" state instead of "Work in progress" state
        -   The crisis manager can now add plans to an event without any associated assets and start executing the tasks.
        -   Based on asset tags in recovery tasks, impacted assets are added to event tasks.
    -   Fixed: Added event tasks related list in U16 view
-   **Version 6.1.4 - July 2024**

    Fixed: Fixed app compatibility for the glide family releases.

-   **Version 6.1.3 - June 2024**
    -   New:
        -   Added event tasks automation framework
        -   Added new states for event tasks to support failure mode
        -   Added re-trigger for manual or automatic event tasks
        -   Added bulk edit support for event tasks
        -   Added email notification for event task automation flow
    -   Changed: Make event tasks editable for closed-state.
    -   Fixed: Security defect for GlideRecord encoded query.
-   **Version 6.0.1 - February 2024**
    -   New:
        -   Added configuration to set manual or automated updates from CMDB, BIA and BCP
        -   Added dependency update support from CMDB, BIA, and BCP
        -   Added email notification for updates from CMDB, BIA, and BCP
    -   Fixed:
        -   Fixed save UI action appearing on event tasks
        -   Added warning message for event tasks when plan don't have scope
        -   Fixed security gap on exercise flows
-   **Version 5.0.2 - August 2023**
    -   New:
        -   Added exercise and crisis events in the new BCM Next Experience workspace
        -   Added exercise and events activities in My Task
        -   Added new homepage tabs for crisis events and exercise
        -   Added a new overview page with a stepper component for states
        -   Added exercise and crisis events modules in the List view
        -   Added new UI experience for the Assets tab
        -   Added new UI experience Event Tasks
        -   Added 360 degree visualization
    -   Fixed: Unable to close activated plan for table top exercise.
-   **Version 4.1.0 - May 2023**

    Fixed: Look up for reference field is displaying only 10 values at a time in workspace list.

-   **Version 4.0.1 - February 2023**

    Fixed: Fixed report\_view ACLs.

-   **Version 3.0.3 - December 2022**

    Fixed: Fixed parent POM in order to remove the redundant GLIDE-INF folder and content contained within.

-   **Version 3.0.2 - August 2022**
    -   Changed: Updated event tasks to support BCM event scoping changes
    -   Fixed: Fixed security gaps for HTML injections
-   **Version 2.3.1 - March 2022**
    -   New: Ability to define complex approval rules and route exercises for approval
    -   Changed: State, actual date roll-ups, and its associated effort rollup to the event are modified.
-   **Version 2.2.1 - November 2021**
    -   New:
        -   Ability to generate exercise and events PDF
        -   Report actual time taken and total effort at plan and event asset based on task execution duration
        -   Event task execution to honor dependency defined in plan
        -   Ability to add ad hoc task to activated plan
    -   Changed:
        -   Former behavior of adding activated plan and tasks per event asset is modified to avoid task duplication. Activated plan and ad hoc plan are unique per event
        -   Event tasks contain a list of impacted assets for which the tasks will be executed
    -   Removed: Impacted asset and plan asset columns on activated plans are deprecated
-   **Version 2.1.1 - June 2021**
    -   New: Self-service view added for event tasks
    -   Changed: Workspace layout of event activated plan and event task modified
    -   Removed: Mandatory check of plan in activated plan
-   **Version 2.0.1 - March 2021**
    -   New:
        -   Support to add any asset/process/service to recover during crisis
        -   Track adhoc tasks to recover an asset
    -   Changed: Activated plan and event tasks now reference impacted assets. A plan instance is used to track activities for an impacted asset/process/service

