---
title: Define an objective for a safety audit
description: Define an objective to add detailed goal and scope of the safety audit. You can create as many objectives as the audit requires.
locale: en-US
release: zurich
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-01"
reading_time_minutes: 4
breadcrumb: [Create and manage a safety audit, Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define an objective for a safety audit

Define an objective to add detailed goal and scope of the safety audit. You can create as many objectives as the audit requires.

## Before you begin

-   People who should be assigned objectives are added to the audit's **People involved** list. The **Assigned to** field on an objective is filtered to people already added to the audit. For more information, see [Add people involved in a safety audit](hs-add-people-involved-safety-audit.md).
-   Any documents or standards to be cited are uploaded and accessible.

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.safety\_audit\_writer

## About this task

Before an audit begins, define its scope by creating the audit objectives, the criteria used as benchmarks, and the items to be reviewed.

-   An objective describes a specific area of focus for the audit. Each objective has a method \(for example, interview, document review, or inspection\), a due date, and can be assigned to a person involved in the audit.
-   Criteria are the benchmarks or standards against which the audit measures compliance. Criteria are associated with one or more objectives.
-   Items for review are the specific records, documents, or assessments that should be examined to meet an objective. Items for review are assigned to a person involved in the audit, who is responsible for conducting that part of the review and raise findings against them.

**Note:** If you have a previous audit with a similar scope, you can select **Import scope** to pre-populate the objectives and the related sections rather than entering them manually. For more information, see [Import scope from an existing safety audit](hs-import-scope-existing-safety-audit.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  In the **Audits** list, select **All** and open the audit record to add the objective to.

4.  Select the **Objectives** tab and then select **New** in the Objectives section.

5.  On the Objective form, fill in the fields.

    For information on field descriptions, see [Audit Objective fields](../reference/hs-audit-objectives-form.md).

6.  Add criteria to the audit objective.

    1.  Expand the objective card to which you want to add criteria.

    2.  In the **Criteria** section of the objective, select **New**.

    3.  In the Add Criteria dialog box, fill in the fields.

<table id="table_bwn_vgq_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Criteria type

</td><td>

Type of criteria.-   **Regulatory list**: A regulatory or standards list.
-   **Authority document**: An Integrated Risk Management \(IRM\) authority document.

**Note:** This option is available only when Integrated Risk Management \(IRM\) is installed.

-   **H&amp;S Document**: A document from the Health and Safety document library.
-   **Knowledge base article**: A knowledge base article, for example, for company's Health and Safety procedures.
-   **Text**: Free text description of the criteria.


</td></tr><tr><td>

Criteria

</td><td>

Standards that the audit measures compliance against. The items in this list appear based on the selected **Criteria type** and the available record of that type.

**Note:** If you use the 3E integration \(for example, with Health and Safety Environmental Management\), regulatory lists can be populated automatically from 3E when Regulatory list is selected as **Criteria type**.

</td></tr><tr><td>

Title

</td><td>

Label that identifies the text-based criterion.This field appears only when **Text** is selected from **Criteria**.

</td></tr><tr><td>

Objectives

</td><td>

Objectives associated with this criterion.You can link this criterion to multiple objectives on this audit.

</td></tr><tr><td>

Description

</td><td>

Additional context for the criterion.

</td></tr></tbody>
</table>    4.  Select **Add**.

    5.  If necessary, add more criteria to the objective.

7.  Adding items for review to the audit objective.

    1.  Expand the objective card to which you want to add an item for review.

    2.  In the **Items for review** section of the objective, select **New**.

    3.  In the Add Item for review dialog box, fill in the fields.

<table id="table_d1n_4lq_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Item type

</td><td>

Type of item, such as a Health and Safety record type, to be reviewed.

</td></tr><tr><td>

Item for review

</td><td>

Record to be reviewed for this audit. The items in this list appear based on the selected **Item type**.

</td></tr><tr><td>

Priority

</td><td>

Priority level to review this item.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to this item for review.Only the people added to the **People involved** list of this audit are available in this field. For more information, see [Add people involved in a safety audit](hs-add-people-involved-safety-audit.md).

</td></tr><tr><td>

Objectives

</td><td>

Objectives associated with this item for review.You can link this item to additional objectives on this audit.

</td></tr><tr><td>

Criteria

</td><td>

Criteria associated with this item for review.You can link this item to multiple criteria on this audit.

</td></tr><tr><td>

Instructions

</td><td>

Guidance for the person assigned to this item, describing what to review or verify during the audit.

</td></tr></tbody>
</table>    4.  Select **Add**.

    5.  If necessary, add more items for review to the objective.

8.  Select **Save objective**.

9.  If necessary, add more objectives for the audit.


## Result

-   Each objective defined for the audit appears as a collapsible card on the **Objectives** tab. The card header shows the objective name, priority, and state.
-   The objective is also listed in the **Objectives** tab of the assigned person's record on this audit.

## What to do next

People assigned to the audit objectives can raise findings against the items for review during the audit. You can create a finding from the audit's **Findings** tab or directly from within an item for review. For more information, see [Add a finding for a safety audit](hs-add-finding-rca-safety-audit.md).

**Parent Topic:**[Create and manage a safety audit](hs-create-manage-safety-audit-workspace.md)

