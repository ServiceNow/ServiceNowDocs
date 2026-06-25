---
title: Field Service Management release notes
description: The ServiceNow Field Service Management \(FSM\) application enables your organization to efficiently manage Field Service operations including work order dispatch, scheduling, and mobile workforce enablement. Field Service Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
---

# Field Service Management release notes

The ServiceNow® Field Service Management \(FSM\) application enables your organization to efficiently manage Field Service operations including work order dispatch, scheduling, and mobile workforce enablement. Field Service Management was enhanced and updated in the Australia release.

## Field Service Management highlights for the Australia release

-   Increase productivity by Field Service Managers, who can do their work from anywhere on their mobile device with Field Service Manager Mobile.
-   Allow overbooking in priority cases, consider holidays at the territory level, enable flexible sourcing for work and travel times, and consider task dependencies when scheduling or rescheduling appointments through advanced lead-time management.
-   Determine appointment availability by using territory through APIs, without providing specific contact or location information.
-   View run summaries in Schedule Optimization to understand what was evaluated during scheduling, including objectives, constraints, travel mode, and assignment outcomes.
-   Review the Field Service Management features and activation plugins now available through the ServiceNow Store application. For more details, see the "Changed in the Release" section.

See [Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md) for more information.

## New in the Australia release

-   **[Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/using-dispatcher-workspace.md)**

    [Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/using-dispatcher-workspace.md) now enables you to perform the following tasks:

    -   Show multiple time zones on the map in Dispatcher Workspace with a segmented time indicator to see which time zone each Field Service technician is in. For more information, see [Time zones in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/time-zones-dispatcher.md).
    -   Quickly see a work order task in the task panel and find it on the calendar rather than having to search through multiple days. For more information, see [Open tasks from the task list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/open-task-platform-list.md).
    -   See live traffic on the map in Dispatcher Workspace. For more information, see [Show map overlays in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/map-overlay-dispatcher.md).
    -   Flag multiple tasks at once. For more information, see [Flag or unflag tasks from the list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/flag-task-list-workspace.md).
    -   Quickly find tasks in the calendar from the task list. For more information, see [Flag or unflag tasks from the list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/flag-task-list-workspace.md).
    -   View analytics, including the number of technicians without a work schedule or valid location. For more information, see [Scheduling Health dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/scheduling-health-dashboard.md).
    -   Show an overtime indicator on the calendar to visually see which technicians have overtime tasks. For more information, see [Show overtime indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/dispatcher-wrkspc-settings.md).
    -   Control the size of the cells on the calendar to see shorter tasks more easily. For more information, see [Zoom in or out on the calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/calendar-zoom-dispatcher.md).
    -   Customize the information displayed in work order task popovers in Dispatcher Workspace to show the data most relevant to dispatchers. Popovers on the calendar, map, and task panel now support configurable field display, with a consistent visual experience across all three surfaces. For more information, see [Configure popover fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configure-popover-fields.md).
    -   Stay in the same position in the calendar in Dispatcher Workspace when you change from day to day. For more information, see [Properties installed with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md).
    -   The Assignment group task filter setting is moved from Dispatcher Workspace settings to the main Dispatcher Workspace page and is now a button. For more information, see [Search work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/search-work-order-tasks.md).
    -   Quickly edit tasks in Dispatcher Workspace directly from the contextual side panel. For more information, see [Quickly edit work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/quick-edit-tasks.md).
    -   Add work notes or comments to work order tasks in Dispatcher Workspace from the activity stream. For more information, see [Add work notes or comments with the activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/activity-stream-csp.md).
-   **[Field Service Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/manager-mobile-app.md)**

    Field Service Managers can do their work from anywhere on their mobile device, including the following tasks:

    -   [Manage Field Service technicians from Field Service Manager mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/mange-agents-mobile.md)
    -   [Create a work order task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/create-task-manager-mobile.md)
    -   [Create a personal event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/event-manager-mobile.md)
    -   [View analytics from Field Service Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/view-analytics-manager.md)
