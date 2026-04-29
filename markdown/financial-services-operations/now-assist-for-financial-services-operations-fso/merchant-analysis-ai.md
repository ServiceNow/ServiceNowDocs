---
title: Merchant analysis with AI agent
description: The Merchant analysis for disputes AI agent checks the credibility of the merchant in the context of the dispute, based on ratings and reviews from web search. If a web search returns no results for a merchant, then the merchant is classified as not credible.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resolve ACH disputes with AI agents, ACH dispute AI agents overview, AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Merchant analysis with AI agent

The Merchant analysis for disputes AI agent checks the credibility of the merchant in the context of the dispute, based on ratings and reviews from web search. If a web search returns no results for a merchant, then the merchant is classified as not credible.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.dispute\_agent, and now\_assist\_panel\_user.

## About this task

This agent retrieves dispute task details, performs a web search to assess merchant credibility, and provides a recommendation, which the dispute agent accepts or rejects.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a card dispute.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case you want to work on.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  If the task isn’t assigned to an agent and once the dispute agent selects **Assign to me** the AI agent is invoked.

    If the task is already assigned to the dispute agent, then the recommendations provided by the AI agent are automatically displayed.

8.  Based on the AI agent's analysis, the dispute agent can select these options on the workspace.

    -   **Apply Recommendation**: The dispute agent selects this option to accept the recommendation after reviewing the merchant analysis.
    -   **Ask a follow up**: The dispute agent selects this option only if they aren’t sure about the analysis done and want to verify further. The analysis is then displayed in the Now Assist panel.
9.  Merchant analysis is performed in two parts: evaluating web credibility based on reviews associated with the merchant name, and reviewing past dispute history across all payment types.

10. Once the dispute agent selects **Apply Recommendation** option for the selected transaction, the recommended **Outcome** and **Rationale** on the recommendation card component are copied to the **Final action** and **Resolution reason** respectively and the task is closed.

    **Note:** You can also access the recommendation for the merchant analysis as follows.

    1.  Once the dispute agent selects **Assign to me**, a notification appears for that agent in the Now Assist.
    2.  Select the Now Assist panel icon \(![now assist panel icon](../../../common/image/icon-ai-sparkle.png)\) and open the active chat for the disputed transaction.
    3.  In the chat, the AI agent generates a recommendation for the dispute with a valid reason.

        If the dispute agent disagrees with the analysis, then a rationale is prompted by the AI agent for the disagreement. On providing a valid rationale, the task proceeds to the next task.

    ![Evaluate merchant analysis AI agent in ACH disputes](../image/now-assist-merchant-analysis.png)

11. Once the dispute agent selects the appropriate action, the **Merchant analysis action** is updated with the **Final action** and **Resolution reason**.

    For information about evaluate merchant analysis in ACH disputes, see [Evaluate merchant analysis](../../fso-card-operations/task/fso-ach-evaluate-merchant.md).


## Result

Based on the response from the dispute agent, the **Final action** field is updated as **Credible** or **Not credible**. The task navigates to the next task, [Evaluate Nacha operating guidelines with AI agent](nacha-guidelines-ai.md).

**Parent Topic:**[Resolve ACH disputes with AI agents](resolve-ach-disputes-with-ai-agents.md)

