---
title: Create an epic in Agile Development 2.0
description: Define the high-level requirements of the features that you want to develop by creating epics in Agile Development 2.0.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Create an epic in Agile Development 2.0

Define the high-level requirements of the features that you want to develop by creating epics in Agile Development 2.0.

## Before you begin

Role required: scrum\_story\_creator, scrum\_admin

## About this task

Create epics in Agile Development 2.0 and organize them in a hierarchy of parent and children. You can associate an epic to a product, theme, or configuration item \(an item or service that is affected\).

## Procedure

1.  Navigate to **Agile Development** &gt; **Epics**.

2.  Select **New**.

    Alternatively, you can open the new epic form using the Agile board, from a theme record, or from a product record.

    You can also convert an existing active story into an epic. For details, see [Related links and lists for a Story in Agile Development 2.0](../reference/agile-2-0-story-related-lists-related-links.md).

3.  On the form, fill in the fields.

<table id="table_wgj_cxt_msb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number for the epic.

</td></tr><tr><td>

Product

</td><td>

Product associated with this epic.You can associate an epic with only one product at a time.

</td></tr><tr><td>

Priority

</td><td>

Priority of the epic.

</td></tr><tr><td>

State

</td><td>

State of the epic. Select one of the following:-   **Draft**

The epic requirements, such as the detailed description, are still being drafted.

-   **Ready**

The epic is ready for pickup by the product team. The product manager and the scrum team can break the epic down into stories.

-   **Work in Progress**

The development team is working on the stories for epic and recording the changes in the work notes field.

-   **Complete**

The development and testing efforts on all the stories and any child epics for the epic are complete.

-   **Cancelled**

The epic has been canceled.

This field is automatically set to **Draft**.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the epic.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the epic.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work done on the epic.

</td></tr><tr><td>

Total story count

</td><td>

Number of stories in the epic.

</td></tr><tr><td>

Completed count

</td><td>

Number of completed stories in the epic.

</td></tr><tr><td>

Percent complete by count

</td><td>

Percentage of completed work in the epic. Story count is used to calculate this value.

</td></tr><tr><td>

Total estimate

</td><td>

Sum of the estimates of all stories in the epic.

</td></tr><tr><td>

Completed estimate

</td><td>

Sum of the estimates of all the completed stories in the epic.

</td></tr><tr><td>

Percent complete by epic

</td><td>

Percentage of completed work in the epic. Story estimate is used to calculate this value.

</td></tr><tr><td>

Missing estimate

</td><td>

Number of stories in the epic that are missing estimates.

</td></tr><tr><td>

Top program

</td><td>

Program mapped to the scrum work enabling top-down hybrid planning.This field is visible in the Scrum view of the epic form if you activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

</td></tr></tbody>
</table>    Fill in the Planning section if you want to create benefit plans for the epic. This section is available in the Benefit view of the epic form.

4.  Click **Submit**.


## What to do next

-   Add child epics or stories to the epic:
    -   Create a child epic for this epic by selecting **New** from the Child Epics related list.
    -   Add stories to this epic by selecting **New** from the Stories related list. For more information, see [Create a story in Agile Development 2.0](create-a-story.md).

        An epic can have one or more stories, but a story can belong to only one epic at a time.

-   You can also associate epics to a project in Project Portfolio Management from the Epics related list.

    This related list appears only when the value for the **Execution Type** field is selected as **Agile** and the Agile Development 2.0 plugin is installed.


-   **[Create a monetary benefit plan for an epic](create-monetary-benefit-plan-agile-epic.md)**  
Epic benefit plans capture the potential benefits accrued by the epic when the epic is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
-   **[Create a non-monetary benefit plan for an epic](create-non-monetary-benefit-plan-agile-epic.md)**  
Epic benefit plans capture the potential non-financial benefits accrued by the epic when the epic is executed. Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
-   **[Associate monetary and non-monetary benefit plans](associate-benefit-plans-agile-epic.md)**  
Associate monetary and non-monetary benefit plans, so that you can capture the potential benefits \(financial and non-financial\) accrued by the epic for the hybrid benefit plans.
-   **[Generate labor costs for epics](gen-labor-costs-epics.md)**  
View the labor cost expenses based on the resource assignments for your epics.

**Parent Topic:**[Using Agile Development 2.0](../concept/using-agile-development-2-0.md)

