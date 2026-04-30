---
title: Exploring Service Reliability Management
description: Service Reliability Management \(SRM\) provides a self-serve, guided experience for teams to autonomously manage the health of their technical services. The experience is built using the Service Operations Workspace application and combines ITOM and ITSM capabilities into a single service operations workflow.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Service Reliability Management, ITOM Health, IT Operations Management]
---

# Exploring Service Reliability Management

Service Reliability Management \(SRM\) provides a self-serve, guided experience for teams to autonomously manage the health of their technical services. The experience is built using the Service Operations Workspace application and combines ITOM and ITSM capabilities into a single service operations workflow.

## SRM overview

Optimize service health with Service Reliability Management \(SRM\) for teams in IT adopting site reliability engineering \(SRE\) practices. SRM is a single operations workspace that empowers teams to improve the reliability of digital services with SRE.

-   Use on-call escalations to respond to issues identified by your monitoring and ITOM alerts in a timely manner.
-   Reduce setup friction with guided self-service to onboard distributed teams with separated data, empowered access, and minimal governance from central IT.

When SRM is activated, several plugins and applications are also installed. For more information, see [Plugins or applications installed with ITOM Health](../../it-operations-management/reference/plugin-app-itom-health.md).

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

Administrator \[srm\_admin\]**Note:** Not the ServiceNow `admin` role

</td><td>

SRM Administrators can manage account settings, configurations, and users.

 Administrators can perform the following actions:

-   Access, create, edit, or delete all SRM configurations.
-   Add or manage integrations.
-   Create Integrations with Application Performance Monitoring \(APM\) tools
-   Set up and maintain Reliability Indicators.
-   Set up and maintain Error Budget Policies.

</td><td>

-   Manager
-   Responder

</td></tr><tr><td>

Manager \[srm\_manager\]

</td><td>

Managers oversee a team of SREs. Managers assign SREs to the team on-call schedule, monitor their performance, create procedures to deal with incidents, and develop solutions. Managers ensure resilience across all the systems and the DevOps workflows.Managers can perform the following actions within the context of their teams:

-   Define and set up and teams, on-call schedules, and services.
-   Add and delete users such as responders, and managers for the teams the are a part of.
-   Add or manage integrations.
-   Create Integrations with Application Performance Monitoring \(APM\) tools
-   Set up and maintain Reliability Indicators.
-   Set up and maintain Error Budget Policies.

</td><td>

Responder

</td></tr><tr><td>

Responder \[srm\_responder\]

</td><td>

A Service Reliability Engineer \(SRE\) that uses SRM to perform everyday tasks. Responders are the individuals who are on call and diagnose and remediate incidents.

 Responders can only access configurations that they’re a part of. They can only access the alerts or incidents for which they have permissions.

 SREs can perform the following actions, within the context of their teams:

-   Set up services, teams, and integrations
-   Confirm their on-call schedules
-   Manage incident and alert records
-   Update teams that they’ve created
-   Add other responders
-   Create Integrations with Application Performance Monitoring \(APM\) tools
-   Set up and maintain reliability metrics
-   Set up and maintain error budget actions

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
2.  Along with SLO Management, teams have access to implement themselves on SRM to register these services and define service level objectives \(SLO\) to ensure business outcomes. Example: 95% monthly availability for billing portal.
3.  Monitoring integrations are set up by the teams to collect the real-time health of these services. Example: Cloud Observability.
4.  Monitoring creates service level indicator \(SLI\) impacting alerts when services are under-performing. Automation groups and enriches. Example: Billing portal latency is exceeding 7 s.
5.  When the alerts indicate an outage or customer impacting degradation, incidents are created and on-call notifications notify appropriate team resources. Example: A Billing SRE team is notified via phone call of a latency issue on the billing portal.
6.  After incidents are collaboratively diagnosed and remediated, action items for improved resilience are captured. Example: The Billing team decides to add additional web server capacity.
7.  Management continually reviews SLO performance, helps to prevent changes when the error budget is exhausted, and prioritizes improvement initiatives for under-performing services.

## SRM benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Team-based experience|[Working with SRM teams](sr-work-teams.md)|Service Reliability Responder, Manager, and administrator|
|Service registration|[Working with SRM services](sr-work-services.md)|Service Reliability Responder, Manager, and administrator|
|Prebuilt integrations|[Working with SRM integrations](sr-work-integrations.md)|Service Reliability Responder, Manager, and administrator|
|Measure service health|[Working with Reliability metrics](../../slo-management/concept/sr-work-SLI-SLO.md)|Service Reliability Responder, Manager, and administrator|
|On-call coverage|[Create your SRM On-call schedule](../task/sr-create-on-call-schedule.md)|Service Reliability Responder, Manager, and administrator|
|Remediate high severity alerts and incidents|[Working with SRM reliability tasks](../task/sr-work-reliability-tasks.md)|Service Reliability Responder, Manager, and administrator|

## What to explore next

To learn more about configuring and using SRM, see:

-   [Configuring Service Reliability Management](configuring-service-reliability-management.md)
-   [Using Service Reliability Management](using-service-reliability-management.md)
-   [Service Reliability Management reference](../reference/service-reliability-management-reference.md)

-   **[Get started with Service Reliability Management](sr-get-started.md)**  
SRM accelerates your path to viewing service health in the context of service level objectives and incident resolution. Helps IT Operations and DevOps teams deliver on the promise of agility, performance, and uptime.
-   **[SRM alert workspace](../reference/sr-alerts-workspace.md)**  
The alert workspace contains various areas containing alert details and possible actions.
-   **[SRM incident workspace](../reference/sr-incidents-workspace.md)**  
The incident workspace contains various panels containing incident details and possible actions.

**Parent Topic:**[Service Reliability Management](../reference/sr-landing-page.md)

