---
title: Field Service Management release notes
description: The ServiceNow Field Service Management application unites AI, data, and workflows on a single enterprise-grade platform to revolutionize field operations in completion of any job the first time, every time. Field Service Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Field Service Management release notes

The ServiceNow® Field Service Management application unites AI, data, and workflows on a single enterprise-grade platform to revolutionize field operations in completion of any job the first time, every time. Field Service Management was enhanced and updated in the Zurich release.

## Field Service Management highlights for the Zurich release

-   Use the aggregated agent schedule to optimize the allocation of resources for a territory up to the specified cut-off date.
-   Flag a task or use assignment assistance directly from the Work Order Task page to streamline task management.
-   Configure Schedule Optimization to instantly adjust technician schedules in response to real-time events, like new priority 1 tasks, task cancellations, paid time off requests, or delays.

See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more information.

## Important information for upgrading Field Service Management to Zurich

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.

## New in the Zurich release

-   **[Using Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use Dispatcher Workspace to perform the following tasks:

    -   Use the advanced resource filter to sort contractors and equipment.
    -   Add agents to Dispatcher Workspace to see their schedules, or assign them tasks if you manage the assignment group or territory they're a part of. This action can be done without loading the entire assignment group or territory that the agent is a member of.
    -   Set up the calendar to use multiple time zones at once. For more information, see [Show multiple time zones at once in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=use-stacked-time-zones&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).
    -   Navigate from a work order task to a related list of smart assessments that are associated with that work order.
-   **[Assigning work order tasks to agents manually](https://www.servicenow.com/docs/access?context=c_DispatchWorkOrderTasks&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use the records page to perform the following tasks that was limited to Dispatcher Workspace before:

    -   Flag a work order task.
    -   Use assignment assistance.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use Schedule Optimization to do the following:

    -   Initiate immediate optimization to adjust schedules and tasks when an in-day event occurs, like a new priority 1 task, a canceled task, an agent taking PTO, or an agent running late.
    -   Assign the best agent for a work order task based on agent efficiency, which helps schedule and assign tasks more appropriately, using Field Service Agent Efficiency.
    -   Define work, travel, and overtime penalty values for each agent so the optimization engine can either schedule a nearby agent with a higher penalty or a distant agent with a lower penalty.

    -   Improve task scheduling by assigning dependent tasks to a single technician within the same shift.
-   **[Workforce](https://www.servicenow.com/docs/access?context=configuring-workforce&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Enable managers to show or hide work order tasks from the **Calendars** tab in Workforce. When Workforce Optimization for Field Service is enabled, these tasks can also be viewed in Hybrid and Map views.

-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Manage resource attributes for any duration, whether a single day or multiple days.

-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use Appointment Booking to do the following:

    -   Enable better control over task sequencing using new dependency types, such as 'Finish to Start - Same Day' and 'Finish Together' with lag options, integrated with appointment booking for more precise scheduling. Enhance operational insight for all roles through improved visualizations including dependency trees, conflict alerts, and task indicators, which support dispatcher decisions and technician execution.
    -   Optimize appointment recommendations by allowing radius configuration at the territory level, tailored to diverse areas, such as urban versus rural. This capability includes an extension point for customers to implement custom radius logic with default instance-level values if no specific configuration is set.
    -   Enhance appointment recommendations by allowing grading against user-defined similar services rather than identical ones, resulting in more versatile scheduling options. This feature includes an extension point for customers to specify which services they consider similar, and the system defaults to same-catalog matching if no custom configuration is provided.
    -   Increase scheduling flexibility with new features to support slot overlap and overrides. This capability enables territory-based customization of appointment windows, default schedules, and specific slot-level overrides, giving more control over availability.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**
    -   The Resource Schedule Attribute related list and form have been added to agent profiles.
    -   The Aggregated Agent Schedule has been added to Capacity by list in the Capacity definition form.
    -   The Agent Schedule Attribute Plan table and form have been renamed to Resource Schedule Attribute.

## Changed in this release

-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use the aggregated schedules of all agents of a territory to allocate resources until a specified cut-off date, after which predicted capacity can be used for bookings. This feature optimizes resource utilization and capacity management for a territory, which helps ensure that business services remain available without overburdening resources.

-   **[Google Maps APIs for  Field Service  capabilities](https://www.servicenow.com/docs/access?context=google-maps-api-keys&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you create a Google API key after March 2025, you must upgrade to a supported ServiceNow release version to verify compatibility.

-   **[Smart Assessment for Field Service](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use Smart Assessment for Field Service to do the following:

    -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
    -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
    -   View completed questionnaires in the workspace.
    -   Create follow-up work order tasks from a work order questionnaire based on the responses.
    -   Allow users to retry or replace an attachment if the upload is unsuccessful.
-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Migrates data from the Work Parameter table to the Resource Schedule Attribute table for each technician, confirming that work parameters align with the new schedule attributes.


## Deprecations

-   Non-collapsed mode is being deprecated and removed from Dispatcher Workspace. Dispatchers must use collapsed mode to see available resources in Dispatcher Workspace.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being deprecated. It will no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Field Service Management is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **Financial Management**

    Field Service Management integrates with the ServiceNow® Financial Management application to allocate, track, and report expenses in your organization.

    **Note:** The Financial Management for CSM plugin \(com.snc.financial\_management\_for\_csm\) is no longer available for direct activation. You can request this plugin through Now Support Customer Service.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-integration&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The Customer Service Management \(CSM\) with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and ServiceNow® Customer Service Management \(CSM\) applications to enable you to view account and contact information on work orders and work order tasks in the Field Service Management application.

-   **[Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Field Service Management integrates with the ServiceNow® Service Portfolio Management application to enable you to create work orders directly from project tasks.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service-specific implementations that provide tier-1 agents with the tools needed to respond to customers and resolve cases.


-   **[Now Assist for FSM release notes](now-assist-for-fsm-rn.md)**  
The ServiceNow® Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Zurich release.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

