---
title: Configuring Workforce
description: Configure Workforce to view agent schedules, create personal events, and view tasks on a map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/configuring-workforce.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configuring Workforce

Configure Workforce to view agent schedules, create personal events, and view tasks on a map.

The CSM/FSM Configurable Workspace includes Workforce, which is a centralized workspace for essential tools such as the Team Calendar, Map, and Agent Location History Map. This integration allows for access and management of team schedules, geographical data, and historical agent movements, all from one location.

You can configure the team calendar to select which event types are visible. You can also enable users to switch between assignment group view and territory view. Additionally, you can improve the visibility of team members' schedules on a group calendar. By enabling team calendar visibility, they make these schedules accessible to both their own group and other groups.

To enable the territory view, you must [Configure Field Service Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/workforce-optimization-for-field-service/configuring-territory-planning-fsm.md). Managers need the wm\_manager role to view schedules in Workforce. Additionally, each territory must be assigned a manager. For more information on assigning territories to managers, see [Managing territories and agents from Territory Planning console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-manager-workforce/using-territory-planning-console.md).

When Workforce Optimization for Field Service is active, you can appoint additional managers to your assignment groups to allow them access to Workforce. This ensures that more team leaders can effectively manage and optimize Workforce activities. For more information on adding additional managers, see [Assign additional managers to user groups when Workforce Optimization for Field Service is installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/workforce-optimization-for-field-service/assign-additional-managers-to-user-groups.md).

Workforce supports a high volume of agents and tasks by default. If your workforce management requires expanded capacity, you can contact support or submit a change control request to adjust the configuration.

## Configuration overview

The steps for setting up Workforce are:

-   [Configure event types to appear on the Team calendar in Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/configure-event-types-to-appear-on-the-team-calendar.md)

    Customize the team calendar by configuring which event types are displayed.

-   [Set your Workforce system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/workforce-system-properties.md)

    Modify the Workforce configuration by setting system properties to enable visibility for both group and territory views.

-   [Configure team calendar visibility for group members](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/configure-team-cal-visibility-grp-members.md)

    Increase Team calendar visibility to enable teams to better coordinate meetings, events, and tasks.

-   [Configure territory view to allow users to see other members' schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/enable-territory-view.md)

    Allow users to switch between viewing assignment groups and territories within Workforce.


