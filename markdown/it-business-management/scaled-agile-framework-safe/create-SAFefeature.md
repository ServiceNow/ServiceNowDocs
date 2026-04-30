---
title: Define a feature in SAFe
description: Create a feature in SAFe and break it down into smaller user stories for implementation and delivery by SAFe teams.
locale: en-US
release: yokohama
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Define a feature in SAFe

Create a feature in SAFe and break it down into smaller user stories for implementation and delivery by SAFe teams.

## Before you begin

Role required: safe\_art\_user or safe\_admin

## Procedure

1.  Create a feature using any of the following options.

<table id="choicetable_djp_xvn_mcb"><thead><tr><th align="left" id="d70704e64">

Option

</th><th align="left" id="d70704e67">

Steps

</th></tr></thead><tbody><tr><td id="d70704e73">

**From the Backlog tab**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **SAFe Board** &gt; **Backlog**.
2.  From the list, select **ART**.
3.  From the adjacent list, select your agile release train \(ART\).
4.  From the Create list, select **Create Feature**. The feature is displayed in the **Backlog** tab with the state as **Backlog**.


</td></tr><tr><td id="d70704e121">

**From the Feature module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Features**.
2.  Click **New**.


</td></tr><tr><td id="d70704e151">

**From the Epics module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Epics**.
2.  Click any epic.
3.  In the SAFE Features related list, click **New**.


</td></tr><tr><td id="d70704e184">

**From the Agile Release Trains module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Agile Release Trains**.
2.  Click any agile release train.
3.  In the SAFe Features related list, click **New**.


</td></tr></tbody>
</table>    You can also convert an active SAFe story into a SAFe feature. For details, see [Related links and lists for a SAFe story](../reference/related-links-and-lists-of-a-safe-story.md).

2.  On the form, fill in the fields.

<table id="table_jpv_hwh_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number for the feature.

</td></tr><tr><td>

Enabler

</td><td>

Option that identifies a feature as an enabler. An enabler does not bring any business value but helps in laying the foundation for future work. For example, you can use an enabler to investigate the architecture that is used to build stories.

</td></tr><tr><td>

Color

</td><td>

Color that you attribute to the feature. Feature colors help you visually identify and group stories by their feature on the team's backlog page of the SAFe board.This color also appears as a filled circle on the SAFe story cards on the SAFe PI planning board so that you can identify its feature.

</td></tr><tr><td>

WSJF score

</td><td>

Weighted Shortest Job First \(WSJF\) score that you use to prioritize and sequence jobs to produce an optimum business value. A job with the highest WSJF score receives the highest priority for implementation. A job can be an epic, feature, or any business capability.

</td></tr><tr><td>

State

</td><td>

State of the feature. Select one of the following:-   **Funnel**: In this state, you can create features from approved ideas.
-   **Analysis**: In this state, the product management team reviews the features and considers the acceptance criteria, benefit hypothesis, technical feasibility, and scope estimates.
-   **Backlog**: In this state, you can prioritize approved features and assign them to an ART.
-   **Implementation**: In this state, you can break down a feature into stories that you can later assign to a team.
-   **Validation on staging**: In this state, you can integrate the feature in the system and present it to the product management team for approval and feedback.
-   **Deployment**: In this state, the deployment testing of feature is complete.
-   **Released**: In this state, you are ready to release the feature to the end users and assess the benefit hypotheses.
-   **Cancelled**: In this state, a feature has been canceled.


</td></tr><tr><td>

SAFe epic

</td><td>

Epic to which the feature belongs.

</td></tr><tr><td>

Agile release train

</td><td>

Agile release train to which the feature belongs.

</td></tr><tr><td>

Program increment

</td><td>

Program increment in which the feature is scheduled for completion.

</td></tr><tr><td>

SAFe team

</td><td>

Team that is primarily responsible for the delivery of the feature.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the feature.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the feature.

</td></tr><tr><td>

Work notes

</td><td>

Work notes that indicate the progress of the feature at various stages in its life cycle.

</td></tr></tbody>
</table><table id="table_krh_2ys_2dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User-business Value

</td><td>

Estimate of the business value of the job from this feature. Consider the impact on revenue or other solutions in the market that offer similar capabilities.

</td></tr><tr><td>

Time criticality

</td><td>

Estimated impact on the business when deadlines are missed. For example, consider how shifting deadlines can reduce the projected revenue gain.

</td></tr><tr><td>

Risk reduction

</td><td>

Analysis of how much risk this feature can help you avoid. Answer questions such as the following:-   Does the job add value to the business in other ways?
-   Does the job bring in new business opportunities?
-   Does the job reduce the risk for a future delivery?


</td></tr><tr><td>

Job size

</td><td>

Estimated duration for completion of the job.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

Use the SAFe stories related list to view and add stories to the feature.

-   **[Split a SAFe feature](split-a-safe-feature.md)**  
Split a SAFe feature into two separate features so that you can track complete and incomplete stories. You can move the feature with the incomplete stories to your backlog or to a future program increment \(PI\) so that you can maintain accurate metrics of the previous sprints and PIs.

**Parent Topic:**[SAFe entities](../concept/key-entities-SAFe.md)

**Related topics**  


[Define a story in SAFe](create-SAFestory.md)

