---
title: Manage costs
description: When the cost management feature is enabled, time cards can be used to manage the cost of labor in the Cost Management application.
locale: en-US
release: xanadu
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage costs

When the cost management feature is enabled, time cards can be used to manage the cost of labor in the Cost Management application.

When a time card for a project task is approved, an expense line is generated for the corresponding labor cost associated with the project. If the project has a [Rate Models](../../../product/project-portfolio-suite-with-financials/concept/rate-model.md) associated, then the hourly rate for calculating labor cost for the expense lines is derived from the rate model. If no rate model is associated to the project, the rate listed in the Labor Rate Card is considered. If no Labor Rate Cards is applicable, the property com.snc.time\_card.default\_rate defines the default hourly rate.

## Roles

The timecard\_admin role enables users to approve, modify, and delete the time cards of other users.

**Parent Topic:**[Time Card Management](time-card-management.md)

**Related topics**  


[Activate Cost Management](../../../product/cost-management/task/t_ActivatingCostManagement.md)

