---
title: Customer Project Management personas, roles, and tables
description: An overview of the tasks that can be performed by the different Customer Project Management roles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating with Customer Project Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Customer Project Management personas, roles, and tables

An overview of the tasks that can be performed by the different Customer Project Management roles.

## Personas and roles

The following table lists the personas, their description and the roles included with them.

<table id="table_isk_pj5_fkb"><thead><tr><th>

Persona

</th><th>

Description

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Customer project manager

</td><td>

A user who creates and manages projects for customer accounts. -   Creates new projects.
-   Sets up project tasks and resource plans.
-   Identifies customer contacts who have access to projects and project tasks.
-   Assigns and manages tasks and dependencies.

</td><td>

-   it\_project\_manager
-   sn\_customerservice.projectmanager

</td></tr><tr><td>

Project stakeholder

</td><td>

A user who is responsible for activities that require viewing customer project details and project tasks.

</td><td>

-   sn\_customerservice.projectstakeholder
-   At least one CSM role

</td></tr><tr><td>

Customer service agent

</td><td>

A user who can create cases from projects and project tasks and resolve cases within the set SLA.-   Works on cases created from projects and project tasks.
-   Communicates with the customer on case status.

</td><td>

-   sn\_customerservice\_agent
-   sn\_customerservice.projectstakeholder

</td></tr><tr><td>

Customer

</td><td>

An external user who is responsible for overseeing the project delivery. -   Reviews project status and progress on the Customer Service Portal.
-   Completes assigned tasks.
-   Creates cases for project issues.

</td><td>

Any of the following CSM external roles:-   sn\_customerservice.customer
-   sn\_customerservice.customer\_admin
-   sn\_customerservice.partner
-   sn\_customerservice.partner\_admin

</td></tr></tbody>
</table>## Tables

Tables are added with activation of Customer Service Management.

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

