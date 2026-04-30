---
title: Major Incident Management in Service Operations Workspace
description: Create and manage major incidents in Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Incident Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Major Incident Management in Service Operations Workspace

Create and manage major incidents in Service Operations Workspace.

## Major Incident Management overview

Introduction to Major Incident Management in Service Operations Workspace 

![Major incident record](../image/mim_sow_record_page_new.png.png "Major incident record")

A major incident \(MI\) is created when an issue occurs that results in significant disruption to the business and demands a response beyond the normal incident management process.

Major incidents have a separate procedure with shorter timescales and higher priorities to encourage a faster resolution process for the incidents with a high business impact.

The definition of what constitutes a major incident must be determined based on your requirements. For example, a major incident can be created if a critical business service is impacted or if there’s a service outage that affects many users.

## Major incident user roles

The major incident manager \(major\_incident\_manager\) user role is available in the base system and enables you to manage and resolve major incidents. As a major incident manager, you can do the following:

-   Promote a major incident candidate to a major incident.
-   Create a major incident.
-   Directly promote an incident to a major incident without going through the proposal process.

## Major incident creation

A major incident is created or promoted from a major incident candidate. A major incident candidate can be created from the incident record page in Service Operations Workspace in the following ways:

-   Propose an incident as a major incident candidate.
-   Create a major incident candidate.
-   Use major incident trigger rules to propose an incident as a major incident candidate or promote directly to a major incident automatically.

## Major incident response and handling

When responding to a major incident, some crucial actions include the following:

-   Finding the correct resources
-   Communicating updates to users and stakeholders
-   Setting up conference calls to investigate and resolve the incident
-   Escalating the incident when required

You must define the communication plans that are associated with a major incident based on pre-defined conditions. Incident communication plans and related communication tasks are created for a major incident based on the communication plan definitions. Afterwards, tasks get executed as defined in the associated incident communication.

-   **[Major Incident Management process in Service Operations Workspace](mim-process-sow.md)**  
A major incident has a high impact and urgency that affects a large number of users and deprives the business of one or more crucial services. Given the urgency of the situation, a well-coordinated response process is required to accelerate the resolution and minimize the business impact.
-   **[Managing a major incident record](managing-major-incident-sow.md)**  
Manage a major incident record with a playbook or the various tabs on the major incident record page.

**Parent Topic:**[Incident Management in Service Operations Workspace](incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace](../task/create-incident-sow.md)

[View and update incident information on the Overview tab](../task/view-update-inc-overview-tab.md)

[Viewing incident record information using the Contextual side panel](view-inc-record-info-contextual-sidepanel.md)

[Work on an incident in Service Operations Workspace](../task/work-on-incident-sow.md)

[Remedial actions using Playbook](remedial-actions-playbook.md)

