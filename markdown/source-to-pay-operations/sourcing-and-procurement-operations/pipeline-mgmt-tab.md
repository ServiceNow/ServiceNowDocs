---
title: Pipeline management tab
description: The Pipeline management tab enables you to get insights into savings and pipeline projects, improving visibility, tracking, and collaboration across teams.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Sourcing Pipeline Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Pipeline management tab

The Pipeline management tab enables you to get insights into savings and pipeline projects, improving visibility, tracking, and collaboration across teams.

To view the Pipeline management tab in the Source-to-Pay Worksapce, you must have the sn\_spend\_pipeline.sourcing\_pipeline\_user role and have the following applications installed:

-   Spend and Savings Management \(sn\_spend\_mgmt\)
-   Sourcing Pipeline Management \(sn\_spend\_pipeline\)

![Pipeline management tab](../image/pipeline-management-tab.png "Pipeline management tab")

## Components in the Pipeline management tab

<table id="table_owl_24z_lxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

My work

</td></tr><tr><td>

New pipeline projects this week

</td><td>

Single score

</td><td>

Displays the projects that are new this week and assigned to the logged-in user.

</td></tr><tr><td>

Pipeline projects starting withing 30 days

</td><td>

Single score

</td><td>

Displays the pipeline projects assigned to the logged-in user with an estimated start date due in 30 days or less.

</td></tr><tr><td>

Contracts expiring within 180 days

</td><td>

Single score

</td><td>

Displays the contracts with an expiration date in 180 days or less, where the logged-in user is the contract administrator.

</td></tr><tr><td>

Active projects

</td><td>

Ring chart

</td><td>

Displays the active projects assigned to the logged-in user, excluding projects in the Closed completed or Closed cancelled states.

</td></tr><tr><td>

Active projects by priority

</td><td>

Bar graph

</td><td>

Displays the projects by priority assigned to the logged-in user, excluding projects in the Closed completed or Closed cancelled states.

</td></tr><tr><td>

My pipeline projects

</td><td>

List

</td><td>

Displays a list of all active pipeline projects assigned to the logged-in user, sorted by priority and excluding projects in the Closed completed or Closed cancelled states.

</td></tr><tr><td class="sub-head" colspan="3">

My savings

</td></tr><tr><td>

Hard savings YTD

</td><td>

Single score

</td><td>

Displays the total hard savings from closed and completed pipeline projects assigned to the logged-in user, where the savings end date is greater than or equal to the current year.**Note:** The My Savings section displays the savings scores calculated from the annualized data entered on the pipeline object.

For more information about how the Hard Savings YTD metric is calculated, see [Hard Savings YTD metric calculation](pipeline-hard-savings-ytd.md).

</td></tr><tr><td>

Cost avoidance YTD

</td><td>

Single score

</td><td>

Sum of all the Cost avoidance on the Closed Completed pipeline projects assigned to the logged in user, where the savings end date is greater than or equal to the current year.For more information about how the Cost Avoidance YTD metric is calculated, see [Cost Avoidance YTD metric calculation](pipeline-cost-avoidance-ytd.md).

</td></tr><tr><td>

Planned savings - Current year

</td><td>

Single score

</td><td>

Total estimated savings \(estimated hard savings + estimated cost avoidance\) from planned pipeline projects assigned to the logged-in user, where the estimated end date falls within the current year.For more information about how the Planned Savings \(Current Year\) metric is calculated, see [Planned Savings \(Current Year\) metric calculation](pipeline-planned-savings-current-year.md).

</td></tr><tr><td>

Active savings - Current year

</td><td>

Single score

</td><td>

Displays the total estimated savings \(estimated hard savings + estimated cost avoidance\) from in-progress pipeline projects assigned to the logged-in user, where the estimated end date falls within the current year.For more information about how the Active Savings \(Current Year\) metric is calculated, see [Active Savings \(Current Year\) metric calculation](pipeline-active-savings-current-year.md).

</td></tr></tbody>
</table>-   **[Hard Savings YTD metric calculation](pipeline-hard-savings-ytd.md)**  
**Hard Savings YTD** \(Year-to-Date\) shows the total realized savings from pipeline projects that were closed and completed within the current calendar year. These are confirmed, negotiated savings — not estimates or projections.
-   **[Cost Avoidance YTD metric calculation](pipeline-cost-avoidance-ytd.md)**  
**Cost Avoidance YTD** measures the costs that were prevented through pipeline projects during the current calendar year. Unlike hard savings, which reflect a direct reduction in spend, cost avoidance captures expenditures that were not incurred.
-   **[Planned Savings \(Current Year\) metric calculation](pipeline-planned-savings-current-year.md)**  
**Planned Savings \(Current Year\)** shows the projected savings from pipeline projects in **Planned** state—projects approved and scheduled but not yet started. This metric uses the **Targeted savings** field to represent future savings goals.
-   **[Active Savings \(Current Year\) metric calculation](pipeline-active-savings-current-year.md)**  
**Active Savings \(Current Year\)** shows the targeted savings from pipeline projects that are currently in progress. This metric represents in-flight work where final realized savings are not yet known.

**Parent Topic:**[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

