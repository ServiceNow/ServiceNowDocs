---
title: Exploring SLO Management
description: Service Level Objective Management \(SLO Management\) helps IT services meet customer expectations.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Exploring SLO Management

Service Level Objective Management \(SLO Management\) helps IT services meet customer expectations.

## SLO Management overview

SLO Management is a framework for setting clear expectations and measuring the performance of IT services. It helps organizations deliver consistent services and identify areas for improvement. SLOs define the target service level for a specific service, such as incident resolution or service request fulfillment. Effective SLO management involves setting realistic objectives, monitoring performance, and continuously improving services to meet customer needs.

## SLO Management users

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

SRM administrators can manage account settings, configurations, and users.

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

Managers oversee a team of service reliability engineers \(SREs\). Managers assign SREs to the team on-call schedule, monitor their performance, create procedures to deal with incidents, and develop solutions. Managers help ensure resilience across all the systems and the DevOps workflows.Managers can perform the following actions within the context of their teams:

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

An SRE that uses SRM to perform everyday tasks. Responders are the individuals who are on call and diagnose and remediate incidents.

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
</table>**Note:** If you're using the SLO plugin without SRM, make sure that the required alert and cmdb\_ci read access is granted to team members.

## SLO Management workflow

1.  Define SLOs - Identify critical services and define SLOs based on customer expectations and business requirements.

    **Note:** SLOs can also be generated automatically using the Now Assist SLO creator agent. For details, see [Generating service level objectives](../../now-assist-itom/concept/now-assist-itom-slo-generation.md).

2.  Establish SLIs - Develop Service Level Indicators \(SLIs\) to measure SLO performance.
3.  Monitor and analyze - Track SLI data and analyze performance against SLO targets.
4.  Identify gaps and improve - Determine areas where SLOs aren't being met and implement changes to improve service performance.
5.  Review and refine - Regularly review SLO performance and refine SLOs as needed.

## SLO Management benefits

-   Improved service quality - SLOs help IT services meet customer expectations, leading to increased satisfaction and loyalty.
-   Increased transparency - Clear SLOs provide a shared understanding of service expectations between IT and customers.
-   Better resource allocation - SLOs help prioritize resources and focus on areas that need improvement.
-   Enhanced collaboration - SLO management encourages collaboration between IT teams and customers to achieve common goals.
-   Data-driven decision making - SLO performance data informs decisions and drives continuous service improvement.
-   Automated SLO generation - The SLO creator agent analyzes operational data to generate SLOs, helping teams get started with SLO-based monitoring. For details, see [Generating service level objectives](../../now-assist-itom/concept/now-assist-itom-slo-generation.md).

