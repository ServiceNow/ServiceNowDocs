---
title: Automatic pipeline project creation via Shopping Hub or Employee Center intake requests
description: When a shopper submits sourcing requests for products, pipeline projects are automatically created, provided the product price meets the budget conditions defined in the decision table.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Sourcing Pipeline Management, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Automatic pipeline project creation via Shopping Hub or Employee Center intake requests

When a shopper submits sourcing requests for products, pipeline projects are automatically created, provided the product price meets the budget conditions defined in the decision table.

By default, the budget threshold is set to $250,000. However, you can configure the budget conditions in the decision table to suit your business requirements. For more information, see [Pipeline project creation rule for high-value sourcing requests](pipeline-project-creation-rule.md).

If multiple sourcing requests are submitted for products that belong to the same spend category or the same sourcing manager, only a single pipeline project is created to group all those products.

Pipeline projects created automatically through sourcing intake requests are set to the Draft state.

## Fields automatically populated in the pipeline project record

The following fields are automatically populated for pipeline project records created through an intake request:

<table id="table_dh4_3jd_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

-   If the intake request results in a single sourcing request \(SR\), the short description follows this format:

PIPE00001 for &lt;Product Name&gt;

-   If multiple SRs are created from the same intake request, the format is:

PIPE00001 Multiple requests for &lt;Requestor Name&gt;


</td></tr><tr><td>

Requestor

</td><td>

Populated based on the value provided in the **Who is this request for** field.

</td></tr><tr><td>

Number

</td><td>

An auto-generated number that uniquely identifies the pipeline project.

</td></tr><tr><td>

Estimated end date

</td><td>

If multiple SRs have different delivery dates, the earliest delivery date is used as the estimated end date.

</td></tr><tr><td>

Spend category

</td><td>

Derived from the Product Category field using predefined spend category to product category mappings.**Note:** If the sourcing requests in a pipeline project have different spend categories, the **Spend category** field is left blank. If the sourcing manager is the same across different spend categories, the requests are grouped into one pipeline project. In such cases, the **Spend category** field is left blank.

</td></tr></tbody>
</table>## Sourcing requests grouping logic

The following conditions determine how sourcing requests \(SR\) are grouped into pipeline projects.

<table id="table_bc1_xrf_sfc"><thead><tr><th>

Grouping logic

</th><th>

Condition

</th></tr></thead><tbody><tr><td>

Group SRs by spend category \(if available\)

</td><td>

-   If an SR includes multiple products with different product categories, and category taxonomy is configured, then separate pipeline projects are created for each spend category.
-   However, if the sourcing manager is the same for those spend categories, they’re grouped into one pipeline project. In this case, the **Spend Category** field is left blank in the grouped pipeline project.

</td></tr><tr><td>

Group SRs without spend categories

</td><td>

-   SRs that do not have a spend category are grouped into a single pipeline project.
-   If four SRs are created from the same intake request, and three have spend categories while one doesn't, the one without is grouped with the others.

</td></tr><tr><td>

Spend category restrictions for adding SRs to a pipeline project

</td><td>

SRs can be added to an existing pipeline project in the following scenarios:-   The spend category of the SRs matches with that of the pipeline project.
-   The spend category is blank and not defined for the SRs.
-   The SRs must be in either the Pending Review or Pending Approval state.

</td></tr></tbody>
</table>## How pipeline project creation affects cancellation

The way a pipeline project is created determines when and how it can be canceled.

<table id="table_dcb_1md_wfc"><thead><tr><th>

Pipe creation method

</th><th>

Cancellation behavior

</th></tr></thead><tbody><tr><td>

Auto-created pipeline projects from sourcing requests

</td><td>

If a pipeline project is auto-created from a sourcing request \(SR\), and that SR is later canceled, the pipeline project is also canceled but only in Draft state.If the pipeline project has progressed to the Work in Progress \(WIP\) state, it isn’t canceled, even if the associated SR is canceled.

</td></tr><tr><td>

Manually created pipeline projects

</td><td>

For pipeline projects created manually from the List view, the project isn’t canceled even if the associated sourcing request is canceled.

</td></tr><tr><td>

For both auto-created and manually created pipeline projects

</td><td>

If all sourcing requests under a pipeline project are in Closed – Cancelled or Closed – Rejected state, the pipeline project also moves to the Closed – Cancelled state.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

