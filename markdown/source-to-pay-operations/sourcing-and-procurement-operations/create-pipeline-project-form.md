---
title: Create New Pipeline Project form
description: Use the Create New Pipeline Project form to provide details about the pipe project.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Sourcing and Procurement Operations reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create New Pipeline Project form

Use the Create New Pipeline Project form to provide details about the pipe project.

<table id="table_xfm_xr5_ksb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Pipeline Project

</td></tr><tr><td>

Number

</td><td>

An auto-generated number that uniquely identifies the pipeline project.

</td></tr><tr><td>

State

</td><td>

The current state of the pipeline project. Available values:-   **Draft**
-   **Planned**
-   **Work in Progress**
-   **Closed Complete**
-   **Closed Canceled**

</td></tr><tr><td>

Priority

</td><td>

Indicates how quickly you must complete the pipeline project.

</td></tr><tr><td>

Project type

</td><td>

Specifies the type of project based on the sourcing objective. Available values:-   Supplier Optimization – Consolidating suppliers to reduce spend
-   Contract Optimization - Renegotiating an existing contract
-   Savings Potential – Using market intelligence to potentially lower spend
-   Spend Optimization – Use sourcing events \(RFI, RFQ, RFP\) to lower spend
-   Risk Reduction – Supplier issues or backup for an existing supplier

</td></tr><tr><td>

Assigned to

</td><td>

Person assigned to the pipeline project.

</td></tr><tr><td>

Short description

</td><td>

Name of the pipeline project.

</td></tr><tr><td>

Description

</td><td>

Description of the pipeline project.

</td></tr><tr><td class="sub-head" colspan="2">

Project summary

</td></tr><tr><td>

Opportunity source

</td><td>

The source of the pipeline project.This field takes its value based on where the pipeline is created.

-   Intake Request: When the pipeline project is created from the Employee Center intake request.
-   Adhoc: When the Sourcing Manager or Procurement Specialist manually create the from the list view in Source-to-Pay Workspace.
-   System-generated: When the pipeline project is created by AI.

</td></tr><tr><td>

Business owner

</td><td>

The person who initiates the pipeline project and provides key input and approvals.

</td></tr><tr><td>

Spend category

</td><td>

Spend category used to report on savings.

</td></tr><tr><td>

Business unit

</td><td>

The business unit associated with the pipeline project, such as IT, Finance, HR, or Sales.

</td></tr><tr><td>

Estimated start date

</td><td>

The projected date when the project is expected to begin.

</td></tr><tr><td>

Estimated end date

</td><td>

The projected completion date for the pipeline project. This field reflects the due date specified in the sourcing request. If the pipeline project is associated with multiple sourcing requests, the earliest due date among them is used.

</td></tr><tr><td>

Actual start date

</td><td>

Actual start date of the pipeline project.**Note:** This field is automatically populated when the pipeline project moves to the Work in Progress state.

</td></tr><tr><td>

Actual end date

</td><td>

Actual end date of the pipeline project.**Note:** This field is automatically populated when the pipeline project moves to the Close Complete state.

</td></tr><tr><td>

Savings start date

</td><td>

The date from which savings are expected to begin.**Note:** This field becomes mandatory when the pipeline project moves to the Planned state.

</td></tr><tr><td>

Savings end date

</td><td>

The date until which savings are expected to be captured.**Note:** This field becomes mandatory when the pipeline project moves to the Planned state.

</td></tr><tr><td class="sub-head" colspan="2">

Financials

</td></tr><tr><td>

Estimated spend

</td><td>

The anticipated expenditure for the goods or services covered by the pipeline project.

</td></tr><tr><td>

Annual hard savings

</td><td>

The measurable, recurring cost reductions achieved each year as a result of sourcing activities, contract negotiations, or process improvements.

</td></tr><tr><td>

Annual cost avoidance

</td><td>

The estimated yearly savings realized by preventing future costs or price increases through proactive sourcing strategies or negotiations.

</td></tr><tr><td>

Estimated hard savings

</td><td>

The projected, quantifiable cost reduction expected from the pipeline project, typically derived from direct price decreases or efficiency gains.

</td></tr><tr><td>

Estimated cost avoidance

</td><td>

The projected financial benefit resulting from mitigating potential cost increases, avoiding additional expenses, or improving purchasing efficiency.

</td></tr><tr><td>

Other savings

</td><td>

Any additional savings achieved that don't fall under hard savings or cost avoidance categories.

</td></tr><tr><td>

Final spend

</td><td>

The actual amount spent at the completion of the pipeline project.

</td></tr><tr><td>

Lost savings

</td><td>

Forecasted savings that were not realized due to delays, project cancellations, or scope changes.

</td></tr><tr><td class="sub-head" colspan="2">

Associated records

</td></tr><tr><td>

Previous record type

</td><td>

The classification of the preceding project record.

</td></tr><tr><td>

Previous record ID

</td><td>

The unique identifier of the previous related project or sourcing record, used for reference.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Procurement Operations reference](spo-reference.md)

**Related topics**  


[Pipeline project record tabs and UI actions](pipeline-form-tabs-actions.md)

[Domain separation and Sourcing and Procurement Operations](../concept/psm-domain-separation.md)

[Sourcing and Procurement Operations glossary](../concept/spo-glossary.md#)

