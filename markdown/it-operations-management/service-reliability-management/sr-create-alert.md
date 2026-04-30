---
title: Manually create an SRM alert
description: Create an alert for testing purposes or if you think an issue poses a risk.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with alerts in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Manually create an SRM alert

Create an alert for testing purposes or if you think an issue poses a risk.

## Before you begin

Role required: srm\_admin, srm\_manager, or srm\_responder

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  In the navigation pane, select **Services**.

3.  Select the service that you want to trigger an alert for.

4.  Select the **Related alerts** tab.

5.  Select **Trigger alert** and fill out the **Trigger an alert** form.

    To trigger an alert, you must first create an event to get processed. Only **Service** is required.

<table id="table_ows_1c4_b2c"><thead><tr><th>

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

Enter the name of the node \(for example, FQDN, IP address, or MAC address\) associated with the event.

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

Enter the name of the metric associated with the event.

</td></tr><tr><td>

Source instance

</td><td>

Enter a data source for the event.

</td></tr><tr><td>

Message key

</td><td>

Enter an identifier for multiple events related to the same event.

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

Select the date and time that the event occurred in the source system.

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
</table>6.  Select **Trigger**.

    Service Reliability Management \(SRM\) creates an event to generate the alert. Refresh the screen to see the event processing results.

    Express List automatically displays your alert. If enabled, SRM triggers the applicable automations and on-call escalation workflows.


## What to do next

Consider making the following optional adjustments to your alert for testing purposes or team collaboration:

-   Acknowledge the alert or assign it to someone on your team.
-   Add comments or work notes in the **Compose** panel.
-   Add an attachment related to the alert using the attachment icon ![Attachment icon](../image/icon-sr-attachment.png).

**Parent Topic:**[Working with alerts in SRM](../concept/sr-work-alerts-expresslist.md)

