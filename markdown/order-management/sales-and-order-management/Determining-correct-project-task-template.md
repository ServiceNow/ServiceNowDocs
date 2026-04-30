---
title: Choosing a project template task when duplicates exist
description: As an admin, when you're configuring the decision rules for domain orders and order tasks, you may find that there are multiple project template tasks with the same Short description. It may be difficult to determine the correct project template task to select.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up project oversight conditions and decision rules, Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Choosing a project template task when duplicates exist

As an admin, when you're configuring the decision rules for domain orders and order tasks, you may find that there are multiple project template tasks with the same Short description. It may be difficult to determine the correct project template task to select.

For example, the following decision table for Project Oversight for Domain Order shows two options with the same name for the project template task: Product Order for SD-WAN Security. This project template task has the same **Short description** for two different project template tasks, one for SD-WAN Package and the other for SD-WAN Customer Product Bundle.

![Decision table for domain order that has two project template task options with the same Short description](../image/proj-mgmt-oversight-dup-template-task.png "Duplicate project template tasks in Project Management Oversight for Domain Order")

You can determine the appropriate project template task by finding and verifying the sys\_id of the project template task to be used. For more information, see [Verify the sys\_id of a project task template](../task/find-sysid-proj-template-task.md).

