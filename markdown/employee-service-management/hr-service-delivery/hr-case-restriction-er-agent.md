---
title: HR for HR Security
description: Even Employee Relations agents with privileges to view and modify an ER case are limited from viewing, modifying, or restricting and ER case under certain circumstances for security purposes.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee Relations case restrictions, Configuring Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR for HR Security

Even Employee Relations agents with privileges to view and modify an ER case are limited from viewing, modifying, or restricting and ER case under certain circumstances for security purposes.

Restrictions are enabled for the Employee Relations agent in the following areas of the ServiceNow instance:

## Limited access

When an ER agent is **Subject Person**, or **Opened for**, or **Complainant** on the ER case:

-   **View**

    Can view only the self-service view of the ER case on Agent Workspace, the platform view, and the Employee Center that are available to regular employees. The agent cannot change the view.

-   **UI actions**

    Actions on the ER case that are available to regular employees are also available to the ER agent.

-   **Access to related lists and records**

    No access to the related lists and related records for an ER case, for example, allegations, involved parties, interviews, evidence, and so on. The agent cannot access the related records in the platform view.

-   **Access to Tasks**

    Can view only the assigned tasks and not tasks assigned to other employees.


## No access

When an ER agent is either **Subject of Allegation**, or **Witness** on the ER case, the ER agent will not have any access to that ER case.

