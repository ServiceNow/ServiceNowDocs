---
title: Application services for Event Management operators
description: As an Event Management operator, you need to understand what application services are.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Application services for Event Management operators

As an Event Management operator, you need to understand what application services are.

This is the second lesson in the Event Management tutorial.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Lesson 1

</td><td align="justify">

![Overview events icon](../image/progress-complete2.png)

</td><td>

[An overview of events and alerts](operator-events-alerts.md)

</td></tr><tr><td>

Lesson 2

</td><td align="justify">

![Overview BS icon](../image/progress-wip.png)

</td><td>

An overview of application services

</td></tr><tr><td>

Lesson 3

</td><td align="justify">

![Operator icon](../image/progress-not-started.png)

</td><td>

[Event Management operator workspaces](operator-user-interfaces.md)

</td></tr><tr><td>

Lesson 4

</td><td align="justify">

![What operators do icon](../image/progress-not-started.png)

</td><td>

[What operators do](operator-process.md)

</td></tr></tbody>
</table>An application service is a collection of components, such as network devices, computers, and applications that offer a service to your organization. The services can be something like an email system or a website that tracks orders or requests in a database. Your administrator should have already specified the application services in your ServiceNow instance.

Each component that makes up an application service is referred to as a configuration item or CI. This service map provides a visual representation of an application service:

![Service map](../image/operator-business-service.png "Service map")

In this example, you can see a Web Portal application service with these CIs:

-   **PS Apache03**: An Apache web server that hosts a company website.
-   **PS LinuxApp01** and **PS LinuxApp02**: Two Linux servers that share the workload from the web server.
-   **PS ORA01**: A database server that both Linux servers need to access.
-   **Storage Area Network 001**: A mass storage device on which the other CIs depend.

You can see service maps like this on the Service Operations Workspace dashboard. Later in this tutorial, you will learn about the dashboard and what an application service looks like when an alert is associated with a CI.

## Types of application services

Event Management classifies application services into the following types:

-   **Technical services**

    A technical service is a dynamic grouping of CIs based on some common criteria. For example, a technical service could be comprised of all web servers or all Oracle databases for a specific location, like North America.

-   **Application services**

    An application service can consist of discovered services, manual services, or both. A discovered service is an application service that the [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md) application finds \(if your organization uses [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md)\). A manual service is an application service that your administrator configures by selecting and adding each CI and specifying the relationships between CIs.

-   **Alert groups**

    Alerts that are grouped together, either manually or automatically.


## Alert impact

Application services are critical to the operations of your organization. If an issue occurs on one CI, the entire application service can be affected. Part of your role as an operator is to analyze alerts on CIs and see how they impact the application service as a whole, and then take an action to help remediate or solve the underlying issue. Your administrator can configure impact rules that go into calculations for the severity of an alert.

Later, when you learn how to use the Service Operations Workspace dashboard, you will learn how to view an impact tree for an application service so you can understand the relationship between the severity of an alert and the overall application service.

In this example, you can see how a **Major** alert on an Oracle database \(**PS ORA01**\) also causes a major alert on its parent CIs and on the Web portal application service itself.

![Impact tree](../image/operator-dashboard-impact-tree.png "Impact tree")

## Continue the tutorial

Proceed to the next lesson: [Event Management operator environment](operator-user-interfaces.md).

**Parent Topic:**[Event Management Operator Tutorial](operator-guide-em.md)

