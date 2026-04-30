---
title: Field Service Management release notes
description: The ServiceNow Field Service Management application enables your organization to manage location-based work more efficiently and safely. Field Service Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
---

# Field Service Management release notes

The ServiceNow® Field Service Management application enables your organization to manage location-based work more efficiently and safely. Field Service Management was enhanced and updated in the Xanadu release.

## Field Service Management highlights for the Xanadu release

-   Move agents between territories, optimize scheduling, and minimize manual tracking while agents execute tasks.
-   Create and view sales opportunities during field service visits using the Now Mobile Agent application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US) for more information.

## Important information for upgrading Field Service Management to Xanadu

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Xanadu Patch 9 version or higher to ensure compatibility.

## New in the Xanadu release

-   **[Schedule Optimization features](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use Schedule Optimization to do the following tasks:

    -   Use new objectives such as **Maximize SLA compliance buffers**, **Minimize task time penalties**, and **Maximize preferred agent assignments** when you're creating a policy.
    -   Define start-of-day and end-of-day location for territory users, improving scheduling accuracy by calculating travel times based on actual agent locations.
    -   Keep similar tasks together by scheduling pre-made bundles.
    -   Reduce the beans.ai travel estimate processing time with asynchronous processing.
    -   Access the Field Service Management Scheduling Health dashboard to view task metrics, technician metrics, and optimization configuration details.
    -   Enable dispatchers to influence the behavior of schedule optimization by allowing dispatchers to edit select fields on a work order task. Dispatchers can override work order task parameters, assign tasks based on technician preferences, and allow overtime.
-   **[Field Service Territory Capacity Analytics dashboard](https://www.servicenow.com/docs/access?context=capacity-dashboard&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use the Field Service Territory Capacity Analytics dashboard for the following tasks:

    -   Use interactive charts and graphs to track capacity trends, including overall demand versus allocated capacity and capacity usage over time.
    -   Perform capacity gap analysis with a customizable pivot table view, which enables you to explore data by territory and demand channel.
    -   Apply filters to view specific data based on your setup, which enables targeted analysis and informed decision-making.
-   **[Agent relocation](https://www.servicenow.com/docs/access?context=relocate-agents-territories&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Manage your agents by performing the following tasks:

    -   Relocate agents from one territory to another for a particular duration.
    -   Facilitate precise destination territory selection, which ensures that each agent is placed in the most preferable location.
    -   Match resource availability with task requirements through improved schedule planning, which optimizes task execution and efficiently addresses unscheduled work.
    -   Minimize manual overhead and avoid manual tracking processes by simplifying the handling of temporary resource relocations.
-   **[Optimize agent operations with flexible work locations](https://www.servicenow.com/docs/access?context=change-agent-start-end-location&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Add flexible work locations for agents by performing the following tasks:

    -   Define different start-of-day and end-of-day locations for agents to start their day at one location and end at another location, providing flexibility in their operations.
    -   Offer additional flexibility by implementing exceptions to override default behaviors during specific periods.
    -   Improve scheduling accuracy by calculating travel times based on the agent's start and end locations.
-   **[Sales opportunity in Now Mobile Agent app](https://www.servicenow.com/docs/access?context=create-opportunity&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Enable field service technicians to perform the following the Now Mobile Agent application.

    -   Create sales opportunities directly from customer locations during field service visits.
    -   Access data to view, search, and filter sales opportunities.
-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use Dispatcher Workspace to perform the following tasks:

    -   View multiple time zones to see agents who are available for work order tasks across multiple locations.
    -   Receive intelligent guidance about all possible scheduling options for unscheduled tasks. Rank scheduling options based on agent-to-task match percentage, distance, and more.
    -   Hide off-shift agents so dispatchers can focus on who’s available and ready for tasks at that moment.
-   **Beans.ai map integration for bundled tasks**

    Optimize routes for bundled tasks with beans.ai.

-   **[Appointment booking enhancements](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use appointment booking enhanced configurations to perform the following tasks:

    -   Book appointments for work order tasks.
    -   Enable the system to calculate or skip lead time when rescheduling appointments, depending on the selected configuration.
    -   Consider holidays when calculating lead time for appointments.
-   **[Field Service Marketplace enhancements](https://www.servicenow.com/docs/access?context=fsm-marketplace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**
    -   Automate the process of pushing tasks to the marketplace, automatically creating marketplace requests, and listing eligible contractors as determined by your specified criteria.
    -   Set up task filters to identify the work order tasks that qualify for the marketplace.
    -   Incrementally push marketplace requests to eligible contractors based on their ranking using the **Progressive push** check box.
    -   Evaluate contractor responses and automatically assign tasks to the lowest-cost contractor using the **Response evaluation flow** field.
-   **[Field Service Quality Management](https://www.servicenow.com/docs/access?context=quality-management-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use Field Service Quality Management to do the following tasks:

    -   Review the quality and data from work order tasks before completion.
    -   Address work orders that have been reviewed and sent back for more information.
    -   Provide feedback to technicians and communicate as needed during the review process.
-   **[Workforce enhancements](https://www.servicenow.com/docs/access?context=using-manager-workforce&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Use Workforce enhanced configurations to perform the following tasks:

    -   Extend access across all personas, allowing every user regardless of their role to view their own calendars.
    -   Configure settings to enable group and territory calendar visibility, authoring agents to view the list and calendars of members in their group or within their territory when Workforce Optimization for Field Service isn't enabled.
    -   Enable agents to create personal events for themselves.
-   **[Multiple Work Configurations](https://www.servicenow.com/docs/access?context=configuring-work-configs&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Create configurations for multiple work types, such as Installation, Repair, Break fix, and Maintenance.

    -   Set up work configurations for different work types ensuring that relevant work types and flows appear for specified business units or departments.
    -   Create Service Management configurations \(SM Configs\) to support multiple workflows.
    -   Extend the work order task table to account for different work types.

## UI changes

-   **Capacity Management dashboard**

    Select date ranges and territories to view actual work demand alongside capacity metrics, as well as plot planned capacity against total work over a selected period using filters.

-   **Schedule Optimization**
    -   The Task Filter tab is renamed as Optimization Targets.
    -   A new tab is added for Restricted tasks.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Field Service configuration renamed as Field Service Order configuration for new customers.


## Changed in this release

-   **Capacity and Reservations Management**

    Capacity and Reservations Management data model has been changed to accommodate the agent's start and end location.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Dispatcher Workspace and Workforce Optimization for Field Service support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [Accessibility information](#field-service-management-rn-accessibility) section that follows.

-   **Google Maps APIs for Field Service Capabilities**

    Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

    Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

    You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

    If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

    For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


## Removed in this release

The Field Service dashboard is removed from the Emergency Exposure Management application.

## Deprecations

-   Starting with the Xanadu release, FSM Agent Classic Workspace plugin \(com.snc.agent\_workspace.fsm\) is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Field Service Management is a ServiceNow AI Platform feature that is available with activation of the Field Service Management plugin \(field\_service\_management\). For details, see [Activate Field Service Management](https://www.servicenow.com/docs/access?context=t_ActivateFieldServiceManagement&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

Additional Field Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Field Service Management](https://www.servicenow.com/docs/access?context=field-service-additional-plugins&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

Enable field service technicians to initiate and monitor sales opportunities directly through the Now Mobile Agent application by activating Technician driven sales with the Field Service \(com.snc.fsm\_technician\_sales\) plugin.

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The Dispatcher Workspace and Workforce Optimization for Field Service workspace support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    In addition, the following pages were updated to support reflow:

    -   Territory planning
    -   Service location
    -   Geography
    -   Agent recommendation
    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


## Related ServiceNow applications and features

-   **[Financial Management](https://www.servicenow.com/docs/access?context=c_ITFinance&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Field Service Management integrates with the ServiceNow® Financial Management application to allocate, track, and report expenses in your organization.

    **Note:** The Financial Management for CSM plugin \(com.snc.financial\_management\_for\_csm\) is no longer available for direct activation. You can request this plugin through Now Support Customer Service.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-integration&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and ServiceNow® Customer Service Management \(CSM\) applications to enable you to view account and contact information on work orders and work order tasks in the Field Service Management application.

-   **[Service Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Field Service Management integrates with the ServiceNow® Service Portfolio Management application to enable you to create work orders directly from project tasks.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service-specific implementations that provide tier 1 agents with the tools needed to respond to customers and to resolve cases.


