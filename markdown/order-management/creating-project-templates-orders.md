---
title: Creating project templates and project template tasks
description: You create the project templates and project template tasks that Order Management uses to instantiate projects for order lines and associated domain orders and order tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Creating project templates and project template tasks

You create the project templates and project template tasks that Order Management uses to instantiate projects for order lines and associated domain orders and order tasks.

In the SPM integration, project templates define the structure of a project for order lines and the project planned tasks that map to the order fulfillment tasks for the order line. You specify project templates and project template tasks in the project oversight decision rules. Order Management uses these rules to determine which order items require oversight and the project template or project template tasks used to create the projects.

As an admin or user with the it\_project\_manager role, you create project templates and the project template tasks in Project Portfolio Management. For more information, see [Project templates](https://www.servicenow.com/docs/access?context=c_ProjectTemplates&version=australia&pubname=australia-it-business-management&ft:locale=en-US) and [Create a project template](https://www.servicenow.com/docs/access?context=t_ViewAProjectTemplateForm&version=australia&pubname=australia-it-business-management&ft:locale=en-US). The demo data with the Order Management application includes project templates that you can copy and change as needed.

**Note:** When you create project template tasks for domain orders and order tasks, be sure to anticipate inflight changes that may require additional planned tasks. Define those potential planned tasks in the template tasks so that the system can synchronize the planned tasks with the additional order tasks resulting from inflight changes in Order Management.

## Before creating project templates and project template tasks

Before you create your project template and project task templates for the SPM integration, consider the level of project oversight required for customer orders to be fulfilled. For example, in the following SD-WAN fulfillment flow, the top order line is SD-WAN Service Package, which defines the order line project to be created. Next, identify the domain orders and then the order tasks that require project task oversight.

