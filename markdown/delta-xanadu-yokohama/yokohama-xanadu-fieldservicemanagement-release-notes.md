---
title: Combined Field Service Management release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Field Service Management from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-fieldservicemanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Field Service Management release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Field Service Management from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Field Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Field Service Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

-   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
-   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Field Service Management.

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

-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View the Field Service agent’s real-time location and completed daily route.
    -   Use a condition builder to filter relevant resources. You can also extend existing tables to filter custom fields.
    -   Use advanced filters with hierarchical structures to filter territories.
    -   View task scheduling conflict messages in the Dispatcher Workspace to improve visibility and facilitate resolutions for dispatchers.
-   **[Field Service Agent Efficiency](https://www.servicenow.com/docs/access?context=configuring-agent-efficiency&family=yokohama&ft:locale=en-US)**

Use Agent Efficiency to perform the following tasks:

    -   Define the agent efficiency criteria to calculate the Agent Efficiency for a task.
    -   Calculate the estimated work duration for a work order task more accurately based on the Agent Efficiency feature.
    -   Enhance manual task assignment and dynamic scheduling for a task by leveraging Agent Efficiency.
    -   Optimize Intelligent Task Recommendation by incorporating Agent Efficiency values so that dispatchers can assign tasks more effectively.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&family=yokohama&ft:locale=en-US)**

Use Appointment Booking to perform the following tasks:

    -   Replicate the application and service-based configurations across instances.
    -   Grade the appointment booking slots by recommended or available slots to ensure optimal scheduling.
    -   Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.
-   **[Task dependencies](https://www.servicenow.com/docs/access?context=t_SetAnUpstreamTask&family=yokohama&ft:locale=en-US)**

Use task dependencies to perform the following tasks:

    -   Enable administrators and dispatchers to define advanced task dependencies, such as start together or start after start, so that you can ensure that tasks are executed in the right order.
    -   Enable dispatchers to create task dependencies within or between work orders.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&family=yokohama&ft:locale=en-US)**

Use Schedule Optimization to perform the following tasks:

    -   Enable dispatchers to optimize resource assignments that are based on the dependency relationship between tasks.
    -   Generate more accurate scheduling and assist your field technicians in navigating traffic conditions more effectively by configuring Schedule Optimization. You can consider time-of-day and set up intraday scheduling to leverage real-time traffic data when certain conditions are met.
    -   Use new optimization features, such as **Maximize consecutive collocated task assignments** and **Minimize task start times**, when you're creating a policy.
    -   Provide greater control over task distribution by enabling a new drip feed property, **Number of tasks**, to enhance your scheduling capabilities.
    -   Expect more reliable and efficient task scheduling due to resolved conflicts between the various scheduling engines.
    -   View the task scheduling conflict messages on the task, user, and group records when optimization is in progress.
-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=capacity-management&family=yokohama&ft:locale=en-US)**

Use Capacity and Reservations Management to perform the following tasks:

    -   Leverage the capacity console to efficiently manage resource allocation across territories and demand channels so that you can enable your teams to analyze field technician performance and make data-driven decisions.
    -   Set flexible reservation rules to define the minimum and maximum resource allocations so that you can enable dynamic adjustments to capacity based on shifting demands.
    -   Create recurring capacity assignments for specific days of the week for long-term capacity planning and management.
    -   Enable multiple overrides for the same date range to address demand fluctuations so that you can manage exceptions with more precision and flexibility.
