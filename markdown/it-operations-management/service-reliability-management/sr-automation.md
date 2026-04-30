---
title: Working with SRM alert automations
description: Alert automations contain alert grouping and management conditional triggers that execute response actions automatically, based on the contents of the alert.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Working with SRM alert automations

Alert automations contain alert grouping and management conditional triggers that execute response actions automatically, based on the contents of the alert.

An alert is created in SRM when a third-party monitoring tool has an event. The system analyzes incoming alerts, once a minute, and runs automations accordingly.

**Note:** Prior to creating alert automations, you should have installed and configured the Service Reliability Management application, available in the ServiceNow Store. See [Service Reliability Management](../reference/sr-landing-page.md) for more information.

## Grouping automations

Use alert grouping automations to group similar alerts and reduce the noise in your queue. Grouping automations are routing that helps you categorize by specific conditions. Each automation combines a set of filters and methods based on fields or condition matches.

**Note:** All grouping occurs before management automations run.

System automations for automatic group creation may be included when your system is provisioned. They are active by default.

View the grouping automations by navigating to the **Alert automations** module from your **Home** page. Select **Grouping** in the left panel.

Create grouping automations based on any criteria available from the field or condition fields.

**Note:** Prior to creating grouping automations, you should have teams, schedules, and integrations in place.

Automations are run only once on an alert, however, depending on when the alert or the automation entered the system, different things happen.

-   If an alert is created, and automation 1 is the only automation, it will run only once on that alert.
-   If you add automation 2 and 3 after that alert was created, they will not run on it unless the alert is updated. Those automations were never run on the alert to begin with.
-   If you close and reopen the alert, all three automations will run on it.

If you change an existing automation and an existing alert would have been captured by it, it won’t be. Whatever criteria or actions you have changed won’t be addressed unless the existing alert is closed and reopened. Then, whatever changed automation actions there are will take place.

Grouping automations run in the order chosen, from lowest to highest.

**Note:** Administrators can update, reorder or delete any SRM automation. Responders and managers can update and reorder only their own or their team's automations. Only system administrators \[admin\] can delete global automations.

![This is the alert automation rules homepage.](../image/sr-alert-group-rules-reorder.png)

**Note:**

Order is important for grouping automations because the lower-order automations run first. This can impact whether the conditions of higher-order automations are met, or will process. Lower-order automations can adjust field values or even stop processing.

None of the filters or sorting features for the list view change the order in which the automations are run.

**Grouping automations** list view contains information for:

-   **Order** represents the order the automations run in.
-   **Name** represents the group rule name and description.
-   **Active** represents whether the automation runs or not.
-   **Description** describes the group automation.
-   **Applies to** who is impacted by this rule. Whether the impact is **Global** or to a team.
-   **Clustering timeframe \(minutes\)** represents how long this automation should continue to run and group alerts after an initiating alert.

The run order of alert grouping is as follows:

-   Grouping rules run
-   Manually created groups are updated
-   Automated grouping runs

Alerts are grouped under the primary alert. The oldest of the highest severity alerts becomes the primary alert. The rest become related alerts. Grouping activity is recorded in **Work notes.**.

**Note:** Administrators, Managers and Responders can activate or deactivate only their own or their team’s automations.

System administrators \[admin\] can activate or deactivate any automation, including global automations.

When a Service is deleted, its integrations, alerts, incidents, and automations are removed. This is not a recoverable action so consider deactivating the service instead.

A grouped, related alert contains a **Grouped by** field. This field indicates how the related alert was grouped. For more information, see [SRM alert workspace](../reference/sr-alerts-workspace.md).

## Alert management automations

Use alert management automations to assign and respond to alerts. They run after all grouping has occurred. Management automations are routing that helps you adapt your response to specific conditions. Each automation combines a set of filters and an outcome, usually setting who is assigned, priority, or creating email, Slack channels, or Zoom meetings.

**Note:** Management automations do not run on incidents.

View the management rules by navigating to the **Alert automations** module from your **Home** page. Select **Escalate and notify** in the left panel.

Create rules based on any criteria available from the condition filter fields.

**Note:** Prior to creating management automations, you should have SRM teams, schedules, and integrations in place.

Automations are run only once on an alert, however, depending on when the alert or the automation entered the system, different things happen.

-   If an alert is created, and automation 1 is the only automation, it will run only once on that alert.
-   If you add automation 2 and 3 after that alert was created, they will not run on it unless the alert is updated. Those automations were never run on the alert to begin with.
-   If you close and reopen the alert, all three automations will run on it.

If you change an existing automation and an existing alert would have been captured by it, it won’t be. Whatever criteria or actions you have changed won’t be addressed unless the existing alert is closed and reopened. Then, whatever changed automation actions there are will take place.

Management automations run in the order chosen, from lowest to highest.

![This is the respond to alert rules page.](../image/sr-alert-rules-reorder.png)

**Note:** None of the filters or sorting features for the list view change the order in which the automations are run.

The **Order** field identifies the order in which the automations run.

**Note:**

Order is important for management automations because the lower-order automations run first. This can impact whether the conditions of higher-order automations are met, or will process. Lower-order automations can adjust field values or even stop processing.

You cannot reorder team automations to run before global automations. If a global automation is met, then all processing on automations stop, if the global automation is set for that.

**Escalate and notify automations** list view contains information for:

-   **Order** represents the order the automations run in.
-   **Name** represents the group rule name and description.
-   **Active** represents whether the automation runs or not.
-   **Description** describes the group automation.
-   **Applies to** who is impacted by this rule. Whether the impact is **Global** or to a team.
-   **Stop after automation is run** sets whether processing stops after that rule runs.

Management rule activity is recorded in **Work notes**.

**Note:** Managers and responders can activate, deactivate or delete only their own or their team’s rules.

Administrators and system administrators \[admin\] can activate, deactivate or delete any SRM rule. Only system administrators \[admin\] can activate, deactivate, or delete global automations and only in the classic UI.

When a Team is deleted, its automation rules are removed. This is not a recoverable action so consider deactivating the team instead.

**Parent Topic:**[Using Service Reliability Management](using-service-reliability-management.md)

**Previous topic:**[Manually create an SRM change task](../task/sr-create-change.md)

**Next topic:**[Service Reliability Management reference](../reference/service-reliability-management-reference.md)

