---
title: Combined Field Service Management release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Field Service Management from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-fieldservicemanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Field Service Management release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Field Service Management from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Field Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Field Service Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Upgrade information**
    -   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
    -   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Schedule Optimization v1.2 support for overlapping territories during prioritized optimization](https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-schedule-optimization.html)**

Expand prioritized event optimization to include overlapping territories when determining the technicians and tasks directly impacted by an event. Configure a search radius at the qualifier level to control which overlapping territories are considered.

-   **[Schedule Optimization v1.2 supports matching rules with four additional matching dimensions for prioritized event optimization](https://www.servicenow.com/docs/access?context=triggering-optimization-on-task-or-agent-availability-change&family=brazil&ft:locale=en-US)**

Matching rules for prioritized event optimization now support four additional matching dimensions that enable you to filter technicians and tasks based on specific criteria:

    -   retrieve tasks based on skills
    -   retrieve technicians based on skills
    -   retrieve tasks within radius
    -   retrieve technicians within radius
Combine matching dimensions using AND logic \(all must match\) and OR logic \(any can match\) to more precisely identify which technicians and tasks are directly impacted by events. Configure matching dimensions at the qualifier level to define which technicians and tasks are considered for assignment.

-   **[Schedule Optimization v2.0 skill level and skill expiration support](https://www.servicenow.com/docs/access?context=skills-table-fields&family=brazil&ft:locale=en-US)**

Control how skill requirements are evaluated during Schedule Optimization. Define whether a task requires a specific skill level or any level of a skill, and configure start and end dates for technician skills. Schedule Optimization assigns only technicians with valid qualifications.

-   **[Schedule Optimization v 2.0 expanded Run Summary details](https://www.servicenow.com/docs/access?context=monitoring-schedule-optimization-runs&family=brazil&ft:locale=en-US)**

Gain more visibility into Schedule Optimization results. The Run Summary now displays the optimization horizon, including the start and end dates of the optimization window, and shows all shifts considered during optimization with status and reason codes. Review job-level and qualifier-level optimization metrics and shift plans with their assigned tasks.

-   **[Schedule Optimization v2.0 support time-bound availability of demand channel in a territory](https://www.servicenow.com/docs/access?context=hard-soft-constraints&family=brazil&ft:locale=en-US)**

Assign tasks only to eligible technicians based on the demand channel mapping and availability. For example, a technician mapped to Installation demand channel on Mondays is assigned only Installation tasks scheduled on Mondays.

-   **[Dispatcher Workspace v11.0 view breaks](https://www.servicenow.com/docs/access?context=view-task-calendar&family=brazil&ft:locale=en-US)**

View break and lunch details directly within task events on the calendar in Dispatcher Workspace. Dispatchers no longer need to open a separate record to see when an agent is on break. Lunch breaks can be viewed directly within scheduled tasks.

-   **[Proxy Actions v1.0](https://www.servicenow.com/docs/access?context=configure-proxy-fsm&family=brazil&ft:locale=en-US)**

Proxy Actions let an agent or manager perform specific actions on a work order task on behalf of another technician — someone other than the person the task is actually assigned to. Proxy action policies are administered through a dedicated policy form. The Proxy Admin role automatically inherits delegation admin permissions.

-   **[Manager Workforce v2.0](https://www.servicenow.com/docs/access?context=using-team-calendar&family=brazil&ft:locale=en-US)**

Embedded lunch breaks are now visible and editable directly within Workforce, with break status icons updating automatically as break state changes. Technicians and managers can track and manage break status changes. Lunch breaks can now be embedded directly within scheduled tasks rather than tracked as separate events.

-   **[Scheduling AI Agent Collections v2.0](https://www.servicenow.com/docs/access?context=now-assist-shift-manage&family=brazil&ft:locale=en-US)**

ServiceNow Otto for FSM can now update and delete shifts and schedules on request.

-   **[Shift Scheduling v8.0](https://www.servicenow.com/docs/access?context=embedded-breaks-and-lunches&family=brazil&ft:locale=en-US)**

Embed breaks and lunches directly within a work order task. Breaks can transition automatically at their scheduled start and end time, or require manual action from the technician, based on the new Auto-status breaks setting. Either way, the work order task pauses and resumes with the break, with the change logged to the work notes in a work order task.

-   **[FSM Configurable Dispatcher Workspace Bundle v11.0](https://www.servicenow.com/docs/access?context=quick-filters-dw&family=brazil&ft:locale=en-US)**

Dispatchers can build quick filters for the task panel and calendar using criteria such as skill, parts, and SLA breach. A task filter removes tasks that don't match, while a calendar filter grays them out instead of removing them.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Field Service Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Schedule Optimization**

The Run Summary "Technicians" tab is renamed to "Dropped Technicians".


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Field Service Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Field Service Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Schedule Optimization custom queue properties removed in v2.0**

Starting with the Brazil release, the following Schedule Optimizationcustom queue properties are no longer deployed, enhanced, or supported:

    -   sn\_schedule\_optim.data\_processor\_number\_of\_queues
    -   sn\_schedule\_optim.solution\_processor\_number\_of\_queues
    -   Claim limit properties for all data queues \(1–8\) and all event queues \(1–8\)
    -   Event distribution properties for all data queues \(1–8\) and all event queues \(1–8\)
These properties have been replaced by Queue Registries. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Field Service Management is a ServiceNow AI Platform feature that is active by default.

Leverage advanced features of Appointment Booking, such as the appointment slot recommendation, by activating the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin.

Define the task dependencies for a work order task and schedule tasks based on the dependency by activating the Field Service Task Dependencies \(com.snc.fsm\_task\_dependency\) plugin.

Integrate agent efficiency metrics with Field Service Management to define and use the efficiency of agents to estimate the work duration for tasks by activating the FSM Agent Efficiency \(com.snc.fsm\_agent\_efficiency​\) plugin.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Field Service Management is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Field Service Management is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

-   Define configurable rules that you can use to derive recommendation scores and optimize your appointment booking slots.
-   Create advanced dependency relationships among tasks to enhance scheduling accuracy.
-   Optimize your task assignments by using dependencies that align with the overall objectives and constraints of your resource allocation.
-   Streamline your capacity and resource management by using enhanced visualization in the Capacity Console.
-   Calculate the work duration for a work order task more accurately by using the Agent Efficiency feature.

 See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

