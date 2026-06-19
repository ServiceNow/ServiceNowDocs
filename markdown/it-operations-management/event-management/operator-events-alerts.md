---
title: An overview of alerts for Event Management operators
description: As an Event Management operator, you need to understand how an alert is generated from an event, what to look for in an alert, and how alerts can be grouped together.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/operator-events-alerts.html
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# An overview of alerts for Event Management operators

As an Event Management operator, you need to understand how an alert is generated from an event, what to look for in an alert, and how alerts can be grouped together.

This is the first lesson in the Event Management tutorial.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Lesson 1

</td><td align="justify">

\[Omitted image "progress-wip.png"\] Alt text: Overview icon

</td><td>

An overview of events and alerts

</td></tr><tr><td>

Lesson 2

</td><td align="justify">

\[Omitted image "progress-not-started.png"\] Alt text: Overview of BS icon

</td><td>

[An overview of application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-application-services.md)

</td></tr><tr><td>

Lesson 3

</td><td align="justify">

\[Omitted image "progress-not-started.png"\] Alt text: Overview operator icon

</td><td>

[Event Management operator workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-user-interfaces.md)

</td></tr><tr><td>

Lesson 4

</td><td align="justify">

\[Omitted image "progress-not-started.png"\] Alt text: Overview of what operators do icon

</td><td>

[What operators do](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-process.md)

</td></tr></tbody>
</table>Your organization already has an event monitoring tool in place, such as Microsoft System Center Operations Manager \(SCOM\), Nagios, SolarWinds, and so on. When an issue occurs on your network, such as a computer going down or a database failure, the event monitoring tools send events to your ServiceNow instance. The Event Management application processes the events according to the settings that your administrator configured, and then generates alerts. An alert is an indicator that the issue requires some type of action.

\[Omitted image "operator-event-management-overview.png"\] Alt text: An operator view of Event Management

As an Event Management operator, your role is to view alerts and, depending on how Event Management is implemented in your organization, take an action to help resolve the underlying issue or notify someone who can. Later in this tutorial, you will see the phases of a typical alert management process.

## Alert priority and severity

The two most common characteristics of an alert are the priority and the severity.

-   The priority of an alert is a score that helps you determine how important the impact is to application services. Multiple factors determine the alert priority score. Your Event Management administrator can configure the algorithm that the Event Management application uses to calculate priority.
-   The severity of an alert is an indicator of how serious the underlying issue is. The event monitoring tool in your organization usually sends severity values with the event, which then gets carried over in the alert. These are the default severity types that you will see in this tutorial:

<table id="table_egv_c31_gdb"><thead><tr><th>

Severity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "severity-critical.png"\] Alt text: Resource icon **Critical**

</td><td>

The resource is either not functional or critical problems are imminent.

</td></tr><tr><td>

\[Omitted image "severity-major.png"\] Alt text: Functionality icon **Major**

</td><td>

Major functionality is severely impaired or performance has degraded.

</td></tr><tr><td>

\[Omitted image "severity-minor.png"\] Alt text: Minor icon **Minor**

</td><td>

Partial, non-critical loss of functionality or performance degradation occurred.

</td></tr><tr><td>

\[Omitted image "severity-warning.png"\] Alt text: Warning icon **Warning**

</td><td>

Attention is required, even though the resource is still functional.

</td></tr><tr><td>

\[Omitted image "severity-info.png"\] Alt text: OK icon **OK**

</td><td>

No severity. An alert is created. The resource is still functional.

</td></tr><tr><td>

\[Omitted image "severity-clear.png"\] Alt text: Clear icon **Clear**

</td><td>

The alert no longer needs action.

</td></tr></tbody>
</table>
## Correlated alerts

Some alerts are related to each other. For example, if a router goes down, several separate alerts could be generated, one for each server connected to the router. All of these alerts are related, or correlated. To help you manage correlated alerts, Event Management can automatically group them and establish a two-level hierarchy with one root alert, called the primary alert, at the top, and other related alerts, called secondary alerts, under the primary alert. When you view alerts, primary alerts stand out by default so you know which alert to focus on without being distracted by the secondary alerts.

In our example, if a router goes down on your network, network communication is also affected for connected servers, assuming they cannot reach any other routers. The router outage becomes the primary alert and the alerts generated on the server are secondary alerts that are correlated under the router alert.

\[Omitted image "operator-multiple-alerts.png"\] Alt text: Correlated alerts

Depending on your organization's Event Management implementation, alerts might be grouped automatically based on correlation rules that your administrator sets up. Your instance can also learn how to improve the way it correlates alerts based on these rules. As an operator, you should still verify the accuracy of the correlation and, if necessary, manually correlate additional alerts with the primary alert. Later in the tutorial, you will learn how to do this.

In this tutorial, you will learn how to manually correlate alerts.

## Alert flapping

An alert can flap, meaning that it gets multiple open-close events in rapid succession. Flapping indicates that Event Management does not know whether the underlying events are genuine or not. The events could indicate small issues with the way CIs are configured, or larger issues, like network outages.

\[Omitted image "alert-flapping-cpu.png"\] Alt text: CPU usage

For example, if a server that hosts a web service has too many active processes, it might trigger an event about excessive CPU usage. Since CPU usage can fluctuate rapidly depending on web service requests, several events might be triggered, leading to the alert being put in the flapping state. As an operator, you might need to create an incident to have the server restarted, or someone might have to reconfigure the CPU, or possibly make a hardware change on the device.

As another example, consider a loose network cable that causes momentary, repeated network outages. The thresholds that your administrator configures might not be optimal for this kind of alert and Event Management considers it a flapping alert.

## Continue the tutorial

Proceed to the next lesson: [Application services for Event Management operators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-application-services.md).

**Parent Topic:**[Event Management Operator Tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-guide-em.md)

