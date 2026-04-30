---
title: Define an epic in SAFe
description: Create an epic within SAFe. An epic is the largest unit of work that has one common objective such customer request, or business requirement. An epic is further decomposed into features for implementation and delivery by SAFe agile release trains \(ARTs\).
locale: en-US
release: zurich
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Define an epic in SAFe

Create an epic within SAFe. An epic is the largest unit of work that has one common objective such customer request, or business requirement. An epic is further decomposed into features for implementation and delivery by SAFe agile release trains \(ARTs\).

## Before you begin

Role required: safe\_art\_user or safe\_admin

## Procedure

1.  Create an epic using either of the following options.

<table id="choicetable_djp_xvn_mcb"><thead><tr><th align="left" id="d164255e71">

Option

</th><th align="left" id="d164255e74">

Steps

</th></tr></thead><tbody><tr><td id="d164255e80">

**From the Backlog tab**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)**.
2.  From the list, select the **ART** level.
3.  From the adjacent list, select the required ART value.
4.  Select the **Backlog** tab.
5.  From the **Create** list, select **Create Epic**. The epic is displayed in the **Backlog** tab with the state as **Backlog**.


</td></tr><tr><td id="d164255e131">

**From the Epics module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Epics**.
2.  Click **New**. The epic is displayed in the **Epics** list and **Backlog** tab with the state as **Funnel**.


</td></tr><tr><td id="d164255e170">

**From the Portfolios module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Portfolios**.
2.  In the SAFe epics related list, click **New**.


</td></tr></tbody>
</table>2.  In the form, fill in the fields:

<table id="table_yxr_n2z_msb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number for the epic.

</td></tr><tr><td>

Enabler

</td><td>

Check box identifying the epic as an enabler. Enablers do not add direct business value but help lay a foundation for future work. For example, an enabler epic might be an investigation into the architecture used to build features.

</td></tr><tr><td>

State

</td><td>

State of the epic:-   **Funnel**: Created from **Scaled Agile Framework \(SAFe\)** &gt; **Epic**.
-   **Review**: Under review considering parameters like WSJF score and WIP limited.
-   **Analysis**: Approved or rejected based on parameters like WSJF score refinement, cost estimation, alternatives, and WIP limited.
-   **Backlog**: Approved and assigned to an ART. In this state, the ART level user segments the epic into features.
-   **Implementation**: Epic is being implemented.
-   **Done**: Implementation is complete.


</td></tr><tr><td>

Color

</td><td>

Color that you attribute to the epic. Epic colours help you visually identify and group features by their epic on the ART's backlog page of the SAFe board.

</td></tr><tr><td>

WSJF Score

</td><td>

Weighted Shortest Job First \(WSJF\) score is used to prioritize and sequence jobs to produce optimum business value. A job with the highest WSJF score receives the highest priority for implementation. A job can refer to an epic, feature, or any business capability.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the epic.

</td></tr><tr><td>

Description

</td><td>

A more detailed description of the epic.

</td></tr></tbody>
</table><table id="table_kst_xhb_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User-business Value

</td><td>

Business value of the job based on parameters like impact on revenue or other solutions in the market offering similar capabilities.

</td></tr><tr><td>

Time criticality

</td><td>

Impact on the business when deadlines are missed. For example, how projected revenue gains are reduced over time when deadlines are shifted.

</td></tr><tr><td>

Risk reduction

</td><td>

Analyze how much risk this epic can help you avoid by answering questions such as:-   Does the job add value to the business in other ways?
-   Does the job bring in new business opportunities?
-   Does the job reduce the risk for a future delivery?


</td></tr><tr><td>

Job size

</td><td>

Estimated duration for completion of the job.

</td></tr><tr><td>

Total story count

</td><td>

Number of active stories in the epic. This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Completed count

</td><td>

Number of stories that have been completed in the epic. This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Percent complete by count

</td><td>

Percentage of work that has been completed in the epic. Value is calculated by story count. This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Total estimate

</td><td>

Sum of estimates of all the active stories in the epic.This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Completed estimate

</td><td>

Sum of estimates of all the completed stories in the epic.This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Percent complete by estimate

</td><td>

Percentage of work that has been completed in the epic. Value is calculated by points \(estimate\) of stories in the epic.This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Missing estimates

</td><td>

Number of stories without estimation points.This field is not displayed by default. Configure the field in the form layout.

</td></tr><tr><td>

Top program

</td><td>

Program mapped to the SAFe work enabling top-down hybrid planning. All the active child SAFe features of this epic are automatically associated with the selected program.This field is visible in the SAFe view of the epic form if you activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

</td></tr></tbody>
</table>3.  Fill in the Planning section if you want to create benefit plans for the epic.

    This section is available when the Benefit view is selected.

    |Field|Description|
    |-----|-----------|
    |Planned start date|Projected start date for the epic. The planned start date can be the current date or a future date.|
    |Planned end date|Projected end date for the epic. The planned end date must be after the planned start date.|
    |Planned benefit|Benefit value that is rolled up from the benefit breakdown.|
    |Actual start date|Actual start date for the epic. The actual start date can be on or before the planned start date.|
    |Actual end date|Actual end date for the epic. The actual end date can be before the planned start date but not before the actual start date.|
    |Actual benefit|Actual benefit value that is rolled up from the actual benefit in the benefit breakdown.|

4.  Click **Submit**.


-   **[Create a monetary benefit plan for an epic](create-monetary-benefit-plan-safe-epic.md)**  
Epic benefit plans capture the potential benefits accrued by the epic when the epic is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
-   **[Create a non-monetary benefit plan for an epic](create-non-monetary-benefit-plan-safe-epic.md)**  
Epic benefit plans capture the potential non-financial benefits accrued by the epic when the epic is executed. Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
-   **[Associate monetary and non-monetary benefit plans](associate-benefit-plans-safe-epic.md)**  
Associate monetary and non-monetary benefit plans, so that you can capture the potential benefits \(financial and non-financial\) accrued by the epic for the hybrid benefit plans.
-   **[Generate labor costs for epics](gen-labor-costs-safe-epic.md)**  
View the labor cost expenses based on the resource assignments for your epics.

**Parent Topic:**[SAFe entities](../concept/key-entities-SAFe.md)

