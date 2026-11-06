---
title: Managing major incidents
description: A major incident \(MI\) significantly disrupts the business and requires a response beyond the routine incident management process. Major incidents follow a separate procedure with shorter timescales and higher priority to speed up resolution for incidents with high business impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/major-incident-management.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident Management, IT Service Management]
---

# Managing major incidents

A major incident \(MI\) significantly disrupts the business and requires a response beyond the routine incident management process. Major incidents follow a separate procedure with shorter timescales and higher priority to speed up resolution for incidents with high business impact.

\[Omitted video\] Description: Introduction to Major Incident Management

Your organization must define and agree on what constitutes a major incident. For example, a major incident can be created if a critical business service is impacted or if there is a service outage that affects many users.

You can create a major incident candidate in the following ways:

-   Propose an incident as a major incident candidate by selecting **Propose Major Incident** from the context menu of the Incident form. After incident is proposed, the major incident candidate can be promoted to a major incident.
-   Create a major incident candidate by selecting **Create Major Incident Candidate** in the application navigator.
-   Mark an incident as a major incident candidate based on the major incident trigger rules.

**Note:** When a major incident is created from a major incident candidate, the new major incident is the parent record of the major incident candidate. In this case, the **Caller** and **Company** fields are optional.

As a major incident manager, you can do the following:

-   Promote a candidate to a major incident by selecting **Promote to Major Incident** from the context menu.
-   Create a major incident by selecting **Create Major Incident** in the application navigator.
-   Promote an incident to a major incident without going through the proposal process.

When responding to a major incident, key actions include finding the correct resources, communicating updates to stakeholders, setting up conference calls, and escalating the incident when required. Using [Task Communications Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/tcm-landing-page.md), you can define communication plans that are associated with a major incident based on predefined conditions. Incident communication plans and related communication tasks are created for a major incident based on the communication plan definitions. These tasks run as defined in the attached incident communication plan.

-   **[Major Incident Management process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-management-process.md)**  
A major incident is a highest-impact, highest-urgency incident that affects many users, depriving the business of one or more crucial services. The urgency of the situation requires a well-coordinated response process to accelerate the resolution and minimize the business impact.
-   **[Major Incident Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/mim-plugins.md)**  
You can activate the Major Incident Management plugins if you have the admin role.
-   **[Quick start tests for Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/quick-start-tests-mim.md)**  
Validate that Major Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Create trigger rules for major incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-trigger-rules.md)**  
Create trigger rules to define the conditions under which a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.
-   **[Working on major incident management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/work-on-mim.md)**  
Major incident management includes creating major incidents in different ways, rejecting major incident candidates, and demoting or closing major incidents.
-   **[Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-workbench.md)**  
The major incident workbench is a single-pane view for major incident managers, communication managers, and resolver groups. It aggregates actionable information to help these users manage major incidents.
-   **[Legacy: Major incident overview dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/major-incident-overview.md)**  
The Major Incident Overview module provides two versions of the Performance Analytics \(PA\) dashboard for reviewing major incident information at a glance.

**Parent Topic:**[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/c_IncidentManagement.md)

