---
title: Review and act on cases with the HRBP productivity assistant
description: HR business partners can use the HRBP productivity assistant to review AI-generated summaries and recommendations for their assigned HR cases. They can approve, deny, defer, resume, or cancel a case without opening the case form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/review-hr-cases-pa.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 4
keywords: [HRBP productivity assistant, HR case, AI summary, resolution recommendation, open cases]
breadcrumb: [Use, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Review and act on cases with the HRBP productivity assistant

HR business partners can use the HRBP productivity assistant to review AI-generated summaries and recommendations for their assigned HR cases. They can approve, deny, defer, resume, or cancel a case without opening the case form.

## Before you begin

HR cases must be assigned to you, either through an HRBP data access rule or manually. For more information, see [Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

Role required: HR business partner \[sn\_hrbp\_hub.user\]

## About this task

The assistant returns only active HR cases that are assigned to you. The assistant uses the AI urgency recorded during enrichment, not the **Priority** field in the HR Case record, to determine which cases are urgent.

## Procedure

1.  Access the HRBP productivity assistant from the link in your weekly digest email, or from the EmployeeWorks Web App.

2.  Ask the assistant for the cases that you want to review.

<table id="choicetable_oq1_ylk_skc"><thead><tr><th align="left" id="d232925e139">

Option

</th><th align="left" id="d232925e142">

Description

</th></tr></thead><tbody><tr><td id="d232925e148">

**View your open cases**

</td><td>

Tell the assistant to show your open cases.For example, type `Show me my open cases`.

The assistant lists up to 10 cases at a time. Cases with critical or high AI urgency appear first, sorted by due date.

</td></tr><tr><td id="d232925e164">

**View more cases**

</td><td>

Tell the assistant to show the next set of cases.For example, type `Show me the next 10 cases`.

The assistant returns cases that it hasn't already shown in the conversation.

</td></tr><tr><td id="d232925e180">

**Find a specific case**

</td><td>

Tell the assistant the case number.For example, type `Show me HRC0001234`.

</td></tr><tr><td id="d232925e194">

**View cases pending your approval**

</td><td>

Tell the assistant to show the cases that are waiting for your approval.For example, type `Show me cases pending my approval`.

</td></tr></tbody>
</table>    If you have no open cases, the assistant tells you so.

    The assistant returns the cases that match your request.

3.  Ask the assistant about a specific case.

    For example, type `Tell me more about HRC0001234`. If enrichment on the case isn't complete, the assistant tells you that the case is still being processed.

    The assistant outputs a message that includes the following information:

    -   An AI-generated summary of the case.
    -   The recommendation and AI confidence score, except for Employee Relations cases.
    -   The approvers on the case, and whether the case is pending your approval.
4.  Ask the assistant follow-up questions about the recommendation.

    For example, type `How did you come up with the recommendation?`, `What criteria did you check?`, or `What's the history on this case?`.

5.  Compare the recommendation against the case record and your knowledge of the employee and the policy involved.

    The recommendation is a starting point, not a decision.

    **Important:** Always review AI-generated content for accuracy.

6.  Tell the assistant which action to take on the case.

<table id="choicetable_ng2_wqk_skc"><thead><tr><th align="left" id="d232925e279">

Option

</th><th align="left" id="d232925e282">

Description

</th></tr></thead><tbody><tr><td id="d232925e288">

**Approve a request**

</td><td>

Tell the assistant to approve the case.For example, type `Approve HRC0001234`.

If you aren't one of the required approvers, or if the case doesn't require approval, the assistant tells you so and doesn't change the case.

</td></tr><tr><td id="d232925e304">

**Decline a request**

</td><td>

Tell the assistant to decline the case and include a reason.For example, type `Decline HRC0001234 because the employee doesn't meet the eligibility criteria`.

If you don't include a reason, the assistant asks for one and doesn't decline the case until you provide it. The approver conditions for approving a request also apply.

</td></tr><tr><td id="d232925e320">

**Defer a case**

</td><td>

Tell the assistant to defer the case and include a reason.For example, type `Defer HRC0001234 because supporting documentation is missing`.

The assistant sets the **State** field in the HR Case record to **Suspended** and logs your reason as a work note. Deferring a case doesn't change any pending approval on the case. If you don't include a reason, the assistant asks for one.

</td></tr><tr><td id="d232925e345">

**Resume a deferred case**

</td><td>

Tell the assistant to resume the case.For example, type `Resume HRC0001234`.

The assistant sets the **State** field in the HR Case record to **Work in Progress**.

</td></tr><tr><td id="d232925e371">

**Cancel a case**

</td><td>

Tell the assistant to cancel the case.For example, type `Cancel HRC0001234`.

You can also type `Dismiss HRC0001234` or `End HRC0001234`. Canceling a case doesn't require a reason. The assistant sets the **State** field in the HR Case record to **Canceled**.

</td></tr></tbody>
</table>    If a case doesn't require approval, or isn't waiting for your approval, the assistant tells you that it can't approve or deny the case.

    Before the assistant approves, declines, defers, or cancels a case, it displays the case number, subject person, case type, action, and your reason for denying or deferring the case.

7.  Enter `Yes` to confirm the action.

    The assistant confirms that it completed the action.

8.  Select the case number in the conversation to verify the change on the case page.

    For more information, see [Work an HR case on the case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/work-hr-case-using-case-page.md).

    The case page opens in the side panel and displays the updated case state.


## Result

Your approval or denial is recorded on the case approval, or the **State** field in the HR Case record reflects the new state.

