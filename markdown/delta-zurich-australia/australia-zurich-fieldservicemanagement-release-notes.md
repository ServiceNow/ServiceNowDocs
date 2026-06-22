---
title: Combined Field Service Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Field Service Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-fieldservicemanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Field Service Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Field Service Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Field Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Field Service Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Using Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=zurich&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   Use the advanced resource filter to sort contractors and equipment.
    -   Add agents to Dispatcher Workspace to see their schedules, or assign them tasks if you manage the assignment group or territory they're a part of. This action can be done without loading the entire assignment group or territory that the agent is a member of.
    -   Set up the calendar to use multiple time zones at once. For more information, see [Show multiple time zones](https://www.servicenow.com/docs/access?context=use-stacked-time-zones&family=zurich&ft:locale=en-US).
    -   Navigate from a work order task to a related list of smart assessments that are associated with that work order.
-   **[Assigning WOTs manually](https://www.servicenow.com/docs/access?context=c_DispatchWorkOrderTasks&family=zurich&ft:locale=en-US)**

Use the records page to perform the following tasks that was limited to Dispatcher Workspace before:

    -   Flag a work order task.
    -   Use assignment assistance.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&family=zurich&ft:locale=en-US)**

Use Schedule Optimization to do the following:

    -   Initiate immediate optimization to adjust schedules and tasks when an in-day event occurs, like a new priority 1 task, a canceled task, an agent taking PTO, or an agent running late.
    -   Assign the best agent for a work order task based on agent efficiency, which helps schedule and assign tasks more appropriately, using Field Service Agent Efficiency.
    -   Define work, travel, and overtime penalty values for each agent so the optimization engine can either schedule a nearby agent with a higher penalty or a distant agent with a lower penalty.

    -   Improve task scheduling by assigning dependent tasks to a single technician within the same shift.
-   **[Workforce](https://www.servicenow.com/docs/access?context=configuring-workforce&family=zurich&ft:locale=en-US)**

Enable managers to show or hide work order tasks from the **Calendars** tab in Workforce. When Workforce Optimization for Field Service is enabled, these tasks can also be viewed in Hybrid and Map views.

-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&family=zurich&ft:locale=en-US)**

Manage resource attributes for any duration, whether a single day or multiple days.

-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&family=zurich&ft:locale=en-US)**

Use Appointment Booking to do the following:

    -   Enable better control over task sequencing using new dependency types, such as 'Finish to Start - Same Day' and 'Finish Together' with lag options, integrated with appointment booking for more precise scheduling. Enhance operational insight for all roles through improved visualizations including dependency trees, conflict alerts, and task indicators, which support dispatcher decisions and technician execution.
    -   Optimize appointment recommendations by allowing radius configuration at the territory level, tailored to diverse areas, such as urban versus rural. This capability includes an extension point for customers to implement custom radius logic with default instance-level values if no specific configuration is set.
    -   Enhance appointment recommendations by allowing grading against user-defined similar services rather than identical ones, resulting in more versatile scheduling options. This feature includes an extension point for customers to specify which services they consider similar, and the system defaults to same-catalog matching if no custom configuration is provided.
    -   Increase scheduling flexibility with new features to support slot overlap and overrides. This capability enables territory-based customization of appointment windows, default schedules, and specific slot-level overrides, giving more control over availability.

</td></tr><tr><td>

Australia

</td><td>

-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=australia&ft:locale=en-US)**

