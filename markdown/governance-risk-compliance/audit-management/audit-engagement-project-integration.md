---
title: Roll up expenses and resources in an engagement
description: Any audit project has associated costs, budgets, and resources. Roll ups of these costs, budgets, and resources enable the audit manager to view the entire costs and resources in a consolidated manner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/audit-engagement-project-integration.html
release: brazil
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Audit Management overview, Audit Management, Governance, Risk, and Compliance]
---

# Roll up expenses and resources in an engagement

Any audit project has associated costs, budgets, and resources. Roll ups of these costs, budgets, and resources enable the audit manager to view the entire costs and resources in a consolidated manner.

Starting with the new release, a new plugin called Advanced Audit has been introduced in the Audit Management application. When you activate the Advanced Audit plugin and install the Project Portfolio Management application, you can utilize the project management capabilities to automatically create engagement projects.

When an audit plan is created, the audit manager must be able to view the complete expenses and the resources involved in the engagement. Activating the Advanced Audit plugin enables the rollup of the expenses and resources cost of all engagements for a consolidated view. You can also use the advanced planning capabilities to automatically roll up the expenses and resources of each individual engagement to the parent plan of the engagements.

## Project budget rollup

After an engagement project is automatically created, if the user has the it\_portfolio\_manager role, the user can create a project budget. When a budget is created, the budget cost gets copied over to the **Budgeted expenses** field of the engagement from the engagement project. When you use the advanced planning capabilities to automatically create a plan, the values in the expenses and the resources field are rolled up. These values come from the associated engagements and the engagement projects. To allocate a project budget, see [Allocate budget to a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/allocate-budget-to-project.md). If you allocate a project budget, then the data from the budget cost field gets copied over to the engagement. For example, assume you have an engagement where the budget expense is $100. You can create a project budget for the engagement project with a budget cost of $200. The original budget expense is overwritten. The engagement budget expense is replaced by $200.

## Actual expenses and resources rollup

If actual effort is updated on an engagement project, then that value gets copied over to actual resources on the engagement. The **Actual resources** and **Actual expenses** both are copied over from the **Actual effort** and **Actual cost** fields.

## Resource plan rollup

With Project Portfolio Management, you can add resource plans and cost plans to an engagement. To learn how to create an engagement with advanced planning, see [Create an engagement with advanced planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/creating-an-engagement-with-advance-planning.md)

After you create a resource plan in the **Allocated** state, confirmed and allocated hours are summed in the planned resources on the engagement project.

The **Planned resources** field on the engagement form becomes read-only. The values get automatically rolled up. You cannot manually enter hours in the **Planned resources** field. To manually enter hours in the **Planned resources** field, you must delete the resource plan that you have created.

## Cost plan rollup

If you create an independent cost plan that is not created as a result of a resource plan, the **Planned expenses** field on the engagement form becomes read-only. You cannot manually enter values in this field. You can still edit the **Planned resources** field.

