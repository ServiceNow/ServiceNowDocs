---
title: Manually create an SRM alert
description: Create an alert for testing or if you think an issue poses a risk and should be evaluated as soon as possible.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with alerts in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Manually create an SRM alert

Create an alert for testing or if you think an issue poses a risk and should be evaluated as soon as possible.

## Before you begin

Role required: Responder, Manager, or Administrator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  On the left navigation pane, select **Reliability tasks**.

3.  Select **Trigger alert** from the **Alert** list header.

    ![Reliability tasks landing page.](../image/sr-trigger-alert.png)

4.  In the **Trigger an alert** window, fill in the fields.

    To trigger an alert you must first create an event to get processed. Only **Service** is mandatory.

<table id="id_wkh_v5j_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service

</td><td>

Select a service for the event.

</td></tr><tr><td>

Source

</td><td>

Manual.

</td></tr><tr><td>

Node

</td><td>

Enter a name of the node \(FQDN, IP address or MAC address\) associated with the event.

</td></tr><tr><td>

Type

</td><td>

Enter a type of event.

</td></tr><tr><td>

Resource

</td><td>

Enter a node resource \(process or service\) associated with the event.

</td></tr><tr><td>

Metric Name

</td><td>

Enter a name of the metric associated with the event.

</td></tr><tr><td>

Source instance

</td><td>

Enter a data source for the event.

</td></tr><tr><td>

Message key

</td><td>

Enter an identifier for multiple events related to the same event

</td></tr><tr><td>

Severity

</td><td>

Select the expected impact of this event.Choices are:

-   Critical: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   Major: Major functionality is severely impaired or performance has degraded.
-   Minor \(default\): Partial, non-critical loss of functionality or performance degradation occurred.
-   Warning: Attention is required, even though the resource is still functional.
-   OK: The resource is still functional.


</td></tr><tr><td>

Time of the event

</td><td>

Select date and time that the event occurred in the source system.

</td></tr><tr><td>

Description

</td><td>

Enter information describing the event.

</td></tr><tr><td>

Additional information

</td><td>

Add more information relevant to the event.

</td></tr><tr><td>

Processing notes

</td><td>

Enter relevant processing information.

</td></tr></tbody>
</table>5.  Select **Trigger**.

    The new event is created to generate the alert. Refresh the screen to see to see the event processing results.

    The alert view automatically refreshes your **Alert** list view.

    If enabled, applicable automations are triggered, as well as any on-call escalation workflows for that service’s on-call team.

6.  Open the alert from the list view in the **Alert** tab.

7.  **Acknowledge** the alert, or use **Assign to** to assign it to someone on the team.

8.  Add any comments or work notes in the **Compose** panel.

9.  Add an attachment related to the alert using the attachment icon ![attachment icon](../image/icon-sr-attachment.png).

10. Select **Save**.

    The alert refreshes with comments, work notes, and activity captured in the **Activity** stream. For more information on alert fields, see [SRM alert workspace](../reference/sr-alerts-workspace.md).


**Parent Topic:**[Working with alerts in SRM](../concept/sr-work-alerts.md)

