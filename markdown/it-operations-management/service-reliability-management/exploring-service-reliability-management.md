---
title: Exploring Service Reliability Management
description: Service Reliability Management \(SRM\) provides a self-serve, guided experience for teams to manage service health. The experience is built using the Service Operations Workspace application and combines ITOM and ITSM capabilities into a single workflow.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Exploring Service Reliability Management

Service Reliability Management \(SRM\) provides a self-serve, guided experience for teams to manage service health. The experience is built using the Service Operations Workspace application and combines ITOM and ITSM capabilities into a single workflow.

## SRM overview

Optimize service health with site reliability engineering \(SRE\) practices. SRM is a single operations workspace that empowers teams to improve the reliability of digital services with SRE.

-   Use on-call escalations to respond to issues in a timely manner.
-   Reduce setup friction with guided self-service to onboard distributed teams with separated data, empowered access, and minimal governance from central IT.

When SRM is installed, several plugins and applications are also activated. For more information, see [Plugins or applications installed with ITOM AIOps](../../it-operations-management/reference/plugin-app-itom-health.md).

## SRM users

<table id="table_ayk_qqd_pwq"><thead><tr><th>

Users

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

admin

</td><td>

A ServiceNow administrator is responsible for the administration, development, operation, education, and maintenance of the ServiceNow platform.

 Responsible for installation and can perform Service Operations Workspace Admin Center configuration of SRM.

</td><td>

All

</td></tr><tr><td>

Administrator \[srm\_admin\]**Note:** This role differs from the ServiceNow admin role.

</td><td>

SRM administrators can manage account settings, configurations, and users.

 Administrators can perform the following actions:

-   Access, create, edit, or delete all SRM configurations.
-   Add or manage integrations.
-   Create integrations with Application Performance Monitoring \(APM\) tools.
-   Set up and maintain reliability metrics.
-   Set up and maintain error budget policies.

</td><td>

-   Manager
-   Responder

</td></tr><tr><td>

Manager \[srm\_manager\]

</td><td>

Managers oversee a team of SREs. Managers assign SREs to the team on-call schedule, monitor their performance, and create procedures to handle incidents and develop solutions. Managers promote resilience across all the systems and the DevOps workflows.Managers can perform the following actions within the context of their teams:

-   Define and set up teams, on-call schedules, and services.
-   Add and delete users such as responders and managers for the teams they're a part of.
-   Add or manage integrations.
-   Create Integrations with Application Performance Monitoring \(APM\) tools.
-   Set up and maintain reliability metrics.
-   Set up and maintain error budget policies.

</td><td>

Responder

</td></tr><tr><td>

Responder \[srm\_responder\]

</td><td>

A Service Reliability Engineer \(SRE\) that uses SRM to perform everyday tasks. Responders are the individuals who are on call and diagnose and remediate incidents.

 Responders can only access configurations that they’re a part of. They can only access the alerts or incidents for which they have permissions.

 SREs can perform the following actions, within the context of their teams:

-   Set up services, teams, and integrations.
-   Confirm their on-call schedules.
-   Manage incident and alert records.
-   Update teams that they’ve created.
-   Add other responders.
-   Create integrations with Application Performance Monitoring \(APM\) tools.
-   Set up and maintain reliability metrics.
-   Set up and maintain error budget actions.

</td><td>

Inherits 17 roles including the following:

-   cmdb\_read
-   sn\_sow.sow\_user
-   sn\_sow\_srm.srm\_responder
-   workspace\_user
-   slo\_operator

</td></tr></tbody>
</table>For more information, see [SRM roles and responsibilities](../reference/sr-roles.md).

## SRM workflow

![Infographic showing how responders, managers, and administrators manage teams, register services, define SLO, monitor integrations, respond to notifications, and remediate incidents. For details, refer to the following description.](../image/sr-explore-workfflows.png)

1.  Product teams in IT or Lines of Business continuously deliver new technical and application services. Example: New customer billing portal.
2.  Along with SLO Management, teams can register services and define service level objectives \(SLOs\), helping them reach business outcomes. Example: 95% monthly availability for the billing portal.
3.  Monitoring integrations are set up by the teams to collect the real-time health of these services. Example: Cloud Observability.
4.  Monitoring creates service level indicators \(SLIs\) impacting alerts when services are underperforming. Automation groups and enriches. Example: Billing portal latency is exceeding 7 s.
5.  When the alerts indicate an outage or customer-impacting degradation, incidents are created and on-call notifications notify appropriate team resources. Example: A Billing SRE team is notified via phone of a latency issue on the billing portal.
6.  After teams collaboratively diagnose and remediate incidents, they identify action items for improving the system's resilience. Example: The Billing team decides to add additional web server capacity.
7.  Management continually reviews SLO performance, helps to prevent changes when the error budget is exhausted, and prioritizes improvement initiatives for underperforming services.

## SRM benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Team-based experience|[Working with SRM teams](sr-work-teams.md)|SRM administrators, managers, and responders|
|Service registration|[Working with SRM services](sr-work-services.md)|SRM administrators, managers, and responders|
|Prebuilt integrations|[Working with SRM integrations](sr-work-integrations.md)|SRM administrators, managers, and responders|
|Measure service health|[Working with reliability metrics](../../slo-management/concept/sr-work-SLI-SLO.md)|SRM administrators, managers, and responders|
|On-call coverage|[Create an SRM on-call schedule](../task/sr-create-on-call-schedule.md)|SRM administrators, managers, and responders|
|Remediate high severity alerts and incidents|[Working with SRM reliability tasks](../task/sr-work-reliability-tasks.md)|SRM administrators, managers, and responders|

## What to explore next

To learn more about configuring and using SRM, see:

-   [Configuring Service Reliability Management](configuring-service-reliability-management.md)
-   [Using Service Reliability Management](using-service-reliability-management.md)
-   [Service Reliability Management reference](../reference/service-reliability-management-reference.md)

-   **[Get started with Service Reliability Management](sr-get-started.md)**  
Service Reliability Management \(SRM\) accelerates your path to viewing service health in the context of service level objectives and incident resolution. Helps IT Operations and DevOps teams deliver on the promise of agility, performance, and uptime.
-   **[SRM incidents](../reference/sr-incidents-workspace.md)**  
Track and collaborate on incidents in the Incidents tab, helping you and your teams resolve issues efficiently.

**Parent Topic:**[Service Reliability Management](../reference/sr-landing-page.md)

