---
title: Demand default playbook stages and activities
description: The default demand playbook includes certain predefined stages and activities. These activities guide you through the demand life-cycle, from capturing the initial brief to completing the demand.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 5
breadcrumb: [Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Demand default playbook stages and activities

The default demand playbook includes certain predefined stages and activities. These activities guide you through the demand life-cycle, from capturing the initial brief to completing the demand.

![The stages of a demand AI playbook.](../images/ppw-ai-checkpoint-playbook-stage.png)

## Create demand brief

In this stage, capture the foundational information for the demand including the business justification, risks, and assumptions.

|Activity|Type|Description|
|--------|----|-----------|
|Define demand details|Form|Enter the demand name, description, and business case. For more information, see [Demand form](demand-form-ppw.md).|
|Document risks and assumptions|Form|Document the risk of not performing the demand and any assumptions. For more information, see [Demand form](demand-form-ppw.md).|
|The demand state will be moved to submitted|Automated|Completing the previous activities advances the demand to the next state in its life-cycle.|

## Define demand alignment

In this stage, align the demand with organizational goals, stakeholders, and team members.

<table id="table_pwx_5xm_g3c"><thead><tr><th>

Activity

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define business alignment

</td><td>

Form

</td><td>

Define the business classification for the demand. For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Define strategic alignment

</td><td>

Form

</td><td>

Define how the demand aligns with the organization's strategic objectives. For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Add secondary goals

</td><td>

Related list

</td><td>

Associate secondary goals and targets with the demand. -   You can also add a goal or target relationship.
-   You can view the details of an entry by selecting it from the list.

For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Update demand dates

</td><td>

Form

</td><td>

Specify or update the planned dates for the demand. For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Add collaborators

</td><td>

Form

</td><td>

Add collaborators to the demand and indicate whether an assessment is required. For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Add stakeholders

</td><td>

Related list

</td><td>

Add stakeholders associated with the demand.You can view the details of an entry by selecting it from the list. For more information, see [Create stakeholder form](create-stakeholder-form-ppw.md).

</td></tr><tr><td>

Add demand tasks

</td><td>

Related list

</td><td>

Create demand tasks to break down initial planning activities. For more information, see [Create demand task form](create-demand-task-form-ppw.md).

</td></tr><tr><td>

Update EAP details

</td><td>

Form

</td><td>

Update the **Team** field for the Enterprise Agile Planning \(EAP\) entity, to which the demand is converted.**Note:** This activity is available if the **Type** field is an EAP entity.

</td></tr><tr><td>

The demand state will be moved to screening

</td><td>

Automated

</td><td>

Completing the previous activities advances the demand to the next state in its life-cycle.

</td></tr></tbody>
</table>## Estimate demand cost and effort

In this stage, evaluate the financial and resource requirements for the demand.

<table id="table_ndg_c1n_g3c"><thead><tr><th>

Activity

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update assessment details

</td><td>

Form

</td><td>

Update the assessment information for the demand. For more information, see [Demand form](demand-form-ppw.md).

</td></tr><tr><td>

Estimate financial cost

</td><td>

Related list

</td><td>

View and manage cost plans associated with the demand. -   You can add a cost plan or delete an existing one.
-   You can view the details of an entry by selecting it from the list.

For more information, see [Create cost plan form](create-cost-plan-form-ppw.md).

</td></tr><tr><td>

Estimate resource requirements

</td><td>

Related list

</td><td>

View and manage resource assignments for the demand.You can view the details of an entry by selecting it from the list.

For more information, see [Create resource assignment form](create-resource-assignment-form-ppw.md).

</td></tr><tr><td>

Define benefit estimates

</td><td>

Related list

</td><td>

View and manage benefit plans for the demand.-   You can add a benefit plan or delete an existing one.
-   You can view the details of an entry by selecting it from the list.

For more information, see [Monetary benefit plan form](monetary-benefit-plan-form-ppw.md) and [Non-monetary benefit plan form](non-monetary-benefit-plan-form-ppw.md).

</td></tr><tr><td>

Cost estimates

</td><td>

Form

</td><td>

Review or update the cost estimate details for the demand.

</td></tr><tr><td>

The demand state will be moved to qualified

</td><td>

Automated

</td><td>

Completing the previous activities advances the demand to the next state in its life-cycle.

</td></tr></tbody>
</table>## AI checkpoint

In this stage, associate AI systems with the demand to identify potential AI impacts.

**Note:** If the AI Control Tower plugin is installed and the investment type of the demand is set to artificial intelligence, the AI checkpoint stage is available for playbooks.

|Activity|Type|Description|
|--------|----|-----------|
|Associate AI systems|Form|Add AI systems to the demand by selecting from the existing systems. To link existing systems, use the **Product** and **Impacted AI systems** fields.|

## Confirm demand readiness for review

In this stage, verify that the demand is complete and ready for approval.

|Activity|Type|Description|
|--------|----|-----------|
|Align demand and assign portfolio/program|Form|Review the demand details and confirm readiness for the approval process.|
|The demand state will be moved to approved|Automated|Completing the previous activities advances the demand to the next state in its life-cycle.|

## Approve and finalize demand

In this stage, confirm the demand details and convert the demand to a work entity.

|Activity|Type|Description|
|--------|----|-----------|
|Confirm details and convert to selected entity|Form|Review the selected work entity type, such as project or enhancement, and the approved timeline.|

## Complete demand

This stage is the final stage of the demand workflow.

|Activity|Type|Description|
|--------|----|-----------|
|Review the converted entity|Form|Review the work entity created from the demand to verify that the conversion is complete.|

**Related topics**  


[Playbooks in Next Experience for Demand Management](../concept/playbooks-in-demand-workspace-ppw.md)

[Create and customize playbooks](../task/create-and-customize-playbooks-ppw.md)

[Use Playbooks](../task/use-playbooks-in-ppw.md)

