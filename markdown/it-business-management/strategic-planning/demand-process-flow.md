---
title: Demand workflow
description: The demand workflow defines the life-cycle of a request, from initial intake through assessment and approval to downstream execution. This structured approach ensures that each request is evaluated consistently, aligned with business objectives, and supported by the right processes before any resources are committed.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-01-14"
reading_time_minutes: 2
breadcrumb: [Explore, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Demand workflow

The demand workflow defines the life-cycle of a request, from initial intake through assessment and approval to downstream execution. This structured approach ensures that each request is evaluated consistently, aligned with business objectives, and supported by the right processes before any resources are committed.

## Workflow overview

The end-to-end life-cycle for managing demands is described in the following table. This workflow confirms that the demands are progressively refined, validated, and aligned with business and strategic objectives.

**Note:** The demand workflow overview table describes the traditional demand management process. You can customize the states and activities according to the requirements of your organization by defining your custom playbook.

<table id="table_mb5_3qp_13c"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Demand states involved

</th><th>

Roles involved

</th></tr></thead><tbody><tr><td>

Create a demand

</td><td>

Demands enter the system via Service Catalog, Idea Portal, or directly by demand managers:-   Business users can submit an idea via the Service Catalog or Idea Portal. These ideas are evaluated by demand managers and promoted to a demand, if necessary.
-   Business users can bypass the ideation process and submit a demand directly from the Service Catalog.
-   Demand managers or demand users can directly submit demands from the Next Experience for Demand Management.

</td><td>

Draft

</td><td>

Business user, demand manager, demand user

</td></tr><tr><td>

Complete demand details

</td><td>

The demand manager or demand user reviews and adds required details. Demand managers can create and assign demand tasks to gather more information, if necessary.The demand is moved from the draft to the submitted state once the basic demand details are added.

</td><td>

Draft → Submitted

</td><td>

Demand manager, demand user

</td></tr><tr><td>

Refine and finalize demand

</td><td>

The demand manager completes all required information \(size, impact, business case, timeline, resources, costs/benefits, stakeholder registry, strategy alignment\). They can assign tasks or request SME \(subject matter expert\) support, whenever required.

</td><td>

Submitted

</td><td>

Demand manager

</td></tr><tr><td>

Move demand to screening

</td><td>

The demand manager moves the demand to screening. The assessments are sent to the stakeholders to score the demand once it is in the screening state.

</td><td>

Submitted → Screening

</td><td>

Demand manager

</td></tr><tr><td>

Complete assessments

</td><td>

Stakeholders complete and submit assessments for scoring.

</td><td>

Screening

</td><td>

Stakeholder

</td></tr><tr><td>

Move demand to qualified

</td><td>

The demand moves to the qualified state once the required assessments are submitted.-   Next Experience for Demand Management updates the state automatically.
-   Demand manager manually sets the demand to qualified while it is in screening. For example, when assessments are delayed or not required.

</td><td>

Screening → Qualified

</td><td>

Demand manager, Next Experience for Demand Management

</td></tr><tr><td>

Review demand

</td><td>

Stakeholders review the demand for approval or deferral.

</td><td>

Qualified

</td><td>

Stakeholder

</td></tr><tr><td>

Approve/Defer a demand

</td><td>

The demand manager sets demand as approved \(moves forward for execution\) or deferred \(moves to Deferred state\).

</td><td>

Qualified → Approved/Deferred

</td><td>

Demand manager, demand approver

</td></tr><tr><td>

Convert demand to strategic/operational entity

</td><td>

Once the Demand is approved, the demand manager creates the selected entity such as project, enhancement, or Enterprise Agile Planning \(EAP\) entities.The created entity is based on the values in the **Category** and **Type** fields of the Demand record.

Depending on the type of record created, the demand data is migrated to the created entity.

</td><td>

Approved

</td><td>

Demand manager

</td></tr><tr><td>

Complete demands

</td><td>

Based on the selection in the **Close Demand** field, a demand is completed automatically when converted entity is completed, or manually by the demand manager at any state.

</td><td>

Approved → Completed

</td><td>

Demand manager, Next Experience for Demand Management

</td></tr></tbody>
</table>