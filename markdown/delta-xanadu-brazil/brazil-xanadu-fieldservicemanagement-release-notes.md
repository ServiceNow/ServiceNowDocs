---
title: Combined Field Service Management release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Field Service Management from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-fieldservicemanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 16
breadcrumb: [Products combined by family]
---

# Combined Field Service Management release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Field Service Management from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Field Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Field Service Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Xanadu Patch 9 version or higher to ensure compatibility.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[Schedule Optimization features](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&family=xanadu&ft:locale=en-US)**

Use Schedule Optimization to do the following tasks:

    -   Use new objectives such as **Maximize SLA compliance buffers**, **Minimize task time penalties**, and **Maximize preferred agent assignments** when you're creating a policy.
    -   Define start-of-day and end-of-day location for territory users, improving scheduling accuracy by calculating travel times based on actual agent locations.
    -   Keep similar tasks together by scheduling pre-made bundles.
    -   Reduce the beans.ai travel estimate processing time with asynchronous processing.
    -   Access the Field Service Management Scheduling Health dashboard to view task metrics, technician metrics, and optimization configuration details.
    -   Enable dispatchers to influence the behavior of schedule optimization by allowing dispatchers to edit select fields on a work order task. Dispatchers can override work order task parameters, assign tasks based on technician preferences, and allow overtime.