[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=australia&ft:locale=en-US) now enables you to perform the following tasks:

    -   Show multiple time zones on the map in Dispatcher Workspace with a segmented time indicator to see which time zone each Field Service technician is in. For more information, see [Time zones](https://www.servicenow.com/docs/access?context=time-zones-dispatcher&family=australia&ft:locale=en-US).
    -   Quickly see a work order task in the task panel and find it on the calendar rather than having to search through multiple days. For more information, see [Open tasks from the task list](https://www.servicenow.com/docs/access?context=open-task-platform-list&family=australia&ft:locale=en-US).
    -   See live traffic on the map in Dispatcher Workspace. For more information, see [Show map overlays in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=map-overlay-dispatcher&family=australia&ft:locale=en-US).
    -   Flag multiple tasks at once. For more information, see [Flag or unflag tasks from the list](https://www.servicenow.com/docs/access?context=flag-task-list-workspace&family=australia&ft:locale=en-US).
    -   Quickly find tasks in the calendar from the task list. For more information, see [Flag or unflag tasks from the list](https://www.servicenow.com/docs/access?context=flag-task-list-workspace&family=australia&ft:locale=en-US).
    -   View analytics, including the number of technicians without a work schedule or valid location. For more information, see [Scheduling Health dashboard](https://www.servicenow.com/docs/access?context=scheduling-health-dashboard&family=australia&ft:locale=en-US).
    -   Show an overtime indicator on the calendar to visually see which technicians have overtime tasks. For more information, see [Show overtime indicator](https://www.servicenow.com/docs/access?context=dispatcher-wrkspc-settings&family=australia&ft:locale=en-US).
    -   Control the size of the cells on the calendar to see shorter tasks more easily. For more information, see [Zoom in or out on the calendar](https://www.servicenow.com/docs/access?context=calendar-zoom-dispatcher&family=australia&ft:locale=en-US).
    -   Customize the information displayed in work order task popovers in Dispatcher Workspace to show the data most relevant to dispatchers. Popovers on the calendar, map, and task panel now support configurable field display, with a consistent visual experience across all three surfaces. For more information, see [Configure popover fields](https://www.servicenow.com/docs/access?context=configure-popover-fields&family=australia&ft:locale=en-US).
    -   Stay in the same position in the calendar in Dispatcher Workspace when you change from day to day. For more information, see [Properties installed](https://www.servicenow.com/docs/access?context=r_PropInstallWFieldServMgmnt&family=australia&ft:locale=en-US).
    -   The Assignment group task filter setting is moved from Dispatcher Workspace settings to the main Dispatcher Workspace page and is now a button. For more information, see [Search tasks](https://www.servicenow.com/docs/access?context=search-work-order-tasks&family=australia&ft:locale=en-US).
    -   Quickly edit tasks in Dispatcher Workspace directly from the contextual side panel. For more information, see [Quick edit tasks](https://www.servicenow.com/docs/access?context=quick-edit-tasks&family=australia&ft:locale=en-US).
    -   Add work notes or comments to work order tasks in Dispatcher Workspace from the activity stream. For more information, see [Add work notes or comments](https://www.servicenow.com/docs/access?context=activity-stream-csp&family=australia&ft:locale=en-US).
-   **[Field Service Manager Mobile](https://www.servicenow.com/docs/access?context=manager-mobile-app&family=australia&ft:locale=en-US)**

Field Service Managers can do their work from anywhere on their mobile device, including the following tasks:

    -   [Manage Field Service technicians from Field Service Manager mobile](https://www.servicenow.com/docs/access?context=mange-agents-mobile&family=australia&ft:locale=en-US)
    -   [Create a work order task](https://www.servicenow.com/docs/access?context=create-task-manager-mobile&family=australia&ft:locale=en-US)
    -   [Create a personal event](https://www.servicenow.com/docs/access?context=event-manager-mobile&family=australia&ft:locale=en-US)
    -   [View analytics from Field Service Manager Mobile](https://www.servicenow.com/docs/access?context=view-analytics-manager&family=australia&ft:locale=en-US)
-   **[Locations on personal events](https://www.servicenow.com/docs/access?context=create-personal-event&family=australia&ft:locale=en-US)**

See locations for personal events regardless of where they're created in Field Service Management applications including Dispatcher Workspace and Field Service Manager Mobile.

-   **[ServiceNow Agent mobile app](https://www.servicenow.com/docs/access?context=Use-mobile-app-fsm&family=australia&ft:locale=en-US)**
    -   Generate work summary reports and capture signatures in them at the work order task level along with the existing work order level. Additionally, you can view responses and score information for the smart assessment questionnaires in the work summary report.
    -   Perform asset audits for the technician's personal stockroom to verify and reconcile assets between a physical stockroom and the data on the ServiceNow instance.
-   **[Configuring Smart Assessment from new templates](https://www.servicenow.com/docs/access?context=configure-sa-from-new-template&family=australia&ft:locale=en-US)**

Create versions of published smart assessment templates to add or modify questions and instructions. When a new version is published, the previous version moves to a retired state, but is maintained for traceability. Completed and cancelled assessments aren't affected.

-   **[ServiceNow Lens form auto-filler](https://www.servicenow.com/docs/access?context=c_form-auto-filler-fsm&family=australia&ft:locale=en-US)**

Capture an image using the mobile camera to automatically extract and populate smart assessment fields, reducing manual data entry effort for technicians. AI-powered image recognition analyzes the image and fills the extracted data in the relevant fields.

-   **[Respond to a reviewed work order task](https://www.servicenow.com/docs/access?context=respond-task-review-mobile&family=australia&ft:locale=en-US)**

View and resubmit smart assessment questionnaire responses that need additional information, enabling more informed and timely corrections of responses from job sites.

-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&family=australia&ft:locale=en-US)**

Enhance scheduling accuracy and performance with [Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&family=australia&ft:locale=en-US)

    -   View comprehensive details for all optimization runs to quickly identify issues. Access standardized information about run status, included tasks and qualifiers, unassigned tasks with explanations, and the objectives and constraints applied during each optimization.
    -   Manage integrations more easily by configuring options to enable or disable third-party map providers beyond the default provider.
    -   Ensure only relevant tasks are processed by removing intraday events that don't meet specified criteria from both scheduled and prioritized optimization runs.
    -   Speed up high-volume scheduling by splitting groups or territories into smaller sets that process simultaneously. View how they are distributed using the **Job Distribution** column in both batch and intraday runs.
    -   Improve scheduling accuracy by introducing a **Window End Buffer Duration** field on the Work Order task record that enables you to configure a buffer duration that extends optimization beyond the defined window end so tasks are retained in the schedule.
    -   Speed up scheduling results by configuring matching rules to define which tasks and technicians are affected when a prioritized event occurs, such as identifying all technicians with matching certifications when someone calls in sick. You can enable matching rules per qualifier, then set criteria such as radius, skills, or time thresholds.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&family=australia&ft:locale=en-US)**

Use [Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&family=australia&ft:locale=en-US) to perform the following tasks:

    -   Ensure better alignment with your operations by defining advanced lead time and cut-off logic through APIs or extension points. You can implement a custom script through an extension point based on job type, time of day, and day of week.
    -   Accommodate emergencies or priorities even if the capacity or appointment slots are full by enabling overbooking of appointments.
    -   Configure appointment slots to consider the holiday settings for a territory and display the available slots accordingly.
    -   Ensure guaranteed appointment slots by configuring availability checks to be performed at the time of slot retrieval so that any slot displayed is assured to be bookable without needing further capacity validation during the appointment booking.
    -   Ensure an accurate calculation of the duration for a task while booking an appointment by defining work and travel duration either in the appointment schedule configuration or in the schedule override configuration.
    -   Determine appointment availability using territory and demand channel mapping when contact or location details are not provided.
    -   Consider task dependencies while booking or rescheduling appointments and display the slots for the successor tasks after the estimated completion time including the defined lag time for the predecessor task.
-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&family=australia&ft:locale=en-US)**

Capacity and Reservations Management now enables you to perform the following tasks:

    -   Associate technicians with specific demand channels within a territory on a time-bound, recurring basis to model scheduling patterns based on union rules, part-time shifts, or regional strategies.
    -   Define agent-territory-demand channel associations with recurrence, start and end dates, and active status using the new Territory Resource Demand table.
    -   Filter agents based on supported demand channels during dynamic scheduling, schedule optimization, or manual scheduling.
    -   Calculate appointment booking availability in scripted mode based on agent demand channel recurrence.
-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Manage shifts with Now Assist](https://www.servicenow.com/docs/access?context=now-assist-shift-manage.dita&family=australia&ft:locale=en-US)**

Use Now Assist for FSM to manage shift coverage through a conversational experience, including creating and viewing shifts.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Field Service Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&family=zurich&ft:locale=en-US)**

Use the aggregated schedules of all agents of a territory to allocate resources until a specified cut-off date, after which predicted capacity can be used for bookings. This feature optimizes resource utilization and capacity management for a territory, which helps ensure that business services remain available without overburdening resources.

-   **[Google Maps APIs for  Field Service  capabilities](https://www.servicenow.com/docs/access?context=google-maps-api-keys&family=zurich&ft:locale=en-US)**

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you create a Google API key after March 2025, you must upgrade to a supported ServiceNow release version to verify compatibility.

-   **[Smart Assessment for Field Service](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&family=zurich&ft:locale=en-US)**

Use Smart Assessment for Field Service to do the following:

    -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
    -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
    -   View completed questionnaires in the workspace.
    -   Create follow-up work order tasks from a work order questionnaire based on the responses.
    -   Allow users to retry or replace an attachment if the upload is unsuccessful.
-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&family=zurich&ft:locale=en-US)**

Migrates data from the Work Parameter table to the Resource Schedule Attribute table for each technician, confirming that work parameters align with the new schedule attributes.


</td></tr><tr><td>

Australia

</td><td>

-   **[\[Placeholder link text to key external.sn-app-store\]](https://www.servicenow.com/docs/access?context=external.sn-app-store&family=australia&ft:locale=en-US)**

The following plugins are planned for deprecation in the C release. Beginning with the Australia release this plugin will be migrated to a store application. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed.

Beginning with the Australia release, the following applications have been moved to the [\[Placeholder link text to key external.sn-app-store\]](https://www.servicenow.com/docs/access?context=external.sn-app-store&family=australia&ft:locale=en-US). Any application enhancements will be delivered through the related store app.

    -   [Advanced Appointment Booking](https://www.servicenow.com/docs/access?context=appintment-booking-day-level-config&family=australia&ft:locale=en-US) \(com.snc.advanced\_appointment\_booking\)
    -   [Field Service Contractor Management](https://www.servicenow.com/docs/access?context=configuring-fsm-contractor-management&family=australia&ft:locale=en-US) \(com.snc.fsm\_contractor\_management\)
    -   [Field Service Marketplace](https://www.servicenow.com/docs/access?context=configuring-contractor-marketplace&family=australia&ft:locale=en-US) \(com.snc.fsm\_marketplace\)
    -   [Field Service Territory Planning](https://www.servicenow.com/docs/access?context=configuring-territory-planning-fsm&family=australia&ft:locale=en-US) \(com.snc.fsm\_territory\_planning\)
    -   Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\)
    -   [Field Service Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&family=australia&ft:locale=en-US) \(com.snc.fsm\_capacity\_management\)
    -   [Field Service with Service Locations Support](https://www.servicenow.com/docs/access?context=Configuring-service-location&family=australia&ft:locale=en-US) \(com.snc.fsm\_service\_locations\)
    -   [Technician driven sales with Field Service](https://www.servicenow.com/docs/access?context=create-opportunity&family=australia&ft:locale=en-US) \(com.snc.fsm\_technician\_sales\)
    -   [Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine-plugin&family=australia&ft:locale=en-US) \(com.snc\_schedule\_optimization\)
    -   [Field Service Quality Management](https://www.servicenow.com/docs/access?context=config-quality-mgmt&family=australia&ft:locale=en-US)
    -   [Field Service Mobile Agent](https://www.servicenow.com/docs/access?context=setting-up-field-service-mobile-agent&family=australia&ft:locale=en-US)
    -   Map Integrations for Field Service \(com.snc.app\_fsm\_map\_integr\)
    -   Beans.ai plugin \(com.sn\_beans\_ai\_spoke\)
    -   [Intelligent Task Recommendations](https://www.servicenow.com/docs/access?context=activate-intelligent-task-recommendation&family=australia&ft:locale=en-US) \(sn\_fsm\_task\_rec\)
    -   [Field Service Management Scheduling Automations](https://www.servicenow.com/docs/access?context=activate-intraday-scheduling-plugin&family=australia&ft:locale=en-US) \(sn\_fsm\_sched\_flws\)
    -   Application Common Configuration \(sn\_app\_cmn\_config\): This is a component of Dispatcher Workspace.
    -   Intelligent Task Recommendations \(sn\_task\_recommend\): This is a component of Intelligent Task Recommendations.
    -   Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\)
    -   Field Service Work Configurations \(com.snc.fsm\_work\_types\)
    -   Work Order Questionnaires \(com.snc.fsm\_questionnaire\)
    -   Work Order Management \(com.snc.work\_management\)
-   **[Google maps ID](https://www.servicenow.com/docs/access?context=r_PropInstallWFieldServMgmnt&family=australia&ft:locale=en-US)**

The **google.maps.map\_id** system property enables Field Service Management to use Google Maps for cloud-based map styling, vector mapping, and advanced markers. You must obtain your own map ID.

-   **[Schedule Optimization features](https://www.servicenow.com/docs/access?context=hard-soft-constraints&family=australia&ft:locale=en-US)**

The **Enable assignments only with preferred/secondary agents** constraint has been renamed to **Enable assignments based on technician assignment preference** and updated to restrict task assignment exclusively to technicians marked as required on the work order task. If no required technician is available or eligible, the task is dropped from optimization and logged in the run summary.

-   **[Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&family=australia&ft:locale=en-US)**

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Field Service Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Field Service Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Non-collapsed mode is being deprecated and removed from Dispatcher Workspace. Dispatchers must use collapsed mode to see available resources in Dispatcher Workspace.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being deprecated. It will no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Field Service Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Use the aggregated agent schedule to optimize the allocation of resources for a territory up to the specified cut-off date.
-   Flag a task or use assignment assistance directly from the Work Order Task page to streamline task management.
-   Configure Schedule Optimization to instantly adjust technician schedules in response to real-time events, like new priority 1 tasks, task cancellations, paid time off requests, or delays.

 See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Increase productivity by Field Service Managers, who can do their work from anywhere on their mobile device with Field Service Manager Mobile.
-   Allow overbooking in priority cases, consider holidays at the territory level, enable flexible sourcing for work and travel times, and consider task dependencies when scheduling or rescheduling appointments through advanced lead-time management.
-   Determine appointment availability by using territory through APIs, without providing specific contact or location information.
-   View run summaries in Schedule Optimization to understand what was evaluated during scheduling, including objectives, constraints, travel mode, and assignment outcomes.
-   Review the Field Service Management features and activation plugins now available through the ServiceNow Store application. For more details, see the "Changed in the Release" section.

 See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

