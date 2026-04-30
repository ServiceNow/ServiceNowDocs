---
title: Field Service Management release notes
description: The ServiceNow Field Service Management application automates processes, enhances communication, and transforms field service delivery with AI-powered workflows to resolve customer needs efficiently, transparently, and proactively. Field Service Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
---

# Field Service Management release notes

The ServiceNow® Field Service Management application automates processes, enhances communication, and transforms field service delivery with AI-powered workflows to resolve customer needs efficiently, transparently, and proactively. Field Service Management was enhanced and updated in the Yokohama release.

## Field Service Management highlights for the Yokohama release

-   Define configurable rules that you can use to derive recommendation scores and optimize your appointment booking slots.
-   Create advanced dependency relationships among tasks to enhance scheduling accuracy.
-   Optimize your task assignments by using dependencies that align with the overall objectives and constraints of your resource allocation.
-   Streamline your capacity and resource management by using enhanced visualization in the Capacity Console.
-   Calculate the work duration for a work order task more accurately by using the Agent Efficiency feature.

See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) for more information.

## Important information for upgrading Field Service Management to Yokohama

-   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
-   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

## New in the Yokohama release

-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Dispatcher Workspace to perform the following tasks:

    -   View the Field Service agent’s real-time location and completed daily route.
    -   Use a condition builder to filter relevant resources. You can also extend existing tables to filter custom fields.
    -   Use advanced filters with hierarchical structures to filter territories.
    -   View task scheduling conflict messages in the Dispatcher Workspace to improve visibility and facilitate resolutions for dispatchers.
