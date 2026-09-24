---
title: Reviewing an Approval Request
description: Review an approval request form to perform the required action according to the role assigned to you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-review-approval-request.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Unified Approvals View, Use, Unified Security Exposure Management, Security Operations]
---

# Reviewing an Approval Request

Review an approval request form to perform the required action according to the role assigned to you.

## Before you begin

Role required: sn\_sec\_exception.approver, sn\_sec\_exception.admin

## About this task

## Procedure

1.  The default list displays approvals in the **All Approvals** list view.

2.  Or you can select request from the **Pending approvals** or **Today's approvals**.

3.  Select a request to review details such as requester information, remediation details, exception request history, and approval history \(previous actions, comments, approvers\).

4.  Select the Approval History or Activity Stream option from the side panel associated with this request, to review the request history.

    The system displays the five most recent approved or rejected records for this request type in the Approval History tab, enabling you to make an informed decision. Additionally, in the Activity tab you can enter a comment, view work notes, and the input stream in this section. Select the stack mode toggle to view Comments, Work Notes, and Activity stream all in one view.

5.  Select **Now Assist Recommendation** option from the side panel to generate tailored recommendations for this request.

    **Note:** Now Assist analyses risk rating, request details, questionnaire answers, vulnerability, and asset information for a request to provide Approve or Reject recommendations, confidence score, and reasoning to the approvers. For more information, see: [Generate approval recommendations with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-approval-recommendation-skill.md)

    The recommendation panel shows three elements:

    -   **Recommendation** — either **Approve** or **Reject**, derived from the analyzed inputs.
    -   **Confidence score** — a percentage indicating how strongly the model agrees with its own recommendation. Scores at or above 80% indicate high agreement; scores between 50% and 80% indicate moderate agreement; scores below 50% indicate low agreement and signal that the request likely needs deeper human review.
    -   **Reasoning** — a short explanation citing which inputs drove the recommendation \(for example, "High risk rating combined with weak compensating-control evidence"\).
    Now Assist recommendations are decision aids, not approvals. The final approve or reject action is always yours. Apply additional scrutiny to low-confidence recommendations and to recommendations that contradict your own initial reading of the request.

6.  Select Approve or Reject at the top-right corner of the form, if you’re the assigned Approver for that request.

    To process multiple requests simultaneously, use **Bulk Approve** or **Bulk Reject** from the approvals list view. Only requests in the Requested state are affected.

7.  Navigate to completed records using the links provided in the form.

    Approved or rejected items are moved from the open to the completed section.

8.  If there are remaining legacy approvals, select the “Old Approvals List” link at the top of the page to view and act on those items.

    **Note:** Approvers receive notifications or reminders for pending requests based on system configuration.


