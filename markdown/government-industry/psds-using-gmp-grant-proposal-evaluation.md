---
title: Evaluate a grant proposal in the Grants Management Grants Proposal Playbook
description: Create and assign merit review tasks and allocate budgets and propose funding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-using-gmp-grant-proposal-evaluation.html
release: australia
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 3
breadcrumb: [Grants Management Proposal Playbook, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Evaluate a grant proposal in the Grants Management Grants Proposal Playbook

Create and assign merit review tasks and allocate budgets and propose funding.

The Evaluation stage of the grants proposal playbook consists of two tasks: **Conduct merit review\(s\)** and **Build funding proposal**.

**Note:** From Grants management version 1.31, the **Build funding proposal** activity is renamed to **Funding allocation**.

In the evaluation stage, the grants program manager oversees, tracks, and manages the reviews across the proposal.

In the **Conduct merit review\(s\)** activity, the grants program manager selects a reviewer group and reviewers and creates merit review tasks for each person in the group. The grants program manager then tracks the reviews across the proposal, monitoring the state, score flag, and the time remaining to complete the review task. When the merit review is complete and the grants proposal is scored and ranked, the merit review activity auto-completes and advances to the **Build funding proposal** activity.

In the **Build funding proposal** activity, the funding information is updated based on the inputs and submissions by the merit reviewers. Grant proposals are compared and budgets are allocated. The grants program manager then either submits funding proposals to the grants program director for further approval or declines the proposal with reasons. The status of the proposals is updated to reflect the grants program director's decisions and the applicants are notified about the outcome.

**Procedure**:

1.  Navigate to **All &gt;** &gt; **CSM Configurable Workspace**.
2.  Navigate to **Lists &gt;** &gt; **Grant Proposals** and select **My grant proposals**.
3.  Select the grant proposal and navigate to **Evaluation**.
4.  In the **Conduct merit review\(s\)** task, select the reviewer group from the drop-down and select **Create Tasks**.

    A review task is created for each of the reviewers from the selected review group. The reviewer groups are created by the grants program manager during the grant setup stage.

5.  Review or edit the reviewers and select **Update Review Tasks**.The grants program manager can edit the reviewer group at any time before any one review task is complete.
6.  Assign the review tasks and notify the selected reviewers by selecting the review tasks and select**Release Tasks**.

    The state of the selected review tasks is now In progress and the reviewers receive notifications on the Reviewer Service Portal.

7.  Review and manage the merit review tasks across the grant proposals by selecting **View all reviewers for this program** and switch to the workspace view by selecting the Record Details icon \[Omitted image "psds-gmp-record-details.png"\] Alt text: Record details icon..
8.  Move all the selected review tasks back to Draft state by selecting **Reset State**.

    If a reviewer declines, the grants program manager is notified. The grants program manager can cancel that review and move the task to the next stage, or assign a new review group to restart the review process.

    When all the review tasks are complete, the playbook automatically advances to the Build funding recommendation task.

    The grants program manager can track the progress of the funding status and view requested budget, allocated budget, and the rank based on the merit review scoring.

9.  In the **Build funding proposal** task, review and manage the funding proposals by selecting **View funding proposal**.

    All the scored proposals appear in the Funding proposal tab along with the ranks and budget details.

    **Note:** From Grants management version 1.31, the **Build funding proposal** activity is renamed to **Funding allocation** to support the [Rolling grant approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-rolling-grant-approvals-concept.md) feature. To allocate budget for the proposals in a rolling grants approval workflow, see [Mark proposals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-rolling-grants-mark-proposals-task.md).

10. From the list of scored proposals, select one or more proposals to perform either of these actions:
    -   Decline funding and provide a reason by selecting **Propose Decline**.
    -   View the funding proposal page from where you can allocate budget, submit the proposals, and notify the grant program director for further approval by selecting **Add to Proposal**.
11. As the grants program director, view the funding proposals in the CSM Configurable Workspace by navigating to **List** &gt; **My approvals**.
12. From the list of available funding proposals, as the grants program director, select one or more proposals to perform either of these actions.
    -   Decline funding and provide a reason by selecting **Reject**.
    -   Award the grant by selecting **Approve**.

When the grants program director approves the funding proposal, the evaluation stage is complete and the grant proposal advances to the Decision stage.

**Related topics**  


[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-release-merit-review-tasks.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-release-merit-review-tasks.md)

