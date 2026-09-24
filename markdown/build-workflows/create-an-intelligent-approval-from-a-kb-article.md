---
title: Create an intelligent approval from a KB article
description: Generate an intelligent approval from an existing KB article.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/create-an-intelligent-approval-from-a-kb-article.html
release: brazil
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 3
keywords: [intelligent approvals, create intelligent approval, create from KB article, AI approval, publish policy]
breadcrumb: [Build intelligent approvals, Intelligent approvals, Build workflows]
---

# Create an intelligent approval from a KB article

Generate an intelligent approval from an existing KB article.

## Before you begin

-   Role required: sn\_iap.policy\_manager or sn\_iap.policy\_admin
-   Identify the number or title of a published KB article containing an approval policy.

## Procedure

1.  Navigate to **All** &gt; **Intelligent Approvals** &gt; **Intelligent Approvals Home**.

    \[Omitted image "example-create-iap-from-kb-01.png"\] Alt text: Intelligent approval homepage

2.  In the **Ask or search for anything** chat bar, type a request to create an intelligent approval.

    \[Omitted image "example-create-iap-from-kb-02.png"\] Alt text: Sample chat request to create an intelligent approval

    For example, type `Create an intelligent approval from KB0010002.`

3.  Follow the chat instructions to select the appropriate KB article.

    **Important:** The KB article must be published and accessible to you. You can search for a KB article by number, title, or a description. ServiceNow Otto will display potential KB articles that match your criteria.

    The system analyzes your policy document to determine what records the policy applies to, what conditions start the approval process, and the approvals conditions to apply.

    \[Omitted image "example-create-iap-from-kb-03.png"\] Alt text: Sample analysis of policy KB article

4.  Review the approval conditions of the intelligent approval.

    \[Omitted image "example-create-iap-from-kb-04.png"\] Alt text: Sample suggested table and approval conditions extracted from policy KB

    For example, intelligent approvals for change request records should use the change\_request table.

5.  Select **Edit** to see the conditions when the intelligent approval will make a decision.

    \[Omitted image "example-create-iap-from-kb-05.png"\] Alt text: Sample suggested conditions

    For example, an intelligent approval may review change request records when the State is Assess or when the State is Authorize, and when the Type is Normal or when the State is Emergency.

    Select **Define my own** to override the **Suggestion** scope and start conditions. Enter a description of the record types, field values, and start conditions that you want to use for this intelligent approval.

6.  When the approval conditions meet your criteria, select **Submit**.

    The system reviews your policy document and generates the intelligent approval. The generation process may take a moment to complete.

    \[Omitted image "example-create-iap-from-kb-06.png"\] Alt text: Intelligent approval generation status messages

7.  To review the details of the intelligent approval, select **Open preview**.

    \[Omitted image "example-create-iap-from-kb-07.png"\] Alt text: Link to open intelligent approval card

    The system displays the intelligent approval details card.

8.  Review the **Overview** and **Test results** tabs of your intelligent approval policy.

    \[Omitted image "example-create-iap-from-kb-08.png"\] Alt text: Intelligent approval Overview tab displaying a 100% rate of test approvals that can be automated

    A high percentage of **AI approved/rejected** results indicates that the policy document provides clear, consistent criteria for the system to evaluate. A high percentage of **Can't decide** results could indicate that the policy document requires human approval or that approval conditions need improvement.

    **Important:** AI-generated approvals and rejections may be inaccurate or inappropriate. Review the approval results before publishing the policy.

9.  Review the **Suggested improvements** tab.

    \[Omitted image "example-create-iap-from-kb-09.png"\] Alt text: Sample suggested improvements document

    The suggested improvements document contains items that you can add, edit, or remove from your policy source document.

10. From the PDF document viewer toolbar, select **Download** to save a PDF copy of the suggestions.

    \[Omitted image "example-create-iap-from-kb-09-a.png"\] Alt text: Option to download suggested improvements document

11. Use the suggested improvements to update the approval source policy document.

    Make edits to the source policy document outside your instance using an appropriate document editor application.

    **Important:** AI-generated suggestions may be inaccurate or inappropriate. Review the suggestions before changing the policy.

12. Upload the updated policy document, and review the percentage of **AI approved/rejected** results.

    For instructions on uploading a new source document, see [Update source document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/update-source-document.md).

13. Select the three-dot menu, and select **Potential overlapping approvals**.

    \[Omitted image "example-create-iap-from-kb-10.png"\] Alt text: Check for potential overlapping approvals

    \[Omitted image "example-create-iap-from-kb-10-a.png"\] Alt text: Empty list of potential overlapping intelligent approvals

    The system reviews your existing intelligent approvals to identify any potential approval conflicts.

    You can resolve overlapping intelligent approvals by one of these methods.

    -   You can leave your new intelligent approval in the draft state and update the existing intelligent approval to include the scope and coverage of your new intelligent approval. Choose this method when you want your existing intelligent approval to replace your new intelligent approval.
    -   You can deactivate the existing intelligent approval. Choose this method when you want your new intelligent approval to replace your existing intelligent approval.
14. When the percentage of **AI approved/rejected** results meets your requirements, select **Publish**.

    \[Omitted image "example-create-iap-from-kb-11.png"\] Alt text: Successfully Published banner message


## Result

\[Omitted image "example-create-iap-from-kb-12.png"\] Alt text: Intelligent approvals homepage with the Change Request Policy v1 card showing an active status

The intelligent approval policy is published and activated for all incoming requests that match the configured trigger conditions. The system evaluates matching requests as they are created and automatically approves or rejects requests that clearly meet the policy criteria. Requests that the system can't evaluate remain open for human reviewers to approve.

