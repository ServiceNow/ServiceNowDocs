---
title: Get started with Service Reliability Management
description: Service Reliability Management \(SRM\) accelerates your path to viewing service health in the context of service level objectives and incident resolution. Helps IT Operations and DevOps teams deliver on the promise of agility, performance, and uptime.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Get started with Service Reliability Management

Service Reliability Management \(SRM\) accelerates your path to viewing service health in the context of service level objectives and incident resolution. Helps IT Operations and DevOps teams deliver on the promise of agility, performance, and uptime.

Get started with SRM to understand the different sections in the SRM interface.

For more information on roles, see [SRM roles and responsibilities](../reference/sr-roles.md).

## Basic SRM tasks

|Step|Description|Reference|
|----|-----------|---------|
|Set up teams and services|Setup guides for the Home, Services, and Teams pages show how to add a team or service to SRM.|[Add an SRM team](../task/sr-create-team.md)|
|Visit and learn about your Home page|The Home page is where you find the things most important to you. For example, the services with critical alerts and incidents and work assigned to you and your team.|[SRM Home page](../reference/sr-home-page.md)|
|Learn how to navigate SRM|Get familiar with the different sections and elements of the SRM interface. The sections and elements are used throughout the documentation.|[SRM interface](sr-navigate-interface.md)|

SRM helps you when you must create and administer teams, services, and integrations.

<table id="table_zqr_2l1_zhz"><thead><tr><th>

Step

</th><th>

Description

</th><th>

See this

</th></tr></thead><tbody><tr><td>

Manage an application or technical service in SRM

</td><td>

Define the basic tasks and parameters that make up your service and how it should behave.

</td><td>

[Add a service to SRM](../task/sr-add-service.md)

</td></tr><tr><td>

Set up an SRM team

</td><td>

Set up a team. Teams are responsible for the issues that occur in their associated services.

</td><td>

[Add an SRM team](../task/sr-create-team.md)

</td></tr><tr><td>

Set up on-call schedules and escalation policies

</td><td>

Create an on-call schedule for your team to make sure they're available to resolve issues. You can set up an escalation policy to make sure at least one team member is engaged in incident response.

</td><td>

[Create an SRM on-call schedule](../task/sr-create-on-call-schedule.md)

</td></tr><tr><td>

Configure service relationships

</td><td>

Use a map canvas to add, configure, and arrange services. You can add child services that depend on parent services.

</td><td>

[View impact of child service on parent service](../../event-management/task/cross-business-service-impact.md)

</td></tr><tr><td>

Integrate services with third-party monitoring tools

</td><td>

Set up a third-party integration, such as Datadog or ServiceNow Cloud Observability, with SRM so that alerts are available to your teams within SRM.

</td><td>

[Working with SRM integrations](sr-work-integrations.md)

</td></tr><tr><td>

Establish SLOs, SLIs &amp; error budgets for services

</td><td>

Establish goals for how well your service should operate. Also, specify the maximum amount of time that a technical system can fail without contractual consequences.

</td><td>

Service Level Objective Management

</td></tr><tr><td>

Set up alert automations

**Note:** This functionality is only available if you have installed the Alert automations application.

</td><td>

Alert automations enable you to define alert conditions. Set up alert rules for each APM tool to define the conditions when the APM tool should send notifications to SRM.

</td><td>

The Alert automation application is available from the ServiceNow Store.

</td></tr></tbody>
</table>-   **[SRM Home page](../reference/sr-home-page.md)**  
The Service Reliability Management \(SRM\) Home page provides relevant information about your work, services, schedules, maintenance reminders, and teams. View the Home page by navigating to **Service Reliability Management**.
-   **[SRM interface](sr-navigate-interface.md)**  
The different components on the Service Reliability Management \(SRM\) interface provide easy access to different functions. The features and functions that appear depend on your role and permissions.

**Parent Topic:**[Exploring Service Reliability Management](exploring-service-reliability-management.md)

