---
title: Demand workflow playbook stages
description: The default demand workflow playbook includes predefined stages and activities that guide you through the demand life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/portfolio-planning/demand-default-playbook-stages-activities-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 10
breadcrumb: [Playbooks in Next Experience for Demand Management, Manage demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Demand workflow playbook stages

The default demand workflow playbook includes predefined stages and activities that guide you through the demand life cycle.

## Overview of the stages

The demand workflow playbook is the only predefined playbook for demands. When the AI Control Tower Core plugin is installed, the demand workflow playbook includes an additional AI checkpoint stage after the Estimate demand cost and effort stage.

The playbook consists of seven stages, including the AI checkpoint stage. These stages contain certain activities that consist of forms and related lists. You can view the details of an entry by selecting it from the list. All mandatory form fields in an activity must be filled to mark it as complete. Any activity in any stage can be skipped. To enable the following activities, an activity can be marked as complete or skipped. After an activity is enabled, you can return to it at any time and restart it. If you restart an activity, you must complete or skip it and all subsequent activities. You can also restart a playbook, but all information is lost.

**Note:** The options to add and delete entries in a related list are available only when the playbook uses the Demand Playbook Experience. For more information, see [Demand playbook experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

Example scenario: The examples in this topic follow a single demand through the playbook. A customer service team requests self-service order tracking in the customer portal, including an AI chatbot that answers order questions. The demand is named Customer portal order tracking.

## Create demand brief

This stage captures the foundational information for the demand, including the business justification, risks, and assumptions. Capture what the demand is and why it is needed, including the business case, risks, and assumptions.

\[Omitted image "demand-playbook1.png"\] Alt text: The Define demand details activity in the Create demand brief stage.

<table id="table_hnz_jxm_g3c"><thead><tr><th>

Activity

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define demand details

</td><td>

Form

</td><td>

In this activity, provide the demand name, description, and business case. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md). For example, for a demand for customer portal order tracking:

-   Name: Customer portal order tracking
-   Description: Let customers check order status and delivery dates in the portal
-   Business case: Reduce order-status calls to the support center

</td></tr><tr><td>

Document risks and assumptions

</td><td>

Form

</td><td>

Document the risk of not performing the demand and any assumptions. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).For example:

-   Risk of not performing: Support call volume keeps growing during peak season without self-service tracking
-   Assumptions: The order management system provides delivery status through an API

</td></tr><tr><td>

The demand state will be moved to submitted

</td><td>

Automated

</td><td>

When you complete the previous activities, the playbook moves the demand to the **Submitted** state if the conditions for the state change are met. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

</td></tr></tbody>
</table>Complete the mandatory form fields to mark this stage as complete. Any demand user with the it\_demand\_user role can complete this stage and submit the demand. The remaining stages must be filled by a user with the it\_demand\_manager role and only they can advance the demand.

## Define demand alignment

This stage aligns the demand with organizational goals, stakeholders, and team members. Connect the demand to business classification, strategic goals, dates, and the people who collaborate on or assess it.

\[Omitted image "demand-playbook2.png"\] Alt text: The Define business alignment activity in the Define demand alignment stage.

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

Define the business classification for the demand such as its category and type. In this activity, you can specify the investment class, investment type and define the priority of the demand. You can also choose how you want to close the demand record. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).

</td></tr><tr><td>

Define strategic alignment

</td><td>

Form

</td><td>

Define how the demand aligns with the organization's strategic objectives. When you select a primary goal, the associated strategic priority is populated automatically. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).

</td></tr><tr><td>

Add secondary goals

</td><td>

Related list

</td><td>

Associate secondary goals and targets with the demand. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).For example:

-   Goal: Reduce support costs
-   Target: Fewer order-status calls each quarter

</td></tr><tr><td>

Update demand dates

</td><td>

Form

</td><td>

Specify or update the approved and planned dates for the demand. If the approved dates aren't available, specify the tentative planned dates. Set both the planned start date and the planned end date, because the **Resources** tab of the demand displays resourcing only after both dates are set. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).

</td></tr><tr><td>

Add collaborators

</td><td>

Form

</td><td>

Add collaborators to the demand and indicate whether an assessment is required. If the **Assessment required** check box is selected, assessments are triggered when the demand moves to the Screening state. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).For example, the portal product owner and the support center manager as collaborators.

</td></tr><tr><td>

Add stakeholders

</td><td>

Related list

</td><td>

Add stakeholders associated with the demand. When the assessments are triggered, they are sent to the stakeholders for completion. For more information, see [Demand stakeholder form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-stakeholder-form-ppw.md).For example, the vice president of customer service as a stakeholder.

</td></tr><tr><td>

Add demand tasks

</td><td>

Related list

</td><td>

