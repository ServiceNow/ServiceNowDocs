---
title: HR Service Delivery Employee Relations assignment rules
description: HR Service Delivery employee relations assignment rules allow you to automatically assign a group to ER cases when the assignment group is empty.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery Employee Relations assignment rules

HR Service Delivery employee relations assignment rules allow you to automatically assign a group to ER cases when the assignment group is empty.

When the HR case template sets the assignment group, assignment rules are ignored.

When an ER case is created, it:

-   Checks for the Skills/Assignment group from the HR Case Template for the associated HR service. See [Configure an HR case template for an HR service](../task/configure-hr-case-template.md).
-   If there is no assignment group for the HR case template, the base system provides the Employee Relations Case assignment rule.
-   The Employee Relations Case assignment rule assigns the Employee Relations group to the case.

**Note:** For more information, see [Add or modify an HR assignment rule](../task/t_CreatingAnAssignmentRule.md).

