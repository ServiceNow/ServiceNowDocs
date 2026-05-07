---
title: Operator phase 1: Analyze and acknowledge an alert
description: As an Event Management operator, the first thing you should do is access alerts and then find the ones you want to focus on. You can open the Alert form to analyze the details, and then acknowledge it to let other operators know that the issue causing the alert should be addressed in some way.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Operator phase 1: Analyze and acknowledge an alert

As an Event Management operator, the first thing you should do is access alerts and then find the ones you want to focus on. You can open the Alert form to analyze the details, and then acknowledge it to let other operators know that the issue causing the alert should be addressed in some way.

## Before you begin

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Analyze icon](../image/progress-wip.png)

</td><td>

Analyze and acknowledge an alert

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Triage icon](../image/progress-not-started.png)

</td><td>

[Triage alerts](operator-phase-triage-incident.md)

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Close alert icon](../image/progress-not-started.png)

</td><td>

[Close an alert](operator-close-alert.md)

</td></tr></tbody>
</table>You must understand both of your operator environments: the Service Operations Workspace dashboard and Service Operations Workspace. Review [Event Management operator environment](../concept/operator-user-interfaces.md) if you have not already done so. This tutorial uses the Service Operations Workspace dashboard.

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Event Management** &gt; **Workspaces** &gt; **Service Operations Workspace**.

    In the list, click **Alerts** &gt; **All Alerts**. By default, all alerts appear in the list sorted by **Group**. Click any heading to sort by that value. To view current filter settings, click the filter icon ![Filter icon](../image/filter-icon.png). To modify filter settings, click **Advanced view**.

    ![List of alerts](../image/list-all-alerts.png)

2.  Find the alerts to focus on by clicking **Application Services** &gt; **Services**, or by using any of the filtering and sorting options.

3.  Click an alert name to open the **Details** tab for the alert.

    The important fields on the form and related items are described after the screenshot.

    ![Alert details](../image/operator-app-service-alert-example.png)

<table id="table_umx_h5t_hdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated alert number that you saw in the list of alerts on the Service Operations Workspace dashboard.

</td></tr><tr><td>

Node

</td><td>

The name of the CI with which the alert is associated. The event that generated the alert occurred on this CI. You might see a computer name, or an IP address or MAC address of a device.

</td></tr><tr><td>

Resource

</td><td>

The object on the node that caused the event. You might see values like the name of a hard disk, a CPU, or the name of a process or a service. You can add information to this field if necessary.

</td></tr><tr><td>

Configuration item

</td><td>

The CI in the CMDB to which this alert applies. If the **Node** field is filled in but this field is empty, and if you know which CI the node represents, you can enter the CI in this field to manually associate the alert with it. **Note:** Your administrator can configure rules that automatically bind CIs to an alert, usually based on what is in the **Node** field. However, it is possible that the system is unable to find the correct CI to bind the alert to. In this case, you might need to manually select a CI.

For the purposes of this tutorial, we assume that the correct CI is bound to the alert.

 When an alert contains a CI, the **Overview** tab opens when selecting the alert.

</td></tr><tr><td>

Task

</td><td>

Any existing task that is associated with the alert, such as an incident, change request, or problem, is shown in this field. When you first look at an alert, this field is blank. You can associate a task when you triage the alert. You associate an incident to an alert and assign the incident to someone at a later stage in this tutorial.

</td></tr><tr><td>

Description

</td><td>

A description of the alert that came from the alert monitoring software in your organization. You can add information if necessary.

</td></tr><tr><td>

Severity

</td><td>

Severity value for the alert: -   Critical: Immediate action is required. Either the resource is not functional or critical problems are imminent.
-   Major: Major functionality is severely impaired or performance has degraded.
-   Minor: There is a partial, non-critical loss of functionality, or performance has degraded.
-   Warning: Attention is required even though the resource is still functional.
-   Info: An informational message. An alert is created, but the resource is still functional.
-   Clear or Resolved: No action is required. An alert is not created from this event. Existing alerts are closed.


</td></tr><tr><td>

State

</td><td>

The processing state that the alert is in. A newly generated alert is in the **Open** state. Other states are:-   **Reopen** indicates that a previously closed alert is open again, and it requires your attention.
-   **Flapping** indicates that the alert is receiving a high frequency of identical events from the same source, which can cause many alerts to re-open even after it is closed.
-   **Closed** indicates that the alert is closed and does not require any further action. You will close an alert as part of the last stage in this tutorial.


</td></tr><tr><td>

Maintenance

</td><td>

Indicates that the alert does not need to be worked on and is hidden from the list of alerts in the Service Operations Workspace dashboard. In this example, we do not want to put the alert in maintenance.

</td></tr><tr><td>

Acknowledged

</td><td>

Indicates that an operator verified that the alert is genuine and is triaging it. You acknowledge the alert at a later stage in this topic.Your Event Management administrator can also have alerts automatically acknowledged immediately after they are generated. If this is the case, the **Acknowledge** check box on the Alert form might already be selected.

</td></tr><tr><td>

Parent

</td><td>

Displays a value only for secondary alerts. The value indicates the alert number of the parent alert. The field is empty for primary alerts \(alerts with no parent alert\).

</td></tr><tr><td>

Knowledge article

</td><td>

Any existing knowledge base \(KB\) article that is associated with the alert. When you first open an alert, this field is blank. You can associate a KB article when you triage the alert.

</td></tr></tbody>
</table>4.  Click the **Impacted Services** tab and then click the service name.

    Before you acknowledge the alert, you might want to learn more about the services that are affected due to the service that is the source of the alert.

    The service opens and displays the **Details** tab. Click **Service Map** to view the map of related application services.

    ![Service map](../image/operator-bsm-alert-example.png)

    Notice that the major severity indicator in orange is displayed on several CIs. It starts with the Oracle database \(**PS ORA01**\) and propagates up to all CIs that depend on the database. From this, you can surmise that the alert with the highest level of severity on the Oracle database indicates the root cause of the issue.

    This does not necessarily mean that the system generated separate alerts for each CI, but it is possible. When you triage an alert, you can determine whether alerts on other CIs should be correlated under a primary alert.

5.  Click the **Impact Tree** tab and review the impacts on each CI.

    The percentages next to each CI in the impact tree show you the effect on each CI. In this example, each CI is impacted 100% by the alert, which means the underlying issue that led to the alert is serious enough to impact the functionality of the application service.

    ![Impact tree](../image/operator-dashboard-impact-tree.png)

6.  Acknowledge the alert.

    Acknowledging an alert does not assign it to you, nor does it create a task like an incident or change request. It simply lets other operators know that you are aware of the issue. After you acknowledge an alert, you will take further action during the triage stage.

<table id="choicetable_w31_kkr_jkb"><tbody><tr><td id="d438485e548">

**Acknowledge a single alert**

</td><td>

With this process, you can acknowledge only the alert that you are viewing.1.  Open the Alert Details form as described earlier.
2.  Select the **Acknowledged** check box.


</td></tr><tr><td id="d438485e569">

**Acknowledge one or more alerts**

</td><td>

With this process, you can acknowledge one alert or multiple related alerts.1.  Open the list of alerts as described earlier.
2.  Select each alert to acknowledge.
3.  Click **Acknowledge**.


</td></tr></tbody>
</table>7.  Navigate back and look for the alert that you acknowledged.

    You can see that the **Acknowledged** value is **true**.

    ![Alert that is acknowledged](../image/alert-acknowledged.png)


## What to do next

Go to [Operator phase 2: Triage an alert](operator-phase-triage-incident.md).

**Parent Topic:**[What Event Management operators do](../concept/operator-process.md)