-   **[Locations on personal events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/create-personal-event.md)**

    See locations for personal events regardless of where they're created in Field Service Management applications including Dispatcher Workspace and Field Service Manager Mobile.

-   **[Completing work on the ServiceNow Agent mobile application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/Use-mobile-app-fsm.md)**
    -   Generate work summary reports and capture signatures in them at the work order task level along with the existing work order level. Additionally, you can view responses and score information for the smart assessment questionnaires in the work summary report.
    -   Perform asset audits for the technician's personal stockroom to verify and reconcile assets between a physical stockroom and the data on the ServiceNow instance.
-   **[Configuring Smart Assessment from new templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configure-sa-from-new-template.md)**

    Create versions of published smart assessment templates to add or modify questions and instructions. When a new version is published, the previous version moves to a retired state, but is maintained for traceability. Completed and cancelled assessments aren't affected.

-   **[ServiceNow AI Lens form auto-filler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/c_form-auto-filler-fsm.md)**

    Capture an image using the mobile camera to automatically extract and populate smart assessment fields, reducing manual data entry effort for technicians. AI-powered image recognition analyzes the image and fills the extracted data in the relevant fields.

-   **[Respond to a reviewed work order task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/close-wo-wot-mobile.md)**

    View and resubmit smart assessment questionnaire responses that need additional information, enabling more informed and timely corrections of responses from job sites.

-   **[Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-engine.md)**

    Enhance scheduling accuracy and performance with [Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-engine.md)

    -   View comprehensive details for all optimization runs to quickly identify issues. Access standardized information about run status, included tasks and qualifiers, unassigned tasks with explanations, and the objectives and constraints applied during each optimization.
    -   Manage integrations more easily by configuring options to enable or disable third-party map providers beyond the default provider.
    -   Ensure only relevant tasks are processed by removing intraday events that don't meet specified criteria from both scheduled and prioritized optimization runs.
    -   Speed up high-volume scheduling by splitting groups or territories into smaller sets that process simultaneously. View how they are distributed using the **Job Distribution** column in both batch and intraday runs.
    -   Improve scheduling accuracy by introducing a **Window End Buffer Duration** field on the Work Order task record that enables you to configure a buffer duration that extends optimization beyond the defined window end so tasks are retained in the schedule.
    -   Speed up scheduling results by configuring matching rules to define which tasks and technicians are affected when a prioritized event occurs, such as identifying all technicians with matching certifications when someone calls in sick. You can enable matching rules per qualifier, then set criteria such as radius, skills, or time thresholds.
-   **[Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appointment-booking-administer.md)**

    Use [Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appointment-booking-administer.md) to perform the following tasks:

    -   Ensure better alignment with your operations by defining advanced lead time and cut-off logic through APIs or extension points. You can implement a custom script through an extension point based on job type, time of day, and day of week.
    -   Accommodate emergencies or priorities even if the capacity or appointment slots are full by enabling overbooking of appointments.
    -   Configure appointment slots to consider the holiday settings for a territory and display the available slots accordingly.
    -   Ensure guaranteed appointment slots by configuring availability checks to be performed at the time of slot retrieval so that any slot displayed is assured to be bookable without needing further capacity validation during the appointment booking.
    -   Ensure an accurate calculation of the duration for a task while booking an appointment by defining work and travel duration either in the appointment schedule configuration or in the schedule override configuration.
    -   Determine appointment availability using territory and demand channel mapping when contact or location details are not provided.
    -   Consider task dependencies while booking or rescheduling appointments and display the slots for the successor tasks after the estimated completion time including the defined lag time for the predecessor task.
-   **[Capacity and Reservations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-capacity-management.md)**

    Capacity and Reservations Management now enables you to perform the following tasks:

    -   Associate technicians with specific demand channels within a territory on a time-bound, recurring basis to model scheduling patterns based on union rules, part-time shifts, or regional strategies.
    -   Define agent-territory-demand channel associations with recurrence, start and end dates, and active status using the new Territory Resource Demand table.
    -   Filter agents based on supported demand channels during dynamic scheduling, schedule optimization, or manual scheduling.
    -   Calculate appointment booking availability in scripted mode based on agent demand channel recurrence.
