---
title: Review ACH dispute return recommendation
description: Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action. When the ACH dispute return recommendation AI agent is enabled, it can analyze past disputes with similar transaction values and recommend an action for you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/fso-ach-review-recommendation.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 3
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review ACH dispute return recommendation

Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action. When the ACH dispute return recommendation AI agent is enabled, it can analyze past disputes with similar transaction values and recommend an action for you.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector. If the ACH dispute return recommendation AI agent is enabled, the now\_assist\_panel\_user role is also required.

## About this task

Once the merchant analysis has been conducted and Nacha guidelines have been analyzed, a final action must be taken on the ACH dispute. You can deny a refund, file a refund, or follow up with the Originating Depository Financial Institution \(ODFI\) before making a final decision.

**Note:** The ACH dispute return recommendation AI agent can review past disputes with similar transaction values and recommend an action — **Deny**, **File return**, or **Follow up with ODFI** — along with a reason for the recommendation. It applies predefined rules when historical data is limited. When this agent isn't enabled, determine the final action manually.

Ensure that your assignment logic, such as Advanced Work Assignment \(AWA\), is configured correctly. When a dispute case is assigned to an agent, all associated transactions are automatically assigned to the same agent. This alignment helps maintain consistency and speeds up case resolution.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  Open the **Review ACH dispute return recommendation** task.

    If the AI agent is enabled and the task isn't yet assigned, select **Assign to me** to invoke the AI agent. If the task is already assigned to you, the agent's recommendation is displayed automatically.

    If the AI agent isn't enabled, in **Open Tasks**, select **Review ACH dispute return recommendation** to open the task manually.

8.  If the AI agent is enabled, it prompts one of these actions:

    -   **Deny**
    -   **File Return**
    -   **Followup ODFI**
9.  Review the AI agent's analysis and select one of these options on the workspace.

    -   **Apply Recommendation**: Accept the recommendation after reviewing the analysis. The recommended **Outcome** and **Rationale** on the recommendation card component are copied to **Final action** and **Resolution reason** respectively, and the task closes automatically.
    -   **Ask a follow up**: Select this option only if you aren't sure about the analysis and want to verify further. The analysis is then displayed in the ServiceNow Otto panel.
    **Note:** You can also access the AI agent's recommendation as follows:

    1.  Select the ServiceNow Otto icon \(\[Omitted image "icon-otto.png"\] Alt text: Otto icon.\) and open the active chat for the disputed transaction.
    2.  In the chat, the AI agent generates a recommendation for the dispute with a rationale. If you disagree with the analysis, the AI agent prompts you for a rationale for the disagreement before the task proceeds.
10. If the AI agent isn't enabled, or you want to record the final action yourself, in **ACH dispute return recommendation action**, select the final action:

    1.  **Deny**: The ACH dispute is determined to be invalid and is denied. The provisional credit is either canceled or reversed, depending on whether the credit has already been issued.
    2.  **File return**: The ACH dispute is determined to be valid and meets eligibility for return. A refund is initiated.
    3.  **Follow up ODFI**: More information is required from the ODFI before a refund can be either denied or issued.
11. Close the task.

    This step happens automatically if the AI agent is enabled and you selected **Apply Recommendation**.


## Result

The **Final action** field is updated with one of the following options: **File return**, **Deny**, or **Followup ODFI**, and the process continues to the next task, [Dispute communication initiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-dispute-communication.md).

**Parent Topic:**[Processing an ACH dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/process-dispute-ach.md)

