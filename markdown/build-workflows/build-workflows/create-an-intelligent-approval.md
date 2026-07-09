---
title: Create an intelligent approval
description: Generate an intelligent approval policy from an existing policy document.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 4
keywords: [intelligent approvals, create approval policy, upload policy document, AI approval, publish policy]
---

# Create an intelligent approval

Generate an intelligent approval policy from an existing policy document.

## Before you begin

Role required: sn\_iap.policy\_manager or sn\_iap.policy\_admin

## Procedure

1.  Navigate to **All** &gt; **Intelligent Approvals** &gt; **Intelligent Approvals Home**.

    \[Omitted image "intelligent-approval-create-01.png"\] Alt text: Intelligent approval homepage

2.  Select **Create new**.

3.  Select the existing policy document that you want to upload.

    \[Omitted image "intelligent-approval-create-02.png"\] Alt text: Create intelligent approval dialog to upload document

    The policy document must be in a PDF format, and the file size must be 10 MB or less.

4.  Verify the name of your source policy document, and select **Create intelligent approval**.

    \[Omitted image "intelligent-approval-create-03.png"\] Alt text: Create intelligent approval dialog to create from document

    The system analyzes your policy document to determine what records the policy applies to, what conditions start the approval process, and the approvals conditions to apply.

    \[Omitted image "intelligent-approval-create-04.png"\] Alt text: Sample analysis of policy document

5.  Review the intelligent approvals scope and trigger conditions.

    \[Omitted image "intelligent-approval-create-05.png"\] Alt text: Choose scope and coverage dialog box

    The system displays a **Suggested options** tab with a text description of the record types that the intelligent approval applies to and the approval start conditions.

    **Important:** Review the AI-generated trigger conditions carefully, as outputs may be inaccurate or incomplete.

    Select the **Define my own** tab to override the **Suggested options** scope and start conditions. Enter a description of the record types, field values, and start conditions that you want to use for this intelligent approval.

    \[Omitted image "intelligent-approval-create-05-0A.png"\] Alt text: Define my own text box option with the tooltip, "Describe in your own words what kind of requests you want to apply this intelligent approval to."

6.  Select either the **Suggested options** or **Define my own** descriptive text, and then select **Next**.

    \[Omitted image "intelligent-approval-create-06.png"\] Alt text: Sample Suggested options descriptive text for a Change Request policy

    The system reviews your policy document and generates the intelligent approval. The generation process may take a moment to complete.

    \[Omitted image "intelligent-approval-create-07.png"\] Alt text: Intelligent approval generation status messages

    If the system fails to generate intelligent approvals, verify that you have access permissions to both intelligent approvals and the system records that you want approved. For requirements, see [Configure intelligent approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/configure-intelligent-approvals.md).

7.  Review the **Overview** and **Test results** tabs of your intelligent approval policy.

    \[Omitted image "intelligent-approval-create-09.png"\] Alt text: Intelligent approval Overview tab displaying a 73% rate of test approvals that can be automated

    A high percentage of **AI approved/rejected** results indicates that the policy document provides clear, consistent criteria for the system to evaluate. A high percentage of **Can't decide** results indicates that the policy document needs improvement.

    **Important:** AI-generated approvals and rejections may be inaccurate or inappropriate. Review the approval results before publishing the policy.

8.  Review the **Suggested improvements** tab.

    \[Omitted image "intelligent-approval-create-09-0D.png"\] Alt text: Sample suggested improvements document

    The suggested improvements document contains items that you can add, edit, or remove from your policy source document.

9.  From the PDF document viewer toolbar, select **Download** to save a PDF copy of the suggestions.

    \[Omitted image "intelligent-approval-create-09-0E.png"\] Alt text: Option to download suggested improvements document

10. Use the suggested improvements to update the approval source policy document.

    Make edits to the source policy document outside your instance using an appropriate document editor application.

    **Important:** AI-generated suggestions may be inaccurate or inappropriate. Review the suggestions before changing the policy.

11. Upload the updated policy document, and review the percentage of **AI approved/rejected** results.

    For instructions on uploading a new source document, see [Update source document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/update-source-document.md).

12. Select the three-dot menu, and select **Potential overlapping approvals**.

    \[Omitted image "intelligent-approval-create-10.png"\] Alt text: Check for potential overlapping approvals

    \[Omitted image "intelligent-approval-create-10-0A.png"\] Alt text: Empty list of potential overlapping intelligent approvals

    The system reviews your existing intelligent approvals to identify any potential approval conflicts.

    You can resolve overlapping intelligent approvals by one of these methods.

    -   You can leave your new intelligent approval in the draft state and update the existing intelligent approval to include the scope and coverage of your new intelligent approval. Choose this method when you want your existing intelligent approval to replace your new intelligent approval.
    -   You can deactivate the existing intelligent approval. Choose this method when you want your new intelligent approval to replace your existing intelligent approval.
13. When the percentage of **AI approved/rejected** results meets your requirements, select **Publish**.

    \[Omitted image "intelligent-approval-create-11.png"\] Alt text: Successfully Published banner message


## Result

\[Omitted image "intelligent-approval-create-12.png"\] Alt text: Intelligent approvals homepage with the Change Request Policy v1 card showing an active status

The intelligent approval policy is published and activated for all incoming requests that match the configured trigger conditions. The system evaluates matching requests as they are created and automatically approves or rejects requests that clearly meet the policy criteria. Requests that the system can't evaluate are routed to human reviewers for approval.

If intelligent approvals don't start when expected, verify the intelligent approvals start conditions. Use the **Define my own** option to override the suggested options.

If too many intelligent approvals result in a **Can't decide** decision, review and update your policy document. Load your updated policy and use the suggested improvements to raise the percentage of **AI approved/rejected** results.