-   **[Field Service Agent Efficiency](https://www.servicenow.com/docs/access?context=configuring-agent-efficiency&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Agent Efficiency to perform the following tasks:

    -   Define the agent efficiency criteria to calculate the Agent Efficiency for a task.
    -   Calculate the estimated work duration for a work order task more accurately based on the Agent Efficiency feature.
    -   Enhance manual task assignment and dynamic scheduling for a task by leveraging Agent Efficiency.
    -   Optimize Intelligent Task Recommendation by incorporating Agent Efficiency values so that dispatchers can assign tasks more effectively.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Appointment Booking to perform the following tasks:

    -   Replicate the application and service-based configurations across instances.
    -   Grade the appointment booking slots by recommended or available slots to ensure optimal scheduling.
    -   Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.
-   **[Task dependencies](https://www.servicenow.com/docs/access?context=t_SetAnUpstreamTask&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use task dependencies to perform the following tasks:

    -   Enable administrators and dispatchers to define advanced task dependencies, such as start together or start after start, so that you can ensure that tasks are executed in the right order.
    -   Enable dispatchers to create task dependencies within or between work orders.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Schedule Optimization to perform the following tasks:

    -   Enable dispatchers to optimize resource assignments that are based on the dependency relationship between tasks.
    -   Generate more accurate scheduling and assist your field technicians in navigating traffic conditions more effectively by configuring Schedule Optimization. You can consider time-of-day and set up intraday scheduling to leverage real-time traffic data when certain conditions are met.
    -   Use new optimization features, such as **Maximize consecutive collocated task assignments** and **Minimize task start times**, when you're creating a policy.
    -   Provide greater control over task distribution by enabling a new drip feed property, **Number of tasks**, to enhance your scheduling capabilities.
    -   Expect more reliable and efficient task scheduling due to resolved conflicts between the various scheduling engines.
    -   View the task scheduling conflict messages on the task, user, and group records when optimization is in progress.
-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=capacity-management&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Capacity and Reservations Management to perform the following tasks:

    -   Leverage the capacity console to efficiently manage resource allocation across territories and demand channels so that you can enable your teams to analyze field technician performance and make data-driven decisions.
    -   Set flexible reservation rules to define the minimum and maximum resource allocations so that you can enable dynamic adjustments to capacity based on shifting demands.
    -   Create recurring capacity assignments for specific days of the week for long-term capacity planning and management.
    -   Enable multiple overrides for the same date range to address demand fluctuations so that you can manage exceptions with more precision and flexibility.
-   **[Scheduling Health dashboard](https://www.servicenow.com/docs/access?context=scheduling-health-dashboard&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use the Scheduling Health dashboard to view these additional Schedule Optimization metrics:

    -   Tasks without skills
    -   Technicians without skills
    -   Tasks without parts
    -   Technicians without parts
-   **[Business location-based work management](https://www.servicenow.com/docs/access?context=industry-products-integration&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Enable your staff across various industries to efficiently manage work orders. Your employees can resolve tasks that are specific to their assigned location, while your managers can oversee the tasks across their assigned locations. You can reinforce your security by ensuring that your staff can only access the work orders that are related to their designated locations.

-   **[Managing agents and tasks from Workforce](https://www.servicenow.com/docs/access?context=using-manager-workforce&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Workforce to perform the following tasks:

    -   Enable additional users to use Workforce by adding additional managers to assignment groups.
    -   Enable managers to view the event management tab when Workforce Optimization for Field Service is active.
-   **[Smart Assessment for Field Service Questionnaire](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Use Smart Assessment templates to perform the following tasks:

    -   Migrate from a survey-based questionnaire to Smart Assessment based questionnaires.
    -   Create work order questionnaires.
    -   Set up detailed instructions that include rich text and images.
    -   Configure conditional questions based on responses of all other types of questions and across sections.
    -   Allow additional comments or attachments on a question's response.
    -   Improve the work order questionnaire in the Mobile Agent® application by implementing a paginated layout, providing instructions with questions, and offering in-line choices.
-   **Planned Work Management**

    Seamlessly migrate monthly and annual plans from Planned Maintenance to Planned Work Management.


## UI changes

-   **[Field Service Agent Efficiency](https://www.servicenow.com/docs/access?context=configuring-agent-efficiency&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**
    -   Configure and define the Agent Efficiency criteria.
    -   Add an Agent Efficiency value for an agent.
    -   The **Planned work duration** and **Agent efficiency criteria** fields were added.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    An optional seismic appointment booking Calendar with slot recommendation is available for Appointment Booking.

-   **[Task Dependency](https://www.servicenow.com/docs/access?context=t_SetAnUpstreamTask&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**
    -   Upstream task is renamed as Predecessor task.
    -   Downstream task is renamed as Successor task.
    -   New fields were added to define advanced task dependencies.
-   **[Work order questionnaire](https://www.servicenow.com/docs/access?context=complete-questionnaire-mobile-app&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**
    -   You have in-line choices for a question when completing a work order questionnaire through the Now Mobile Agent application.
    -   You can add additional information to a question when completing a work order questionnaire through the Now Mobile Agent application.
-   **[Smart Assessment for Field Service Questionnaire](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Added a toggle to enable Smart Assessments for a work order questionnaire.


## Changed in this release

-   **[SLAs in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    The SLAs breached query on the Dispatcher Dashboard in Dispatcher Workspace has been updated to look at the SLAs that are associated with the work order tasks only instead of the work orders and work order tasks. The SLA breached counter on the task cards is also static, instead of real time. For more information on changing the SLA timer on task cards, see the Enable the **SLA timer on work order task cards** property on [Configure settings for Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configure-workspce-settings&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US).

-   **[Assignment groups and territories in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    You must save the default assignment groups or territories in Dispatcher Workspace to load when you open Dispatcher Workspace. If you don’t have the defaults saved, then you must select the assignment groups or territories to appear every time you open Dispatcher Workspace. This change is made to improve the performance of Dispatcher Workspace. For more information on saving the default assignment groups, see the Groups section on the **General** tab on [Enable Dispatcher Workspace settings](https://www.servicenow.com/docs/access?context=dispatcher-wrkspc-settings&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US). For information on saving default territories, see [Select Territories in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=select-territory-dispatch&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US). Administrators can disable this by setting the **sn\_fsm\_disp\_wrkspc.enableEmptyState** system property to false.

-   **[Work order questionnaire](https://www.servicenow.com/docs/access?context=complete-questionnaire-mobile-app&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Availability of inline choices for a question and the ability to add additional information for a question when completing a work order questionnaire through the Now Mobile Agent application.

-   **Role to access opportunities**

    The Opportunity Writer sn\_opty\_mgmt\_core.opportunity\_writer role has been replaced with the Opportunity Contributor sn\_opty\_mgmt\_core.opportunity\_contributor role. Field service technicians can use the new Opportunity Contributor\[sn\_opty\_mgmt\_core.opportunity\_contributor role to create and view opportunities.

-   **Google Maps APIs for Field Service Capabilities**

    Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

    Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

    You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

    If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

    For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


## Removed in this release

The approval for new requests workflow was removed from the Field Service Management Business Process configuration. Existing customers that use this workflow are unaffected. New customers can use ServiceNow® Workflow Studio to build the approval for the new requests workflow. For more information on Workflow Studio, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Deprecations

-   Starting with the Yokohama release, Approval Workflow for FSM is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Field Service Management is a ServiceNow AI Platform feature that is active by default.

Leverage advanced features of Appointment Booking, such as the appointment slot recommendation, by activating the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin.

Define the task dependencies for a work order task and schedule tasks based on the dependency by activating the Field Service Task Dependencies \(com.snc.fsm\_task\_dependency\) plugin.

Integrate agent efficiency metrics with Field Service Management to define and use the efficiency of agents to estimate the work duration for tasks by activating the FSM Agent Efficiency \(com.snc.fsm\_agent\_efficiency​\) plugin.

## Related ServiceNow applications and features

-   **Financial Management**

    Field Service Management integrates with the ServiceNow® Financial Management application to allocate, track, and report expenses in your organization.

    **Note:** The Financial Management for CSM plugin \(com.snc.financial\_management\_for\_csm\) is no longer available for direct activation. You can request this plugin through Now Support Customer Service.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-integration&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and ServiceNow® Customer Service Management \(CSM\) applications to enable you to view account and contact information on work orders and work order tasks in the Field Service Management application.

-   **[Service Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Field Service Management integrates with the ServiceNow® Service Portfolio Management application to enable you to create work orders directly from project tasks.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service-specific implementations that provide tier 1 agents with the tools needed to respond to customers and to resolve cases.


-   **[Now Assist for Field Service Management \(FSM\) release notes](now-assist-for-fsm-rn.md)**  
The ServiceNow® Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Yokohama release.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