-   **[Field Service Territory Capacity Analytics dashboard](https://www.servicenow.com/docs/access?context=capacity-dashboard&family=xanadu&ft:locale=en-US)**

Use the Field Service Territory Capacity Analytics dashboard for the following tasks:

    -   Use interactive charts and graphs to track capacity trends, including overall demand versus allocated capacity and capacity usage over time.
    -   Perform capacity gap analysis with a customizable pivot table view, which enables you to explore data by territory and demand channel.
    -   Apply filters to view specific data based on your setup, which enables targeted analysis and informed decision-making.
-   **[Agent relocation](https://www.servicenow.com/docs/access?context=relocate-agents-territories&family=xanadu&ft:locale=en-US)**

Manage your agents by performing the following tasks:

    -   Relocate agents from one territory to another for a particular duration.
    -   Facilitate precise destination territory selection, which ensures that each agent is placed in the most preferable location.
    -   Match resource availability with task requirements through improved schedule planning, which optimizes task execution and efficiently addresses unscheduled work.
    -   Minimize manual overhead and avoid manual tracking processes by simplifying the handling of temporary resource relocations.
-   **[Optimize agent operations with flexible work locations](https://www.servicenow.com/docs/access?context=change-agent-start-end-location&family=xanadu&ft:locale=en-US)**

Add flexible work locations for agents by performing the following tasks:

    -   Define different start-of-day and end-of-day locations for agents to start their day at one location and end at another location, providing flexibility in their operations.
    -   Offer additional flexibility by implementing exceptions to override default behaviors during specific periods.
    -   Improve scheduling accuracy by calculating travel times based on the agent's start and end locations.
-   **[Sales opportunity in Now Mobile Agent app](https://www.servicenow.com/docs/access?context=create-opportunity&family=xanadu&ft:locale=en-US)**

Enable field service technicians to perform the following the Now Mobile Agent application.

    -   Create sales opportunities directly from customer locations during field service visits.
    -   Access data to view, search, and filter sales opportunities.
-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=xanadu&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View multiple time zones to see agents who are available for work order tasks across multiple locations.
    -   Receive intelligent guidance about all possible scheduling options for unscheduled tasks. Rank scheduling options based on agent-to-task match percentage, distance, and more.
    -   Hide off-shift agents so dispatchers can focus on who’s available and ready for tasks at that moment.
-   **[Beans.ai map integration for bundled tasks](https://www.servicenow.com/docs/access?context=c_AutoRouting&family=xanadu&ft:locale=en-US)**

Optimize routes for bundled tasks with beans.ai.

-   **[Appointment booking enhancements](https://www.servicenow.com/docs/access?context=appointment-booking-administer&family=xanadu&ft:locale=en-US)**

Use appointment booking enhanced configurations to perform the following tasks:

    -   Book appointments for work order tasks.
    -   Enable the system to calculate or skip lead time when rescheduling appointments, depending on the selected configuration.
    -   Consider holidays when calculating lead time for appointments.
-   **[Field Service Marketplace enhancements](https://www.servicenow.com/docs/access?context=fsm-marketplace&family=xanadu&ft:locale=en-US)**
    -   Automate the process of pushing tasks to the marketplace, automatically creating marketplace requests, and listing eligible contractors as determined by your specified criteria.
    -   Set up task filters to identify the work order tasks that qualify for the marketplace.
    -   Incrementally push marketplace requests to eligible contractors based on their ranking using the **Progressive push** check box.
    -   Evaluate contractor responses and automatically assign tasks to the lowest-cost contractor using the **Response evaluation flow** field.
-   **[Field Service Quality Management](https://www.servicenow.com/docs/access?context=quality-management-fsm&family=xanadu&ft:locale=en-US)**

Use Field Service Quality Management to do the following tasks:

    -   Review the quality and data from work order tasks before completion.
    -   Address work orders that have been reviewed and sent back for more information.
    -   Provide feedback to technicians and communicate as needed during the review process.
-   **[Workforce enhancements](https://www.servicenow.com/docs/access?context=using-manager-workforce&family=xanadu&ft:locale=en-US)**

Use Workforce enhanced configurations to perform the following tasks:

    -   Extend access across all personas, allowing every user regardless of their role to view their own calendars.
    -   Configure settings to enable group and territory calendar visibility, authoring agents to view the list and calendars of members in their group or within their territory when Workforce Optimization for Field Service isn't enabled.
    -   Enable agents to create personal events for themselves.
-   **[Multiple Work Configurations](https://www.servicenow.com/docs/access?context=configuring-work-configs&family=xanadu&ft:locale=en-US)**

Create configurations for multiple work types, such as Installation, Repair, Break fix, and Maintenance.

    -   Set up work configurations for different work types ensuring that relevant work types and flows appear for specified business units or departments.
    -   Create Service Management configurations \(SM Configs\) to support multiple workflows.
    -   Extend the work order task table to account for different work types.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **Capacity and Reservations Management**

Capacity and Reservations Management data model has been changed to accommodate the agent's start and end location.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=xanadu&ft:locale=en-US)**

Dispatcher Workspace and Workforce Optimization for Field Service support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown) section that follows.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

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

Xanadu

</td><td>

The Field Service dashboard is removed from the Emergency Exposure Management application.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   Starting with the Xanadu release, FSM Agent Classic Workspace plugin \(com.snc.agent\_workspace.fsm\) is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

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

Xanadu

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is available with activation of the Field Service Management plugin \(field\_service\_management\). For details, see [Activate Field Service Management](https://www.servicenow.com/docs/access?context=t_ActivateFieldServiceManagement&family=xanadu&ft:locale=en-US).

 Additional Field Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Field Service Management](https://www.servicenow.com/docs/access?context=field-service-additional-plugins&family=xanadu&ft:locale=en-US).

 Enable field service technicians to initiate and monitor sales opportunities directly through the Now Mobile Agent application by activating Technician driven sales with the Field Service \(com.snc.fsm\_technician\_sales\) plugin.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Dispatcher Workspace and Workforce Optimization for Field Service workspace support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

In addition, the following pages were updated to support reflow:

    -   Territory planning
    -   Service location
    -   Geography
    -   Agent recommendation
This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=xanadu&ft:locale=en-US) for details.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   Move agents between territories, optimize scheduling, and minimize manual tracking while agents execute tasks.
-   Create and view sales opportunities during field service visits using the Now Mobile Agent application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