-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Use Now Assist for FSM to manage shifts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-shift-manage.dita.md)**

    Use Now Assist for FSM to manage shift coverage through a conversational experience, including creating and viewing shifts.


## UI changes

-   **[Configure resources to load](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configure-resource-load.md)**

    Collapse mode on Dispatcher Workspace is now controlled by a system property that determines the number of resources loaded.


## Changed in this release

-   ****

    The following plugins are planned for deprecation in the C release. Beginning with the Australia release this plugin will be migrated to a store application. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed.

    Beginning with the Australia release, the following applications have been moved to the . Any application enhancements will be delivered through the related store app.

    -   [Advanced Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appintment-booking-day-level-config.md) \(com.snc.advanced\_appointment\_booking\)
    -   [Field Service Contractor Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-fsm-contractor-management.md) \(com.snc.fsm\_contractor\_management\)
    -   [Field Service Marketplace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-contractor-marketplace.md) \(com.snc.fsm\_marketplace\)
    -   [Field Service Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-territory-planning-fsm.md) \(com.snc.fsm\_territory\_planning\)
    -   Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\)
    -   [Field Service Capacity and Reservations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-capacity-management.md) \(com.snc.fsm\_capacity\_management\)
    -   [Field Service with Service Locations Support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/Configuring-service-location.md) \(com.snc.fsm\_service\_locations\)
    -   [Technician driven sales with Field Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/create-opportunity.md) \(com.snc.fsm\_technician\_sales\)
    -   [Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-engine-plugin.md) \(com.snc\_schedule\_optimization\)
    -   [Field Service Quality Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/config-quality-mgmt.md)
    -   [Field Service Mobile Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/setting-up-field-service-mobile-agent.md)
    -   Map Integrations for Field Service \(com.snc.app\_fsm\_map\_integr\)
    -   Beans.ai plugin \(com.sn\_beans\_ai\_spoke\)
    -   [Intelligent Task Recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/activate-intelligent-task-recommendation.md) \(sn\_fsm\_task\_rec\)
    -   [Field Service Management Scheduling Automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/activate-intraday-scheduling-plugin.md) \(sn\_fsm\_sched\_flws\)
    -   Application Common Configuration \(sn\_app\_cmn\_config\): This is a component of Dispatcher Workspace.
    -   Intelligent Task Recommendations \(sn\_task\_recommend\): This is a component of Intelligent Task Recommendations.
    -   Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\)
    -   Field Service Work Configurations \(com.snc.fsm\_work\_types\)
    -   Work Order Questionnaires \(com.snc.fsm\_questionnaire\)
    -   Work Order Management \(com.snc.work\_management\)
-   **[Google maps ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md)**

    The **google.maps.map\_id** system property enables Field Service Management to use Google Maps for cloud-based map styling, vector mapping, and advanced markers. You must obtain your own map ID.

-   **[Schedule Optimization features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/hard-soft-constraints.md)**

    The **Enable assignments only with preferred/secondary agents** constraint has been renamed to **Enable assignments based on technician assignment preference** and updated to restrict task assignment exclusively to technicians marked as required on the work order task. If no required technician is available or eligible, the task is dropped from optimization and logged in the run summary.

-   **[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control-rules.md)**

    Query range ACLs, which prevent unauthorized users from inferring sensitive data through repeated range-based queries, are now shipped by default. If you customized any of these ACLs in a previous release, your version remains active and the out-of-box ACL is set to inactive; otherwise, the default ACL replaces the previously generated one. The affected tables are:

    -   task\_rec\_m2m\_recommend\_policy\_criteria
    -   task\_rec\_recommendation\_applicability
    -   task\_rec\_recommendation\_criteria
    -   task\_rec\_recommendation\_policy
    -   app\_cmn\_field\_set
    -   app\_cmn\_field\_set\_item
    -   app\_cmn\_field\_set\_item\_user\_preference
    -   app\_cmn\_module
    -   app\_cmn\_sort\_option\_config
    -   app\_cmn\_state\_color\_config
    -   app\_cmn\_state\_color\_item

