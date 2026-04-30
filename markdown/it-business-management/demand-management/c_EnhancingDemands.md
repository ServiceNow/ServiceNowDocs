---
title: Add details to demands
description: The demand manager typically works with a business relationship manager to identify stakeholders and elicit requirements, risks, and other important information.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add details to demands

The demand manager typically works with a business relationship manager to identify stakeholders and elicit requirements, risks, and other important information.

The Demand Management application streamlines the stakeholder identification process. Auto-populating the list of stakeholders from the portfolio the user selects when filling out the demand form in the service catalog or in the Demand Management application. The Demand Management application also enables you to use assessments to automate some of the information gathering process.

## Add demand tasks

Demand managers analyze business demands, approve demands, and create projects and enhancements. Many times activities such as effort, cost, risk, and benefit estimates are required to analyze a demand and create a business case for approval of the demand. A demand manager can create demand tasks and assign these tasks to individual resources or a group to perform these activities.

The resources assigned to the demand tasks then post time spent while working on a demand or demand task using a time card. The time card data is used to calculate actual effort and cost incurred on the demand task as well as demand.

To [create demand tasks](../task/create-demand-task.md), scroll to the **Demand Tasks** related list on the Demand form and select **New** to create a record.

## Add stakeholders

When a demand is submitted, the demand stakeholder list is populated automatically from the associated portfolio. You can also add stakeholders. To add a person to the stakeholder list, scroll to the Stakeholders related list on the Demand form, select **Create new** to create a record, and fill in the form. To add existing stakeholders to the demand, select **Add existing**.

When adding a stakeholder from the demand form, the **Portfolio** field displays the portfolio that was selected on the Demand form.

A demand can have multiple stakeholders and a stakeholder can be associated with multiple demands.

The newly added stakeholder is automatically associated with the current demand and any other demands that use the same portfolio.

## Add requirements

Demand managers can create as many requirements as needed, but requirements aren’t required. Typically, the stakeholders associated with a demand request have insights into what the requirements are for a demand request to be completed.

Demand managers use the Requirement form to describe the requirement and assign an owner who is responsible for making sure that the requirement is met. When a requirement is complex, demand managers can associate planned tasks, such as project tasks, with the requirement. The demand manager assigns and tracks the tasks until they’re complete.

To add a requirement to a demand, follow these steps:

1.  Open a Demand form and select **New** from the Requirements related list.
2.  On the Requirement form, fill in the fields. For a description of the field names, see [Requirement form](../reference/requirement-form.md).

## Add resource assignments

Resource assignments are another source of information that decision makers can use when evaluating demands. You can create resource assignments for a demand from the **Resource assignments** related list, which appears only if the Resource Management Workspace application is activated.

To [add a resource assignment to the demand](../task/create-manage-resource-plans-demand.md), scroll to the Resource assignments related list on the Demand form and select **New** to create a record.

## Add and recalculate strategy and goal allocations

The Strategy Allocations related list displays the percentage of the demand's total cost and benefits allocated toward the achievement of the associated strategies. The Goal Allocations related list displays the percentage of demand's total cost and benefits allocated toward achievement of goals associated with the demand. For more information, see [Allocate or modify the strategy and goal percentage for a demand](../../itbm-business-outcomes/task/associate-goal-strategy-dmd.md).

Recalculate and update cost field values in the Strategy and Goal Allocation tabs. Use the Recalculate Strategy and Goal Allocation related link to update the demand's total cost and benefits when strategy and goal allocations for the demand are changed. For more information, see [Strategic Spend Tracking for PPM](../../itbm-business-outcomes/concept/ppm-strategic-spend-tracking-overview.md).

**Note:** These related lists and related links appears only when [Strategic Spend Tracking for PPM](../../itbm-business-outcomes/concept/ppm-strategic-spend-tracking-overview.md) is installed. This application is available on ServiceNow Store. You must switch to the **Strategic Alignment** view to see them. If these lists and links aren’t available on the form view that you’re using, ask your administrator to configure the demand form to add them. For more information, see [Install Strategic Spend Tracking for PPM](../../itbm-business-outcomes/task/install-strategic-spend.md).

## Add goal/target relationships

The Goal/Target Relationships related list displays the relationship between a goal and a planning item, strategic item, or any other item such as a demand.

## Allocate funds

If your demand represents a significant, multi-year investment and you must distribute funding across related work, you can allocate funds from your demand. By allocating funds, you can directly support one or more projects, epics, or programs linked to the approved demand.

This link appears only if you have the [Investment Funding](../../investment-funding/task/activate-investment-funding.md) plugin activated, an existing corresponding investment record for this demand, and the investment\_user role.

**Parent Topic:**[Use Demand Management](../reference/r_UsingDemandManagement.md)

**Related topics**  


[Assess demands](c_AssessingDemands.md)

[Create a demand](../task/t_CreatingDemands.md)

[View demands](../task/t_ViewDemands.md)

[RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records for a demand](ridac-entries-for-demand.md)

[Reset a demand to Draft state](../task/reset-demand-to-draft-state.md)

[Delete demands](../task/t_DeletingDemands.md)

[Move and resize a demand](../task/t_MoveAndResizeADemand.md)

[Train the similarity solution for Demand Management to find similar demands](../task/train-similarity-solution-dm.md)

[Identify similar records using Now Assist for Strategic Portfolio Management \(SPM\)](../task/identify-similar-demands.md)

[Associate AI systems with demands](../task/associate-ai-systems-with-demands.md)

[Summarize demands with demand summarization skill](../task/demand-summary-demand-classic.md)

