---
title: Demand workflow
description: The demand workflow defines the stages a demand moves through, from initial intake to assessment, approval, and execution. At each stage, you can evaluate the demand, align it with business objectives, and set up the right processes before resources are assigned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/demand-process-flow.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Demand workflow

The demand workflow defines the stages a demand moves through, from initial intake to assessment, approval, and execution. At each stage, you can evaluate the demand, align it with business objectives, and set up the right processes before resources are assigned.

## Workflow overview

The following table lists the end-to-end life cycle for managing demands. This workflow provides a process for demands so they are progressively refined, validated, and aligned with business and strategic objectives.

**Note:** This workflow describes the traditional demand management process. You can customize the states and activities by defining a custom playbook.

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

Demands enter the system via Service Catalog or Idea Portal, or being submitted directly by demand managers: -   Business users can submit an idea via the Service Catalog or Idea Portal. The idea is then evaluated by demand managers after which they can promote it to a demand.
-   Business users can bypass the ideation process and submit a demand directly from the Service Catalog.
-   Demand managers or demand users can directly submit demands from the Next Experience for Demand Management.

</td><td>

Draft

</td><td>

Business user, demand manager, demand user

</td></tr><tr><td>

Complete demand details

</td><td>

The demand manager or demand user reviews and adds required details. The demand moves from the draft to the submitted state after the basic demand details are added.

</td><td>

Draft → Submitted

</td><td>

Demand manager, demand user

</td></tr><tr><td>

Refine and finalize demand

</td><td>

The demand manager completes all required information \(size, impact, business case, timeline, resources, costs/benefits, stakeholder registry, strategy alignment\). The demand manager can assign tasks or request SME \(subject matter expert\) support.

</td><td>

Submitted

</td><td>

Demand manager

</td></tr><tr><td>

Move demand to screening

</td><td>

The demand manager moves the demand to screening. Assessments are sent to the stakeholders to score the demand after it reaches the screening state.

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

The demand moves to the qualified state after the required assessments are submitted.-   Next Experience for Demand Management updates the state automatically.
-   The demand manager manually sets the demand to qualified while it is in screening, for example, when assessments are delayed or not required.

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

Approve or defer a demand

</td><td>

The demand manager sets the demand to approved \(moves forward for execution\) or deferred \(moves to the Deferred state\).

</td><td>

Qualified → Approved or Deferred

</td><td>

Demand manager, demand approver

</td></tr><tr><td>

Convert demand to strategic/operational entity

</td><td>

After the demand is approved, the demand manager creates the selected entity such as project, enhancement, or Enterprise Agile Planning \(EAP\) entities.The created entity is based on the values in the **Category** and **Type** fields of the Demand record.

Depending on the type of record created, the demand data is migrated to the created entity.

</td><td>

Approved

</td><td>

Demand manager

</td></tr><tr><td>

Complete demands

</td><td>

Based on the selection in the **Close Demand** field, a demand is completed automatically when the converted entity is completed, or manually by the demand manager at any state.

</td><td>

Approved → Completed

</td><td>

Demand manager, Next Experience for Demand Management

</td></tr></tbody>
</table>