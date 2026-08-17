---
title: Evaluate Nacha operating guidelines
description: Evaluate the Nacha operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement. When enabled, the Nacha operating guidelines check AI agent can verify eligibility automatically based on documents such as a valid Written Statement of Unauthorized Debit \(WSUD\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/fso-ach-evaluate-nacha.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 4
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Evaluate Nacha operating guidelines

Evaluate the Nacha operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement. When enabled, the Nacha operating guidelines check AI agent can verify eligibility automatically based on documents such as a valid Written Statement of Unauthorized Debit \(WSUD\).

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector. If the Nacha operating guidelines check AI agent is enabled, the now\_assist\_panel\_user role is also required.

## About this task

Nacha governs the ACH network, which processes electronic payments like payroll, bill payments, and direct deposits in the United States of America. The Nacha Operating Rules and Guidelines establish compliance requirements for all disputed ACH transactions.

This task is dependent on the Dispute Rules Content Pack for Nacha plugin.

The Dispute Rules Content Pack for Nacha includes a Knowledge Base article that contains a table of reason codes and the corresponding eligibility rules.

To access the knowledge base article:

1.  Navigate to **All** &gt; **Knowledge Center**.
2.  Navigate to the knowledge base Dispute Compliance Documents.
3.  Open the knowledge base article Nacha Operating Guidelines for Return Codes.

**Note:** When the Nacha operating guidelines check AI agent is enabled, it can perform this evaluation for you, using the same knowledge article installed with the Dispute Rules Content Pack for Nacha to verify required documentation and confirm actions occur within the allowed time frames. To enable this capability, make sure that the AI Search option is turned on. See [Using Dispute Rules Content Pack for Nacha](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-rules-content-pack-nacha-use.md) for more information about the content pack. When the Nacha operating guidelines check AI agent isn't enabled, use the knowledge base article earlier to evaluate the guidelines manually.

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

7.  Open the **Evaluate Nacha operating guidelines** task.

    If the AI agent is enabled and the task isn't yet assigned, select **Assign to me** to invoke the AI agent. If the task is already assigned to you, the agent's recommendation is displayed automatically.

    If the AI agent isn't enabled, in **Open Tasks**, select **Evaluate Nacha operating guidelines** to open the task manually.

8.  If the AI agent is enabled, review the agent's analysis and select one of these options on the workspace.

    -   **Apply Recommendation**: Accept the recommendation after reviewing the Nacha operating guidelines analysis. The recommended **Outcome** and **Rationale** on the recommendation card component are copied to **Final action** and **Resolution reason** respectively, and the task closes automatically.
    -   **Ask a follow up**: Select this option only if you aren't sure about the analysis and want to verify further. The analysis is then displayed in the ServiceNow Otto panel. If you disagree with the analysis, the AI agent prompts you for a rationale for the disagreement before the task proceeds.
    **Note:** You can also access the AI agent's recommendation as follows:

    1.  Once you select **Assign to me**, a notification appears for you in the ServiceNow Otto panel.
    2.  Select the ServiceNow Otto icon \(\[Omitted image "icon-otto.png"\] Alt text: Otto icon.\) and open the active chat for the disputed transaction.
9.  If the AI agent isn't enabled, or you want to record the final action yourself, update **Nacha eligibility action** to indicate the final action.

    -   **Eligible**: This dispute is considered eligible under Nacha guidelines.
    -   **Ineligible**: This dispute is considered ineligible under Nacha guidelines.
10. Enter a resolution reason.

    This step isn't needed if the AI agent is enabled and you selected **Apply Recommendation**, since the AI agent's rationale is copied into **Resolution reason** automatically.

11. Close the task.

    This step happens automatically if the AI agent is enabled and you selected **Apply Recommendation**.


## Result

The **Final action** field is updated as **Eligible** or **Ineligible**. The task navigates to the next task, [Review ACH dispute return recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-review-recommendation.md).

**Parent Topic:**[Processing an ACH dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/process-dispute-ach.md)

**Related topics**  


[Dispute Reason Codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/components-installed-with-dispute-rules-content-pack-for-nacha.md)

