---
title: Use Rolling grant approvals
description: Rolling grant approvals enhance the Grants Management funding workflow. You can propose awards and declines for any scored subset of applications at any time, without waiting for the entire proposal portfolio to complete review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-using-gm-rolling-grant-approvals-concept.html
release: australia
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 6
breadcrumb: [Evaluate a grant application, Grants Management Proposal Playbook, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Use Rolling grant approvals

Rolling grant approvals enhance the Grants Management funding workflow. You can propose awards and declines for any scored subset of applications at any time, without waiting for the entire proposal portfolio to complete review.

From Grants Management version 1.31, you can choose to process funding decisions incrementally as proposals are scored, or continue working in the traditional full-portfolio model. Select the **Funding Allocation** tab in the evaluation stage of the Grant management playbook to process funding decisions as proposals are scored.

## How rolling grant approvals work

The rolling approval workflow introduces two core capabilities: incremental proposal selection and batch-based Grant Program Director \(GPD\) approval. Grant program managers \(GPMs\) don't have to wait for every proposal to complete merit review and scoring before making funding decisions. Grant program managers can select any subset of scored proposals and mark them for funding or decline independently. These tentative funding recommendations are then grouped into a Funding Request — an approval packet that is submitted to the Grant program director for review. The Grant program director can approve, reject, or return the batch, and the Grant program manager can continue working on remaining proposals while previous batches are under review.

Rolling grant approvals support two common program models:

-   **Full portfolio**. All proposals are scored before any decisions are made. The grant program manager marks all proposals and submits them in a single Funding Request. This is the traditional workflow and continues to function unchanged.

-   **Rolling grants**. Proposals arrive and are scored on a continuous basis. The grant program manager marks and submits proposals in multiple batches over time, each as a separate Funding Allocation Request. Multiple requests can be in different review stages simultaneously.


## Spending Overview Widget

The **Spending Overview** panel on the **Funding Allocation** tab provides real-time budget and decision visibility. The panel contains two chart areas that provide visual breakdowns of the budget and decision metrics. Both chart areas update dynamically as proposals move through the workflow:

-   **Overall Spending**: Displays the total award budget, the committed budget \(Approved for Funding\), the amount pending director review \(Pending Funding Approval\), and the unallocated balance \(Remaining Budget\). A horizontal bar chart following these metrics shows approved funding by applicant type, labeled **Approved for funding by applicant type**.

-   **Decisions in Progress**: Displays the grant program manager's funding and decline recommendations the grant program manager has marked but not yet submitted. A bar chart following these metrics shows the funding recommendations by applicant type, labeled **Marked for funding by applicant type**.


\[Omitted image "psds-rolling-grants-funding-allocation-tab-july-26.png"\] Alt text: Funding allocation tab in rolling grants

The following table describes how budget figures shift as proposals move through each stage of the workflow.

|Workflow stage|Budget movement|Proposal Status|Spending Overview effect|
|--------------|---------------|---------------|------------------------|
|Grant program manager marks proposal for funding|Allocated budget moves from **Remaining Budget** to **Decisions in Progress** \(Marked for Funding\)|Marked for funding|Remaining Budget decreases; Marked for Funding increases|
|Grant program manager marks proposal for decline|No budget movement. Declined proposals carry no allocated budget.|Marked for decline|Marked for Decline count increases. No budget change.|
|Grant program manager submits funding request|Allocated budget moves from **Decisions in Progress** to **Pending Funding Approval**|Submitted for funding or Submitted for decline|Marked for Funding decreases; Pending Funding Approval increases|
|Grant Program Director approves the funding request|Allocated budget moves from **Pending Funding Approval** to **Approved for Funding**. Funds are committed.|Funding confirmed|Pending Funding Approval decreases; Approved for Funding increases|
|Grant Program Director rejects the funding request|Allocated budget is released from **Pending Funding Approval** back to **Remaining Budget**|Decline confirmed|Pending Funding Approval decreases; Remaining Budget increases|

**Note:**

The Total award Budget shown at the top of the Budget Breakdown bar reflects the full program allocation and does not change during the workflow. Only the segments within it shift as proposals move through the life cycle.

## Filter pills

The **Scored Proposals** list on the **Funding Allocation** tab includes a row of filter pills that provide quick-access views of proposals by status. Each pill displays a label and a count in parentheses that updates in real-time.

|Filter pill|Statuses included|What it shows|
|-----------|-----------------|-------------|
|All|All statuses|Every scored proposal in the program. This is the default view. The count shown in parentheses, for example, "**All \(12\)**" reflects the total number of proposals that have completed merit review and are available for allocation decisions.|
|Undecided|Undecided|Proposals with no grant program manager recommendation, including proposals returned by the grant program director.|
|Marked|Marked for Funding; Marked for Decline|All proposals with a tentative grant program manager recommendation that have not yet been submitted for approval.|
|Pending approval|Submitted for Funding; Submitted for Decline|Proposals submitted to the Grant Program Director as part of a funding request and awaiting a decision. The count reflects all proposals currently in the Grant Program Director's review queue.|
|Returned|Returned|Proposals sent back by the Grant Program Director for revision. These re-enter the grant program manager's working queue.|
|Decided|Approved; Declined|Proposals that have reached a final funding decision. Approved proposals have confirmed funding; declined proposals are formally rejected after Grant Program Director review.|

**Note:**

Admins can add, remove, relabel, reorder chart widgets and filter pills, or create custom ones in the **Spending Overview** panel. The two built-in charts can be hidden or relabeled but not deleted from the system. For more information, see [Configure the Spending Overview Widget and Filter pills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-config-spending-overview-widget.md).

## Data model

Rolling grant approvals introduce two new records and extend an existing one.

The **Funding Allocation Review Task** record represents a batch of proposals that the grant program manager has assembled and submitted to the Grant Program Director for review. The record stores the associated grant program and the recommendation reason for the batch. It also tracks the total number of proposals included, counts for funding and for decline, the total allocated amount, and the current state of the review task.

The **Funding Allocation Proposal Mapping** record links an individual proposal to a Funding Allocation Review Task, defining which proposals are part of each batch. When the mapping is active, the proposal is included in the allocation request. When inactive, the proposal has been removed or rejected from it. The Grant Program Director can add comments to each mapping to record the reasons for approving or rejecting a proposal as part of the review.

The existing **Grants Management Case** record gains new fields starting with Grants Management version 1.31. New fields include funding justification, references to the Funding Allocation Review Task the proposal belongs to, and submission counts for funding or decline consideration. A funding status field tracks the proposal's current position in the allocation workflow.

**Related topics**  


[Mark proposals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-rolling-grants-mark-proposals-task.md)

[Submit a Funding Allocation Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-rolling-grants-submit-fr-task.md)

[Review and Approve a Funding Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-review-fr-task.md)

[Release result notices to applicants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-release-result-notices-task.md)

[Grant Proposal funding statuses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-proposal-funding-status-ref.md)

[Configure the Spending Overview Widget and Filter pills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-config-spending-overview-widget.md)

[Grants Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-data-model-gm.md)