-   **[Scheduling Health dashboard](https://www.servicenow.com/docs/access?context=scheduling-health-dashboard&family=yokohama&ft:locale=en-US)**

Use the Scheduling Health dashboard to view these additional Schedule Optimization metrics:

    -   Tasks without skills
    -   Technicians without skills
    -   Tasks without parts
    -   Technicians without parts
-   **[Business location-based work management](https://www.servicenow.com/docs/access?context=industry-products-integration&family=yokohama&ft:locale=en-US)**

Enable your staff across various industries to efficiently manage work orders. Your employees can resolve tasks that are specific to their assigned location, while your managers can oversee the tasks across their assigned locations. You can reinforce your security by ensuring that your staff can only access the work orders that are related to their designated locations.

-   **[Managing agents and tasks from Workforce](https://www.servicenow.com/docs/access?context=using-manager-workforce&family=yokohama&ft:locale=en-US)**

Use Workforce to perform the following tasks:

    -   Enable additional users to use Workforce by adding additional managers to assignment groups.
    -   Enable managers to view the event management tab when Workforce Optimization for Field Service is active.
-   **[Smart Assessment for Field Service Questionnaire](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&family=yokohama&ft:locale=en-US)**

Use Smart Assessment templates to perform the following tasks:

    -   Migrate from a survey-based questionnaire to Smart Assessment based questionnaires.
    -   Create work order questionnaires.
    -   Set up detailed instructions that include rich text and images.
    -   Configure conditional questions based on responses of all other types of questions and across sections.
    -   Allow additional comments or attachments on a question's response.
    -   Improve the work order questionnaire in the Mobile Agent® application by implementing a paginated layout, providing instructions with questions, and offering in-line choices.
-   **[Planned Work Management](https://www.servicenow.com/docs/access?context=migrate-maint-plans-pwm&family=yokohama&ft:locale=en-US)**

Seamlessly migrate monthly and annual plans from Planned Maintenance to Planned Work Management.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Field Service Management features.

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

Dispatcher Workspace and Workforce Optimization for Field Service support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown) section that follows.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[SLAs in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

The SLAs breached query on the Dispatcher Dashboard in Dispatcher Workspace has been updated to look at the SLAs that are associated with the work order tasks only instead of the work orders and work order tasks. The SLA breached counter on the task cards is also static, instead of real time. For more information on changing the SLA timer on task cards, see the Enable the **SLA timer on work order task cards** property on [Configure settings for Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configure-workspce-settings&family=yokohama&ft:locale=en-US).

-   **[Assignment groups and territories in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

You must save the default assignment groups or territories in Dispatcher Workspace to load when you open Dispatcher Workspace. If you don’t have the defaults saved, then you must select the assignment groups or territories to appear every time you open Dispatcher Workspace. This change is made to improve the performance of Dispatcher Workspace. For more information on saving the default assignment groups, see the Groups section on the **General** tab on [Enable Dispatcher Workspace settings](https://www.servicenow.com/docs/access?context=dispatcher-wrkspc-settings&family=yokohama&ft:locale=en-US). For information on saving default territories, see [Select Territories in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=select-territory-dispatch&family=yokohama&ft:locale=en-US). Administrators can disable this by setting the **sn\_fsm\_disp\_wrkspc.enableEmptyState** system property to false.

-   **[Work order questionnaire](https://www.servicenow.com/docs/access?context=complete-questionnaire-mobile-app&family=yokohama&ft:locale=en-US)**

Availability of inline choices for a question and the ability to add additional information for a question when completing a work order questionnaire through the Now Mobile Agent application.

-   **Role to access opportunities**

The Opportunity Writer sn\_opty\_mgmt\_core.opportunity\_writer role has been replaced with the Opportunity Contributor sn\_opty\_mgmt\_core.opportunity\_contributor role. Field service technicians can use the new Opportunity Contributor\[sn\_opty\_mgmt\_core.opportunity\_contributor role to create and view opportunities.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Field Service Management features or functionality were removed.

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

The approval for new requests workflow was removed from the Field Service Management Business Process configuration. Existing customers that use this workflow are unaffected. New customers can use ServiceNow® Workflow Studio to build the approval for the new requests workflow. For more information on Workflow Studio, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Field Service Management features or functionality were deprecated.

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

-   Starting with the Yokohama release, Approval Workflow for FSM is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

Field Service Management is a ServiceNow AI Platform feature that is active by default.

 Leverage advanced features of Appointment Booking, such as the appointment slot recommendation, by activating the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin.

 Define the task dependencies for a work order task and schedule tasks based on the dependency by activating the Field Service Task Dependencies \(com.snc.fsm\_task\_dependency\) plugin.

 Integrate agent efficiency metrics with Field Service Management to define and use the efficiency of agents to estimate the work duration for tasks by activating the FSM Agent Efficiency \(com.snc.fsm\_agent\_efficiency​\) plugin.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