Create demand tasks to break down initial planning activities. For more information, see [Demand task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-demand-task-form-ppw.md).For example, a task for the integration architect to confirm that the order management API returns delivery status.

</td></tr><tr><td>

Update EAP details

</td><td>

Form

</td><td>

Update the **Team** field for the Enterprise Agile Planning \(EAP\) entity, to which the demand is converted.**Note:** This activity is available if the **Type** field is selected as an EAP entity.

</td></tr><tr><td>

The demand state will be moved to screening

</td><td>

Automated

</td><td>

When you complete the previous activities, the playbook moves the demand to the **Screening** state if the conditions for the state change are met. Only users with the it\_demand\_manager role can move a demand to the **Screening** state. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

</td></tr></tbody>
</table>## Estimate demand cost and effort

This stage evaluates the financial and resource requirements for the demand. Estimate the cost, resources, and benefits of the demand, and review the assessment scores.

\[Omitted image "demand-playbook3.png"\] Alt text: The Update assessment details activity in the Estimate demand cost and effort stage.

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

Update the assessment information for the demand. The score is populated from the assessments taken by the stakeholders. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).

</td></tr><tr><td>

Estimate financial cost

</td><td>

Related list

</td><td>

View and manage cost plans associated with the demand. For more information, see [Cost plan form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-cost-plan-form-ppw.md).For example, one cost plan for external development services and another for chatbot licensing.

</td></tr><tr><td>

Estimate resource requirements

</td><td>

Related list

</td><td>

View and manage resource assignments for the demand. For more information, see [Resource assignment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-resource-assignment-form-ppw.md).For example, resource assignments for two portal developers and one quality engineer for three months.

</td></tr><tr><td>

Define benefit estimates

</td><td>

Related list

</td><td>

View and manage benefit plans, both monetary and non-monetary, for the demand. For more information, see [Monetary benefit plan form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/monetary-benefit-plan-form-ppw.md) and [Non-monetary benefit plan form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/non-monetary-benefit-plan-form-ppw.md).For example, a monetary benefit plan for lower support staffing costs and a non-monetary benefit plan for improved customer satisfaction.

</td></tr><tr><td>

Cost estimates

</td><td>

Form

</td><td>

Review or update the cost estimate details for the demand. You can select a rate model or provide the discount rate. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).

</td></tr><tr><td>

The demand state will be moved to qualified

</td><td>

Automated

</td><td>

When you complete the previous activities, the playbook moves the demand to the **Qualified** state if the conditions for the state change are met. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

</td></tr></tbody>
</table>## AI checkpoint

This stage associates AI systems with the demand so that AI impacts are identified before the demand is approved. Identify the AI systems that the demand creates or affects so that AI impacts are known before the demand is approved.

**Note:** If the AI Control Tower Core plugin is installed, the AI checkpoint stage is available for the demand workflow playbook.

\[Omitted image "demand-playbook4.png"\] Alt text: The Associate AI systems activity in the AI checkpoint stage.

<table id="table_pgw_hbn_g3c"><thead><tr><th>

Activity

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Associate AI systems

</td><td>

Form

</td><td>

Add AI systems to the demand by selecting from the existing systems or creating one.-   To link existing systems, use the **Product** and **Impacted AI systems** fields.
-   To create an AI system, select the **Create new AI system** link. This option is available only when AI Control Tower is installed and the investment type of the demand is set to artificial intelligence. For more information, see [Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md).

</td></tr></tbody>
</table>## Confirm demand readiness for review

This stage verifies that the demand is complete and ready for approval. Assign the demand to a portfolio or program and confirm that the demand is ready for approval.

<table id="table_dpl_ccn_g3c"><thead><tr><th>

Activity

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Align demand and assign portfolio/program

</td><td>

Form

</td><td>

Review the demand details and confirm readiness for the approval process. For more information, see [Demand details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-form-ppw.md).For example, the demand is assigned to the Digital Experience portfolio and the Customer Portal Modernization program.

</td></tr></tbody>
</table>## Approve and finalize demand

This stage confirms the demand details and converts the demand to a work entity. Confirm the work entity type and the approved timeline, and convert the demand.

|Activity|Type|Description|
|--------|----|-----------|
|Confirm details and convert to selected entity|Form|Review the selected work entity type, such as project or enhancement, and the approved timeline.|

## Complete demand

This final stage verifies that the demand was converted to the selected work entity and that the demand details carried over. If the demand is not converted to a work item, use the Details page to convert the demand. For more information, see [Create an entity from a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-an-entity-from-a-demand-ppw.md).

|Activity|Type|Description|
|--------|----|-----------|
|Review the converted entity|Form|Review the work entity created from the demand to verify that the conversion is complete.|

**Related topics**  


[Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md)

[Use playbook for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/use-playbooks-in-ppw.md)

[Customize and create playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-and-customize-playbooks-ppw.md)

