---
title: Combined Field Service Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Field Service Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-fieldservicemanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 27
breadcrumb: [Products combined by family]
---

# Combined Field Service Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Field Service Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Field Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Field Service Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Xanadu Patch 9 version or higher to ensure compatibility.

</td></tr><tr><td>

Yokohama

</td><td>

-   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
-   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

</td></tr><tr><td>

Zurich

</td><td>

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Schedule Optimization features](https://servicenow-staging.fluidtopics.net/access?context=schedule-optimization-engine&family=washingtondc&ft:locale=en-US)**

Use Schedule Optimization to do the following tasks:

    -   Schedule complex multi-territory assignments where an agent might be responsible for multiple territories over a longer batch processing period.
    -   Assign tasks to agents regardless of whether they’re primary or secondary members of a single or multiple territories.
    -   Optimize task scheduling by defining the capacity of your agents or work type.
    -   Provide smoother intra-day operations and efficient resource allocation when a single agent might need to handle multiple territories within the same day or across different shifts.
    -   Use new objectives such as **Maximize Assignment to Earlier Shifts**, **Minimize Highest Priority Task Start Times**, and **Minimize SLA Violation** when you're creating a policy.
    -   Use the improved configuration process for batch and intra-day scheduling,which provides common settings for both types while maintaining specific configurations where needed. With this process, you can eliminate duplication and ensure an efficient setup.
    -   Improve your schedule accuracy and adherence and also reduce scheduling changes when intra-day is running through two new system properties.
-   **[Dispatcher Workspace features](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=washingtondc&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   Enable dispatchers to run Schedule Optimization throughout the day as scheduling conditions change.
    -   Create crews that are based on territory memberships.
    -   View your contractor capacity by territory in the calendar view.
    -   View agents on the calendar by their availability in the territory.
    -   Create personal events for Field Service agents to show when they are unavailable for non-work order reasons like an appointment or a phone call they have scheduled.
    -   Change the amount of time shown on the calendar to time intervals of 15, 30, 45, or 60 minutes.
    -   Send messages to agents to discuss work order tasks.
    -   Make bulk updates for your calendar events to save time.
    -   Source one or more parts from a preferred stockroom or assignment group and then transfer them to your personal stockroom to ensure the prompt completion of work order tasks.
-   **[Beans.ai map integration for travel estimates](https://servicenow-staging.fluidtopics.net/access?context=r_PropInstallWFieldServMgmnt&family=washingtondc&ft:locale=en-US)**

Use beans.ai, a new map provider, for travel time estimates for Dynamic Scheduling, Route Optimization, manual task assignment, and agent estimated time arrivals.

-   **[Territory Planning features](https://servicenow-staging.fluidtopics.net/access?context=configuring-territory-planning-fsm&family=washingtondc&ft:locale=en-US)**

Use Territory Planning to do the following tasks:

    -   Create territory-specific crews to streamline territory management, task scheduling, and resource allocation.
    -   Link multiple geographies to one territory by using a composite geography capability that simplifies the representation of complex areas and enables you to have more data management flexibility.
    -   Manage the territories, customized hour ranges, tasks, and agent schedules for your internal agents and contractors so that you can allocate your resources accurately.
-   **[Field Service Marketplace](https://servicenow-staging.fluidtopics.net/access?context=configuring-contractor-marketplace&family=washingtondc&ft:locale=en-US)**

Enable Field Service dispatchers to post tasks on an exclusive contractor marketplace, where contractor companies with skilled workers can offer cost estimates and their availability. Your dispatchers can interact with qualified contractors and select the most suitable contractor for the task.

-   **[Now Assist for Field Service Management \(FSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-fsm&family=washingtondc&ft:locale=en-US)**

Use Now Assist for FSM to summarize work order tasks.

    -   Create work order task summaries during any state of the work order task to track progress.
    -   Create task closure summaries when completing tasks on the mobile application to provide notes for future reference.
-   **[Start of week Appointment Booking](https://servicenow-staging.fluidtopics.net/access?context=configure-week-appt-book&family=washingtondc&ft:locale=en-US)**

Enable the system to start booking an appointment on the first day of a week or a day other than the default Sunday.

-   **[Task initiator Role](https://servicenow-staging.fluidtopics.net/access?context=r_UserRoleInstallWFieldSrvMgmnt&family=washingtondc&ft:locale=en-US)**

Enable work order initiators to qualify work orders in the draft state with the new task initiator role.

Users with a task initiator role can perform the following actions on work orders or tasks that are in the draft state:

    -   Apply a work order template
    -   Add or modify work order tasks
    -   Add or modify part requirements
-   **[Enhanced mobile experience to reserve parts](https://servicenow-staging.fluidtopics.net/access?context=request-inventory&family=washingtondc&ft:locale=en-US)**

Choose whether to reserve a part in a personal stockroom or source it from another stockroom depending on the part's availability when fulfilling or sourcing part requests.

-   **[Linear assets support](https://servicenow-staging.fluidtopics.net/access?context=linear-asset-management&family=washingtondc&ft:locale=en-US)**

Enable the work order initiator or qualifier to perform the following actions:

    -   View the linear asset geometry on the service location maps and pinpoint the work location.
    -   View the linear asset geometry on the map interface and select the start and end locations on the linear assets so that you can create a service location.
Enable agents to perform the following actions when working on linear asset inspection tasks:

    -   Review the start and end location details of a linear asset.
    -   Locate the asset start and end location on a map interface. The start date and work context should be highlighted on the linear asset.
    -   Inspect the different linear asset segments that need to be worked on.
    -   Create a work order task with an accurate point location on the linear asset or segment.
-   **[Suggest parts with Predictive Intelligence](https://servicenow-staging.fluidtopics.net/access?context=predictive-intelligence-fsm&family=washingtondc&ft:locale=en-US)**

Take advantage of automatic suggestions for required parts for work order tasks by using the Predictive Intelligence solution.

-   **[Workforce features](https://servicenow-staging.fluidtopics.net/access?context=using-manager-workforce&family=washingtondc&ft:locale=en-US)**

View the task and action descriptions of the work order tasks in the contextual side panel. Establish the default start and end times for new events directly on the **Event Management** tab.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Schedule Optimization features](https://servicenow-staging.fluidtopics.net/access?context=schedule-optimization-engine&family=xanadu&ft:locale=en-US)**

Use Schedule Optimization to do the following tasks:

    -   Use new objectives such as **Maximize SLA compliance buffers**, **Minimize task time penalties**, and **Maximize preferred agent assignments** when you're creating a policy.
    -   Define start-of-day and end-of-day location for territory users, improving scheduling accuracy by calculating travel times based on actual agent locations.
    -   Keep similar tasks together by scheduling pre-made bundles.
    -   Reduce the beans.ai travel estimate processing time with asynchronous processing.
    -   Access the Field Service Management Scheduling Health dashboard to view task metrics, technician metrics, and optimization configuration details.
    -   Enable dispatchers to influence the behavior of schedule optimization by allowing dispatchers to edit select fields on a work order task. Dispatchers can override work order task parameters, assign tasks based on technician preferences, and allow overtime.
-   **[Field Service Territory Capacity Analytics dashboard](https://servicenow-staging.fluidtopics.net/access?context=capacity-dashboard&family=xanadu&ft:locale=en-US)**

Use the Field Service Territory Capacity Analytics dashboard for the following tasks:

    -   Use interactive charts and graphs to track capacity trends, including overall demand versus allocated capacity and capacity usage over time.
    -   Perform capacity gap analysis with a customizable pivot table view, which enables you to explore data by territory and demand channel.
    -   Apply filters to view specific data based on your setup, which enables targeted analysis and informed decision-making.
-   **[Agent relocation](https://servicenow-staging.fluidtopics.net/access?context=relocate-agents-territories&family=xanadu&ft:locale=en-US)**

Manage your agents by performing the following tasks:

    -   Relocate agents from one territory to another for a particular duration.
    -   Facilitate precise destination territory selection, which ensures that each agent is placed in the most preferable location.
    -   Match resource availability with task requirements through improved schedule planning, which optimizes task execution and efficiently addresses unscheduled work.
    -   Minimize manual overhead and avoid manual tracking processes by simplifying the handling of temporary resource relocations.
-   **[Optimize agent operations with flexible work locations](https://servicenow-staging.fluidtopics.net/access?context=change-agent-start-end-location&family=xanadu&ft:locale=en-US)**

Add flexible work locations for agents by performing the following tasks:

    -   Define different start-of-day and end-of-day locations for agents to start their day at one location and end at another location, providing flexibility in their operations.
    -   Offer additional flexibility by implementing exceptions to override default behaviors during specific periods.
    -   Improve scheduling accuracy by calculating travel times based on the agent's start and end locations.
-   **[Sales opportunity in Now Mobile Agent app](https://servicenow-staging.fluidtopics.net/access?context=create-opportunity&family=xanadu&ft:locale=en-US)**

Enable field service technicians to perform the following the Now Mobile Agent application.

    -   Create sales opportunities directly from customer locations during field service visits.
    -   Access data to view, search, and filter sales opportunities.
-   **[Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=xanadu&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View multiple time zones to see agents who are available for work order tasks across multiple locations.
    -   Receive intelligent guidance about all possible scheduling options for unscheduled tasks. Rank scheduling options based on agent-to-task match percentage, distance, and more.
    -   Hide off-shift agents so dispatchers can focus on who’s available and ready for tasks at that moment.
-   **[Beans.ai map integration for bundled tasks](https://servicenow-staging.fluidtopics.net/access?context=c_AutoRouting&family=xanadu&ft:locale=en-US)**

Optimize routes for bundled tasks with beans.ai.

-   **[Appointment booking enhancements](https://servicenow-staging.fluidtopics.net/access?context=appointment-booking-administer&family=xanadu&ft:locale=en-US)**

Use appointment booking enhanced configurations to perform the following tasks:

    -   Book appointments for work order tasks.
    -   Enable the system to calculate or skip lead time when rescheduling appointments, depending on the selected configuration.
    -   Consider holidays when calculating lead time for appointments.
-   **[Field Service Marketplace enhancements](https://servicenow-staging.fluidtopics.net/access?context=fsm-marketplace&family=xanadu&ft:locale=en-US)**
    -   Automate the process of pushing tasks to the marketplace, automatically creating marketplace requests, and listing eligible contractors as determined by your specified criteria.
    -   Set up task filters to identify the work order tasks that qualify for the marketplace.
    -   Incrementally push marketplace requests to eligible contractors based on their ranking using the **Progressive push** check box.
    -   Evaluate contractor responses and automatically assign tasks to the lowest-cost contractor using the **Response evaluation flow** field.
-   **[Field Service Quality Management](https://servicenow-staging.fluidtopics.net/access?context=quality-management-fsm&family=xanadu&ft:locale=en-US)**

Use Field Service Quality Management to do the following tasks:

    -   Review the quality and data from work order tasks before completion.
    -   Address work orders that have been reviewed and sent back for more information.
    -   Provide feedback to technicians and communicate as needed during the review process.
-   **[Workforce enhancements](https://servicenow-staging.fluidtopics.net/access?context=using-manager-workforce&family=xanadu&ft:locale=en-US)**

Use Workforce enhanced configurations to perform the following tasks:

    -   Extend access across all personas, allowing every user regardless of their role to view their own calendars.
    -   Configure settings to enable group and territory calendar visibility, authoring agents to view the list and calendars of members in their group or within their territory when Workforce Optimization for Field Service isn't enabled.
    -   Enable agents to create personal events for themselves.
-   **[Multiple Work Configurations](https://servicenow-staging.fluidtopics.net/access?context=configuring-work-configs&family=xanadu&ft:locale=en-US)**

Create configurations for multiple work types, such as Installation, Repair, Break fix, and Maintenance.

    -   Set up work configurations for different work types ensuring that relevant work types and flows appear for specified business units or departments.
    -   Create Service Management configurations \(SM Configs\) to support multiple workflows.
    -   Extend the work order task table to account for different work types.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   View the Field Service agent’s real-time location and completed daily route.
    -   Use a condition builder to filter relevant resources. You can also extend existing tables to filter custom fields.
    -   Use advanced filters with hierarchical structures to filter territories.
    -   View task scheduling conflict messages in the Dispatcher Workspace to improve visibility and facilitate resolutions for dispatchers.
-   **[Field Service Agent Efficiency](https://servicenow-staging.fluidtopics.net/access?context=configuring-agent-efficiency&family=yokohama&ft:locale=en-US)**

Use Agent Efficiency to perform the following tasks:

    -   Define the agent efficiency criteria to calculate the Agent Efficiency for a task.
    -   Calculate the estimated work duration for a work order task more accurately based on the Agent Efficiency feature.
    -   Enhance manual task assignment and dynamic scheduling for a task by leveraging Agent Efficiency.
    -   Optimize Intelligent Task Recommendation by incorporating Agent Efficiency values so that dispatchers can assign tasks more effectively.
-   **[Appointment Booking](https://servicenow-staging.fluidtopics.net/access?context=appointment-booking-administer&family=yokohama&ft:locale=en-US)**

Use Appointment Booking to perform the following tasks:

    -   Replicate the application and service-based configurations across instances.
    -   Grade the appointment booking slots by recommended or available slots to ensure optimal scheduling.
    -   Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.
-   **[Task dependencies](https://servicenow-staging.fluidtopics.net/access?context=t_SetAnUpstreamTask&family=yokohama&ft:locale=en-US)**

Use task dependencies to perform the following tasks:

    -   Enable administrators and dispatchers to define advanced task dependencies, such as start together or start after start, so that you can ensure that tasks are executed in the right order.
    -   Enable dispatchers to create task dependencies within or between work orders.
-   **[Schedule Optimization](https://servicenow-staging.fluidtopics.net/access?context=schedule-optimization-engine&family=yokohama&ft:locale=en-US)**

Use Schedule Optimization to perform the following tasks:

    -   Enable dispatchers to optimize resource assignments that are based on the dependency relationship between tasks.
    -   Generate more accurate scheduling and assist your field technicians in navigating traffic conditions more effectively by configuring Schedule Optimization. You can consider time-of-day and set up intraday scheduling to leverage real-time traffic data when certain conditions are met.
    -   Use new optimization features, such as **Maximize consecutive collocated task assignments** and **Minimize task start times**, when you're creating a policy.
    -   Provide greater control over task distribution by enabling a new drip feed property, **Number of tasks**, to enhance your scheduling capabilities.
    -   Expect more reliable and efficient task scheduling due to resolved conflicts between the various scheduling engines.
    -   View the task scheduling conflict messages on the task, user, and group records when optimization is in progress.
-   **[Capacity and Reservations Management](https://servicenow-staging.fluidtopics.net/access?context=capacity-management&family=yokohama&ft:locale=en-US)**

Use Capacity and Reservations Management to perform the following tasks:

    -   Leverage the capacity console to efficiently manage resource allocation across territories and demand channels so that you can enable your teams to analyze field technician performance and make data-driven decisions.
    -   Set flexible reservation rules to define the minimum and maximum resource allocations so that you can enable dynamic adjustments to capacity based on shifting demands.
    -   Create recurring capacity assignments for specific days of the week for long-term capacity planning and management.
    -   Enable multiple overrides for the same date range to address demand fluctuations so that you can manage exceptions with more precision and flexibility.
-   **[Scheduling Health dashboard](https://servicenow-staging.fluidtopics.net/access?context=scheduling-health-dashboard&family=yokohama&ft:locale=en-US)**

Use the Scheduling Health dashboard to view these additional Schedule Optimization metrics:

    -   Tasks without skills
    -   Technicians without skills
    -   Tasks without parts
    -   Technicians without parts
-   **[Business location-based work management](https://servicenow-staging.fluidtopics.net/access?context=industry-products-integration&family=yokohama&ft:locale=en-US)**

Enable your staff across various industries to efficiently manage work orders. Your employees can resolve tasks that are specific to their assigned location, while your managers can oversee the tasks across their assigned locations. You can reinforce your security by ensuring that your staff can only access the work orders that are related to their designated locations.

-   **[Managing agents and tasks from Workforce](https://servicenow-staging.fluidtopics.net/access?context=using-manager-workforce&family=yokohama&ft:locale=en-US)**

Use Workforce to perform the following tasks:

    -   Enable additional users to use Workforce by adding additional managers to assignment groups.
    -   Enable managers to view the event management tab when Workforce Optimization for Field Service is active.
-   **[Smart Assessment for Field Service Questionnaire](https://servicenow-staging.fluidtopics.net/access?context=configuring-smart-assessment-questionnaire&family=yokohama&ft:locale=en-US)**

Use Smart Assessment templates to perform the following tasks:

    -   Migrate from a survey-based questionnaire to Smart Assessment based questionnaires.
    -   Create work order questionnaires.
    -   Set up detailed instructions that include rich text and images.
    -   Configure conditional questions based on responses of all other types of questions and across sections.
    -   Allow additional comments or attachments on a question's response.
    -   Improve the work order questionnaire in the Mobile Agent® application by implementing a paginated layout, providing instructions with questions, and offering in-line choices.
-   **[Planned Work Management](https://servicenow-staging.fluidtopics.net/access?context=migrate-maint-plans-pwm&family=yokohama&ft:locale=en-US)**

Seamlessly migrate monthly and annual plans from Planned Maintenance to Planned Work Management.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Using Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=zurich&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   Use the advanced resource filter to sort contractors and equipment.
    -   Add agents to Dispatcher Workspace to see their schedules, or assign them tasks if you manage the assignment group or territory they're a part of. This action can be done without loading the entire assignment group or territory that the agent is a member of.
    -   Set up the calendar to use multiple time zones at once. For more information, see [Show multiple time zones](https://servicenow-staging.fluidtopics.net/access?context=use-stacked-time-zones&family=zurich&ft:locale=en-US).
    -   Navigate from a work order task to a related list of smart assessments that are associated with that work order.
-   **[Assigning WOTs manually](https://servicenow-staging.fluidtopics.net/access?context=c_DispatchWorkOrderTasks&family=zurich&ft:locale=en-US)**

Use the records page to perform the following tasks that was limited to Dispatcher Workspace before:

    -   Flag a work order task.
    -   Use assignment assistance.
-   **[Schedule Optimization](https://servicenow-staging.fluidtopics.net/access?context=schedule-optimization-engine&family=zurich&ft:locale=en-US)**

Use Schedule Optimization to do the following:

    -   Initiate immediate optimization to adjust schedules and tasks when an in-day event occurs, like a new priority 1 task, a canceled task, an agent taking PTO, or an agent running late.
    -   Assign the best agent for a work order task based on agent efficiency, which helps schedule and assign tasks more appropriately, using Field Service Agent Efficiency.
    -   Define work, travel, and overtime penalty values for each agent so the optimization engine can either schedule a nearby agent with a higher penalty or a distant agent with a lower penalty.

    -   Improve task scheduling by assigning dependent tasks to a single technician within the same shift.
-   **[Workforce](https://servicenow-staging.fluidtopics.net/access?context=configuring-workforce&family=zurich&ft:locale=en-US)**

Enable managers to show or hide work order tasks from the **Calendars** tab in Workforce. When Workforce Optimization for Field Service is enabled, these tasks can also be viewed in Hybrid and Map views.

-   **[Field Service Scheduling](https://servicenow-staging.fluidtopics.net/access?context=setting-up-scheduling-methods&family=zurich&ft:locale=en-US)**

Manage resource attributes for any duration, whether a single day or multiple days.

-   **[Appointment Booking](https://servicenow-staging.fluidtopics.net/access?context=appointment-booking-administer&family=zurich&ft:locale=en-US)**

Use Appointment Booking to do the following:

    -   Enable better control over task sequencing using new dependency types, such as 'Finish to Start - Same Day' and 'Finish Together' with lag options, integrated with appointment booking for more precise scheduling. Enhance operational insight for all roles through improved visualizations including dependency trees, conflict alerts, and task indicators, which support dispatcher decisions and technician execution.
    -   Optimize appointment recommendations by allowing radius configuration at the territory level, tailored to diverse areas, such as urban versus rural. This capability includes an extension point for customers to implement custom radius logic with default instance-level values if no specific configuration is set.
    -   Enhance appointment recommendations by allowing grading against user-defined similar services rather than identical ones, resulting in more versatile scheduling options. This feature includes an extension point for customers to specify which services they consider similar, and the system defaults to same-catalog matching if no custom configuration is provided.
    -   Increase scheduling flexibility with new features to support slot overlap and overrides. This capability enables territory-based customization of appointment windows, default schedules, and specific slot-level overrides, giving more control over availability.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Field Service Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Migration of Field Service Management Core UI dashboards to Next Experience Dashboards**

The following Next Experience Field Service Management dashboards provide a more efficient streamlined way for you to work:

    -   Field Service Management overview
    -   Field Service Contractor
    -   Field Service Planned Maintenance
    -   Field Service Performance Analytics

</td></tr><tr><td>

Xanadu

</td><td>

-   **Capacity and Reservations Management**

Capacity and Reservations Management data model has been changed to accommodate the agent's start and end location.

-   **[Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=xanadu&ft:locale=en-US)**

Dispatcher Workspace and Workforce Optimization for Field Service support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown) section that follows.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[SLAs in Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

The SLAs breached query on the Dispatcher Dashboard in Dispatcher Workspace has been updated to look at the SLAs that are associated with the work order tasks only instead of the work orders and work order tasks. The SLA breached counter on the task cards is also static, instead of real time. For more information on changing the SLA timer on task cards, see the Enable the **SLA timer on work order task cards** property on [Configure settings for Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=configure-workspce-settings&family=yokohama&ft:locale=en-US).

-   **[Assignment groups and territories in Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-dispatcher-workspace&family=yokohama&ft:locale=en-US)**

You must save the default assignment groups or territories in Dispatcher Workspace to load when you open Dispatcher Workspace. If you don’t have the defaults saved, then you must select the assignment groups or territories to appear every time you open Dispatcher Workspace. This change is made to improve the performance of Dispatcher Workspace. For more information on saving the default assignment groups, see the Groups section on the **General** tab on [Enable Dispatcher Workspace settings](https://servicenow-staging.fluidtopics.net/access?context=dispatcher-wrkspc-settings&family=yokohama&ft:locale=en-US). For information on saving default territories, see [Select Territories in Dispatcher Workspace](https://servicenow-staging.fluidtopics.net/access?context=select-territory-dispatch&family=yokohama&ft:locale=en-US). Administrators can disable this by setting the **sn\_fsm\_disp\_wrkspc.enableEmptyState** system property to false.

-   **[Work order questionnaire](https://servicenow-staging.fluidtopics.net/access?context=complete-questionnaire-mobile-app&family=yokohama&ft:locale=en-US)**

Availability of inline choices for a question and the ability to add additional information for a question when completing a work order questionnaire through the Now Mobile Agent application.

-   **Role to access opportunities**

The Opportunity Writer sn\_opty\_mgmt\_core.opportunity\_writer role has been replaced with the Opportunity Contributor sn\_opty\_mgmt\_core.opportunity\_contributor role. Field service technicians can use the new Opportunity Contributor\[sn\_opty\_mgmt\_core.opportunity\_contributor role to create and view opportunities.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Capacity and Reservations Management](https://servicenow-staging.fluidtopics.net/access?context=configuring-capacity-management&family=zurich&ft:locale=en-US)**

Use the aggregated schedules of all agents of a territory to allocate resources until a specified cut-off date, after which predicted capacity can be used for bookings. This feature optimizes resource utilization and capacity management for a territory, which helps ensure that business services remain available without overburdening resources.

-   **[Google Maps APIs for  Field Service  capabilities](https://servicenow-staging.fluidtopics.net/access?context=google-maps-api-keys&family=zurich&ft:locale=en-US)**

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you create a Google API key after March 2025, you must upgrade to a supported ServiceNow release version to verify compatibility.

-   **[Smart Assessment for Field Service](https://servicenow-staging.fluidtopics.net/access?context=configuring-smart-assessment-questionnaire&family=zurich&ft:locale=en-US)**

Use Smart Assessment for Field Service to do the following:

    -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
    -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
    -   View completed questionnaires in the workspace.
    -   Create follow-up work order tasks from a work order questionnaire based on the responses.
    -   Allow users to retry or replace an attachment if the upload is unsuccessful.
-   **[Field Service Scheduling](https://servicenow-staging.fluidtopics.net/access?context=setting-up-scheduling-methods&family=zurich&ft:locale=en-US)**

Migrates data from the Work Parameter table to the Resource Schedule Attribute table for each technician, confirming that work parameters align with the new schedule attributes.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Field Service Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

The Field Service dashboard is removed from the Emergency Exposure Management application.

</td></tr><tr><td>

Yokohama

</td><td>

The approval for new requests workflow was removed from the Field Service Management Business Process configuration. Existing customers that use this workflow are unaffected. New customers can use ServiceNow® Workflow Studio to build the approval for the new requests workflow. For more information on Workflow Studio, see [Flow Designer](https://servicenow-staging.fluidtopics.net/access?context=flow-designer&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Field Service Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Xanadu

</td><td>

-   Starting with the Xanadu release, FSM Agent Classic Workspace plugin \(com.snc.agent\_workspace.fsm\) is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

-   Starting with the Yokohama release, Approval Workflow for FSM is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Zurich

</td><td>

-   Non-collapsed mode is being deprecated and removed from Dispatcher Workspace. Dispatchers must use collapsed mode to see available resources in Dispatcher Workspace.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being deprecated. It will no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Field Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is available with activation of the Field Service Management plugin \(field\_service\_management\). For details, see [Activate Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateFieldServiceManagement&family=washingtondc&ft:locale=en-US).

 Additional Field Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=field-service-additional-plugins&family=washingtondc&ft:locale=en-US).

 Field Service Marketplace is available with activation of the Field Service Marketplace plugin \(com.snc.fsm\_marketplace\). For details, see [Activate Field Service Marketplace](https://servicenow-staging.fluidtopics.net/access?context=activate-contractor-marketplace&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is available with activation of the Field Service Management plugin \(field\_service\_management\). For details, see [Activate Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateFieldServiceManagement&family=xanadu&ft:locale=en-US).

 Additional Field Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=field-service-additional-plugins&family=xanadu&ft:locale=en-US).

 Enable field service technicians to initiate and monitor sales opportunities directly through the Now Mobile Agent application by activating Technician driven sales with the Field Service \(com.snc.fsm\_technician\_sales\) plugin.

</td></tr><tr><td>

Yokohama

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is active by default.

 Leverage advanced features of Appointment Booking, such as the appointment slot recommendation, by activating the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin.

 Define the task dependencies for a work order task and schedule tasks based on the dependency by activating the Field Service Task Dependencies \(com.snc.fsm\_task\_dependency\) plugin.

 Integrate agent efficiency metrics with Field Service Management to define and use the efficiency of agents to estimate the work duration for tasks by activating the FSM Agent Efficiency \(com.snc.fsm\_agent\_efficiency​\) plugin.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Field Service Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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
This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=xanadu&ft:locale=en-US) for details.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Field Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Identify and pinpoint the work order locations on your structured linear assets for accurate field service operations.
-   Streamline your inventory management and ensure that you have timely access to the right parts by viewing the descriptions, models, and related criteria in similar work orders.
-   Explore the Field Service marketplace to help you streamline the work for your contractors and make decisions based on time and costs regarding the task assignments for your contractors.
-   Enable dispatchers to run Schedule Optimization on demand throughout the day as scheduling conditions change.

 See [Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=fsm-application-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Move agents between territories, optimize scheduling, and minimize manual tracking while agents execute tasks.
-   Create and view sales opportunities during field service visits using the Now Mobile Agent application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=fsm-application-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Define configurable rules that you can use to derive recommendation scores and optimize your appointment booking slots.
-   Create advanced dependency relationships among tasks to enhance scheduling accuracy.
-   Optimize your task assignments by using dependencies that align with the overall objectives and constraints of your resource allocation.
-   Streamline your capacity and resource management by using enhanced visualization in the Capacity Console.
-   Calculate the work duration for a work order task more accurately by using the Agent Efficiency feature.

 See [Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=fsm-application-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use the aggregated agent schedule to optimize the allocation of resources for a territory up to the specified cut-off date.
-   Flag a task or use assignment assistance directly from the Work Order Task page to streamline task management.
-   Configure Schedule Optimization to instantly adjust technician schedules in response to real-time events, like new priority 1 tasks, task cancellations, paid time off requests, or delays.

 See [Field Service Management](https://servicenow-staging.fluidtopics.net/access?context=fsm-application-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

