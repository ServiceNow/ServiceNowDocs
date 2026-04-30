---
title: Manage and monitor alerts
description: An alert is a notification for selected events that are considered to be important and require attention. Event Management generates alerts based on event rules.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Manage and monitor alerts

An alert is a notification for selected events that are considered to be important and require attention. Event Management generates alerts based on event rules.

You can monitor and resolve alerts in ways that are based on alert impact calculations and alert configuration and property settings.

-   **[Alert management rules for resolving alerts](alert-management-rule.md)**  
You can configure Event Management to respond to alerts automatically. An alert management rule determines the required alert response, such as to open an incident, knowledge base article, open a task, launch remediation action.
-   **[CI Remediation](ci-remediation.md)**  
Alert and configuration item \(CI\) remediations help troubleshoot and resolve underlying problems that generate alerts. Remediation is based on Orchestration workflows that can be scripted to perform remediation tasks such as gathering system information or rebooting a server.
-   **[How alerts work with CIs in maintenance](c_EMHowImpactTree.md)**  
When a CI is in maintenance, the impact tree, the service map, and Alerts tab are updated based on various factors.
-   **[SLAs for application services and CIs](c_EMSLAsForBSAndCIs.md)**  
Event Management supports the creation of SLAs for application services and for CIs.
-   **[Alert lifecycle configuration](c_EMAlertRule.md)**  
Event Management provides various modules, templates, and properties for configuring alerts and the actions that execute for these alerts.
-   **[Alert priority](alert-priority.md)**  
Determine the order in which to handle alerts according to the alert priority score. Multiple factors determine the alert priority score and this value changes with changes to the underlying factors.
-   **[Alert assignment groups for teams](alert-assignment-group.md)**  
Alert assignment groups assign alerts to the right teams promptly and automatically, improving overall incident management capabilities.
-   **[Express List Configuring Express List views for users and user groups](../../service-operations-workspace-itom/concept/manage-views-express-list.md)**  
Centrally control what users monitor by predefining views in Express List and assigning them to users and user groups.
-   **[Probable Root Cause Analysis \(RCA\)](probable-rca.md)**  
Shorten the mean time to repair \(MTTR\) by discovering the root cause of an alert.
-   **[Alert similarity](alert-similarity.md)**  
Finding alerts that are similar to the alert that you are currently investigating can help save troubleshooting time by seeing how similar alerts were resolved.
-   **[Self-health monitors for Event Management](self-monitoring.md)**  
Use the Event Management self-health monitors to track Event Management features and resolve issues.
-   **[Create maintenance rules](../task/create-maintenance-rule.md)**  
Use maintenance rules to mark CIs in maintenance status. When in maintenance status, these CIs are excluded from impact calculation.
-   **[Resolve an incident related to an alert](../task/t_EMResolveCloseIncidentAlert.md)**  
When you resolve an incident that is associated with an alert, the alert can also close according to the **evt\_mgmt.incident\_closes\_alert** property.
-   **[Close an alert](../task/t_EMCloseAlert.md)**  
Close an alert by an event or a user action. Closing an alert also closes any related incident that is not already resolved or closed.
-   **[Reopen an alert](../task/t_EMReopenAlert.md)**  
Additional events can cause reopening of alerts, or you can reopen an alert by changing its state. When an alert reopens, any associated incidents can also be updated or reopened according to the incident state and the **evt\_mgmt.alert\_reopens\_incident** property.
-   **[Alert insight properties](../reference/configure-alert-insight-properties.md)**  
Use these properties to configure alert insight.
-   **[Rotate event tables and alert table cleanup](rotate-tables-purge-data.md)**  
The growth of data tables impedes performance. Preserve instance performance by event table rotation and alert table cleanup for status and alert history retention.

**Parent Topic:**[Configuring Event Management](using-event-management.md)