## Deprecated features

Starting with the Australia release, the **sn\_fsm\_disp\_wrkspc.calendarCollapsedBehavior** property has been removed and its behavior is now controlled by the **sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.calendar\_resources\_page\_size** property, which determines the number of resources loaded on the page.

## Activation information

Field Service Management is a ServiceNow AI Platform feature that is active by default.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Field Service Manager Mobile \(com.snc.fsm\_manager\_mobile\). For details, see [Activate Field Service Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/activate-manager-mobile.md). Mangers can manage their technicians and tasks using their mobile device.
    -   Field Service Manager Workforce \(com.snc.fsm\_manager\_workforce\). For details, see [Activate Field Service Manager Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/activate-workforce.md). Oversee agent schedules, manage resources, optimize territory coverage, and handle crew tasks and assignments to ensure efficient and effective coverage.
-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release.

    The following plugins are planned for deprecation in the C release. Beginning with the Australia release, this plugin will be migrated to a store application. When you upgrade your instance to at least the Australia release, the store applications will be automatically installed.

    -   Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\)
    -   Field Service Marketplace \(com.snc.fsm\_marketplace\)
    -   Marketplace Core \(com.snc.marketplace\_core\)
    -   Field Service Management Intelligent Task Recommendations \(com.snc.fsm\_task\_recommendations\)
    -   Field Service Management Scheduling Flows \(com.snc.sn\_app\_fsm\_scheduling\_flows\)
    -   Intelligent Task Recommendations \(com.snc.task\_recommendations\)
    -   Application Common Configuration \(com.snc.app\_cmn\_config\)
    -   Field Service Capacity Management \(com.snc.fsm\_capacity\_management\)
    -   Field Service Territory Planning \(com.snc.fsm\_territory\_planning\)
    -   Field Service with Service Locations support \(com.snc.fsm\_service\_locations\)
    -   Sales Mobile Common \(com.snc.sales\_mobile\_cmn\)
    -   Technician driven sales with Field Service \(com.snc.fsm\_technician\_sales\)
    -   Territory Planning \(com.snc.territory\_planning\)
    -   Field Service Mobile \(com.sn\_fsm\_mobile\)
    -   Field Service Quality Management \(com.sn\_fsm\_quality\)
    -   Quality Management \(com.sn\_quality\)
    -   Field Service Contractor Management \(com.snc.fsm\_contractor\_management\)
    -   Beans.AI Spoke \(com.sn\_beans\_ai\_spoke\)
    -   Map Integrations for Field Service \(com.snc.app\_fsm\_map\_integr\)
    -   Schedule Optimization \(com.snc\_schedule\_optimization\)
    -   Field Service Multi-Day Task Scheduling \(com.snc.fsm\_multiday\_tasks\)
    -   Field Service Management Access Hours Management \(com.snc.fsm\_access\_hours\)
    -   Work Order Questionnaires \(com.snc.wm\_questionnaire\)
    -   Work Order Management \(com.snc.work\_management\_core\)

## Related ServiceNow applications and features

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/customer-service-integration.md)**

    The Customer Service Management \(CSM\) with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and ServiceNow® Customer Service Management \(CSM\) applications to enable you to view account and contact information on work orders and work order tasks in the Field Service Management application.

-   **[Project Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/c_ProjectPortfolioSuite.md)**

    Field Service Management integrates with the ServiceNow® Service Portfolio Management application to enable you to create work orders directly from project tasks.

-   **[Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/workspace-landing-page.md)**

    ServiceNow® Workspace is a graphical user interface that provides multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are Customer Service-specific implementations that provide tier-1 agents with the tools needed to respond to customers and resolve cases.


-   **[Now Assist for FSM release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-fsm-rn.md)**  
The ServiceNow® Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Australia release.

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

