---
title: Managing major incidents
description: A major incident \(MI\) is an incident that results in significant disruption to the business. A major incident demands a response beyond the routine incident management process. Major incidents have a separate procedure with shorter timescales and higher priority, so that there is a faster resolution process for incidents with high business impact.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Incident Management, IT Service Management]
---

# Managing major incidents

A major incident \(MI\) is an incident that results in significant disruption to the business. A major incident demands a response beyond the routine incident management process. Major incidents have a separate procedure with shorter timescales and higher priority, so that there is a faster resolution process for incidents with high business impact.

Introduction to Major Incident Management 

The definition of what constitutes a major incident must be determined and agreed on. For example, a major incident can be created if a critical business service is impacted or if there is a service outage that affects many users.

There are multiple ways to create a major incident candidate, such as the following:

-   Propose an incident as a major incident candidate by clicking **Propose Major Incident** from the context menu of the Incident form.
-   Create a new major incident candidate by clicking **Create Major Incident Candidate** from the left navigation pane.
-   Mark an incident as a major incident candidate based on the major incident trigger rules.

**Note:** When a major incident is created from a major incident candidate, the new major incident is considered as a parent record for the current major incident candidate. In such case, the **Caller** and **Company** fields are optional.

As a major incident manager, you can do the following:

-   Promote a candidate to a major incident by clicking **Promote to Major Incident** from the context menu.
-   Create a new major incident by clicking **Create Major Incident** from the left navigation pane.
-   Promote an incident to a major incident without going through the proposal process.

When responding to a major incident, some crucial actions involve finding the right resources, communicating updates to users and stakeholders, setting up conference calls to investigate and resolve the incident, and escalating the incident when required. Using [Task Communications Management](https://www.servicenow.com/docs/access?context=tcm-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US), you can define communication plans that are associated with a major incident based on pre-defined conditions. Incident communication plans and related communication tasks are created for a major incident based on the communication plan definitions. Thereafter, tasks get executed as defined in the attached incident communication.

-   **[Major Incident Management process](major-incident-management-process.md)**  
A major incident is a highest-impact, highest-urgency incident that affects a large number of users, depriving the business of one or more crucial services. Given the urgency of the situation, a well-coordinated response process is required to accelerate the resolution and minimize the business impact.
-   **[Major Incident Management plugins](mim-plugins.md)**  
You can activate the Major Incident Management plugins if you have the admin role.
-   **[Quick start tests for Major Incident Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-mim.md)**  
Validate that Major Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Create trigger rules for major incidents](../task/major-incident-trigger-rules.md)**  
Create trigger rules to define the conditions under which a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.
-   **[Working on major incident management](work-on-mim.md)**  
The section covers topics that help you with a variety of technical concepts related to major incident management such as the different ways to create a major incident, ways to reject a major incident candidate, demote a major incident, or close a major incident.
-   **[Major incident workbench](major-incident-workbench.md)**  
The major incident workbench is a single pane view designed for major incident managers, communication managers, and resolver groups. The workbench helps to manage major incidents by aggregating and providing actionable information.
-   **[Legacy: Major incident overview dashboard](major-incident-overview.md)**  
Major Incident Overview module provides two versions of the Performance Analytics \(PA\) Dashboard to review major incident information at a glance.

**Parent Topic:**[Incident Management](c_IncidentManagement.md)

