---
title: Evaluate merchant analysis
description: Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution. When the ACH disputes AI agent workflow is enabled, an AI agent can perform this analysis automatically based on merchant reviews and past dispute history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/fso-ach-evaluate-merchant.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 3
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Evaluate merchant analysis

Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution. When the ACH disputes AI agent workflow is enabled, an AI agent can perform this analysis automatically based on merchant reviews and past dispute history.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector. If the Merchant analysis with AI agent is enabled, the now\_assist\_panel\_user role is also required.

## About this task

The Merchant analysis with AI agent can perform this evaluation for you if it is activated. The agent checks the merchant's credibility based on ratings and reviews from a web search and reviews past dispute history across all payment types. It then recommends an outcome that you can apply or follow up on. If a web search returns no results for a merchant, the merchant is classified as not credible. When the agent isn't enabled, evaluate the merchant analysis manually.

Ensure that your assignment logic, such as Advanced Work Assignment \(AWA\), is configured to assign all associated transactions to the same agent when a dispute case is assigned. This alignment helps maintain consistency and speeds up case resolution.

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

7.  Open the **Evaluate merchant analysis** task.

    If the AI agent is enabled and the task isn't yet assigned, select **Assign to me** to invoke the AI agent. If the task is already assigned to you, the agent's recommendation is displayed automatically.

    If the AI agent isn't enabled, in **Open Tasks**, select **Evaluate merchant analysis** to open the task manually.

8.  If the AI agent is enabled, review the agent's analysis and select one of these options on the workspace.

    -   **Apply Recommendation**: Accept the recommendation after reviewing the merchant analysis. The recommended **Outcome** and **Rationale** on the recommendation card component are copied to **Final action** and **Resolution reason** respectively, and the task closes automatically.
    -   **Ask a follow up**: Select this option only if you aren't sure about the analysis and want to verify further. The analysis is then displayed in the ServiceNow Otto panel. If you disagree with the analysis, the AI agent prompts you for a rationale for the disagreement before the task proceeds.
    **Note:** You can also access the AI agent's recommendation as follows:

    1.  Once you select **Assign to me**, a notification appears for you in the ServiceNow Otto panel.
    2.  Select the ServiceNow Otto icon \(\[Omitted image "icon-otto.png"\] Alt text: Otto icon.\) and open the active chat for the disputed transaction.
    3.  In the chat, the AI agent generates a recommendation for the dispute with a valid reason.
9.  If the AI agent isn't enabled, or you want to record the final action yourself, in **Merchant analysis action** indicate the final action:

    -   **Credible**: Upon analysis, the merchant is determined to be credible.
    -   **Not Credible**: Upon analysis, the merchant is determined to be not credible.
10. Close the task.

    This step happens automatically if the AI agent is enabled and you selected **Apply Recommendation**.


## Result

The **Final action** field is updated as **Credible** or **Not credible**. The task navigates to the next task, [Evaluate Nacha operating guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-evaluate-nacha.md).

**Parent Topic:**[Processing an ACH dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/process-dispute-ach.md)

