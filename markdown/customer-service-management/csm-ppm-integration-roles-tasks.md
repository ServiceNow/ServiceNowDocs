---
title: Customer Project Management personas, roles, and tables
description: An overview of the tasks that can be performed by the different Customer Project Management roles.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating with Customer Project Management, Integrate, Customer Service Management]
---

# Customer Project Management personas, roles, and tables

An overview of the tasks that can be performed by the different Customer Project Management roles.

## Personas and roles

The following table lists the personas, their description, and the roles included with them.

<table id="table_isk_pj5_fkb"><thead><tr><th>

Persona

</th><th>

Description

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Customer project manager

</td><td>

A user who creates and manages projects for customer accounts. -   Creates projects.
-   Set up project tasks and resource plans.
-   Identifies customer contacts who have access to projects and project tasks.
-   Assigns and manages tasks and dependencies.

</td><td>

-   it\_project\_manager
-   sn\_customerservice.projectmanager

</td></tr><tr><td>

Location Project Member

 \[sn\_bus\_loc.location\_project\_stakeholder\]

</td><td>

Views project details and project tasks of their respective business location. Marks project task as complete.

</td><td>

None

</td></tr><tr><td>

Location Project Manager Contributor

 \[sn\_bus\_loc.location\_manager\_project\_stakeholder\]

</td><td>

Views project details and project tasks of their respective business location and child business locations. Marks project task as complete.

</td><td>

None

</td></tr><tr><td>

Service Organization Project Manager\[sn\_service\_org.project\_manager\]

</td><td>

This role can perform the following actions:-   Project initiation: Creates and launches projects

**Note:** Service Organization project manager and customer project manager can access all project modules.

-   Project planning: Develops project plans, such as, task assignments and resource allocation.

**Note:** On task assignment, an automated mail is generated. Update "Send Email to Contact when Customer Project Task is assigned" flow to disable or enable notifications.

-   Task management: Monitors and manages task dependencies and execution.
-   Coordination: Views and collaborates with location staff, assigning, and tracking tasks of their respective location.

</td><td>

-   sn\_bus\_loc.ibl\_viewer
-   sn\_bus\_loc.ebl\_viewer

</td></tr><tr><td>

Project stakeholder

</td><td>

A user who is responsible for activities that require viewing customer project details and project tasks.

</td><td>

-   sn\_customerservice.projectstakeholder
-   Minimum one CSM role

</td></tr><tr><td>

Customer service agent

</td><td>

A user who can create cases from projects and project tasks and resolve cases within the set SLA.-   work on cases created from projects and project tasks.
-   Communicates with the customer on case status.

</td><td>

-   sn\_customerservice\_agent
-   sn\_customerservice.projectstakeholder

</td></tr><tr><td>

Customer

</td><td>

An external user who is responsible for overseeing the project delivery. -   Review project status and progress on the Customer Service Portal.
-   Completes assigned tasks.
-   Creates cases for project issues.

</td><td>

Any of the following CSM external roles:-   sn\_customerservice.customer
-   sn\_customerservice.customer\_admin
-   sn\_customerservice.partner
-   sn\_customerservice.partner\_admin

</td></tr></tbody>
</table>## Tables

Tables are added with activation of the Customer Project Management plugin.

<table id="table_udf_cmc_kt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Project\[customer\_project\]

</td><td>

Stores customer projects.

</td></tr><tr><td>

Customer Project Task\[customer\_project\_task\]

</td><td>

Stores customer project tasks

</td></tr><tr><td>

Project Contact\[project\_contact\]

</td><td>

Stores project contacts.

</td></tr></tbody>
</table>The following columns are added to the Case table:

-   Customer Project
-   Customer Project Task
-   Issue
-   Project Change Request

