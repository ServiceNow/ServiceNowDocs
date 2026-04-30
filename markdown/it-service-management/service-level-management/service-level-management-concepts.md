---
title: Service Level Management concepts
description: The ServiceNow Service Level Management \(SLM\) application facilitates you to oversee and control the services within the organization.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Service Level Management, Service Level Management, IT Service Management]
---

# Service Level Management concepts

The ServiceNow® Service Level Management \(SLM\) application facilitates you to oversee and control the services within the organization.

Service Level Managers are responsible for a set of agreements between a service provider and customer that define the scope, quality, and speed of the services being provided. The intention of SLM is to provide the customer with an expectation of service within a known timescale and the ability to monitor when service levels are not being met.

The SLM offers the following features:

-   Service Level Agreement \(SLA\) definitions
-   Task SLAs
-   Integration with other ServiceNow plugins

## Service Level Agreement \(SLA\) roles

Ensure that users can perform all necessary actions by assigning SLA roles.

|Role|Definition|
|----|----------|
|sla\_admin|Provides full administrative rights to SLM. Users that possess the sla\_admin role can configure SLM properties, run SLA repair, view the SLA Overview dashboard, and manage SLA definitions. They may associate existing workflows or schedules to SLA definitions, but are unable to create workflows. The additional roles required to create workflows or schedules must be granted explicitly. See [Base system roles](https://www.servicenow.com/docs/access?context=r_BaseSystemRoles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.|
|sla\_manager|Lets users define SLA definitions, view SLA repair logs, and view the SLA Overview dashboard. Does not let users change SLM property values or define SLA condition types.|

## Service Level Agreement \(SLA\) definitions

Use the SLA Definition record to define a specific set of criteria that would result in an SLA being generated. Define some of the following parameters:

-   Table: The task table that the SLA is defined for.
-   Duration: The time duration in which the service must be provided to the customer.
-   Schedule: The schedule, which indicates valid working and non-working days that the service provider follows to deliver the service. The selected schedule is used to determine when the SLA breaches.
-   Conditions: The conditions under which the SLA starts, pauses, stops, or resets.

## Task SLA definitions

When an SLA definition is triggered against a particular task, the task SLA record is generated and contains all the tracking data for the specific SLA on that record. For example, if an SLA definition exists for P1 incidents a task SLA record attaches to the P1 incident record and captures all the data associated with it. Often there are multiple task SLA records against a single task because many definitions apply.

**Note:** This feature is available only in new instances starting with Jakarta or a later release. The Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\) plugin must be activate.

On the Task SLA form, you can also select the target for the SLA: **Response**, **Resolution**, or **None**.

## Integration with other ServiceNow plugins

The following plugins introduce extra functionality within SLM:

-   SLA Contract Add-on
-   Service Portfolio Management - SLA Commitments

## SLM Template support in App Engine Studio

Application Templates support Service Level Management tables to be included when creating templates from applications in the App Engine Studio. The SLM tables that can be included in templates are:

-   SLA Definition \[contract\_sla\]
-   Service Offering SLA \[service\_offering\_sla\]
-   SLA Timer Configuration\[sla\_timer\_config\]
-   SLA timer configuration mapping\[sla\_timer\_config\_mapping\]

**Parent Topic:**[Exploring Service Level Management](exploring-slm.md)

