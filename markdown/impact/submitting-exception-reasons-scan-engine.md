---
title: Submit exceptions for Scan Engine findings
description: Developers can submit exception requests for scan engine findings that don't require remediation. The finding levels available for exceptions depend on the exception reason scope configured by your system administrator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/submitting-exception-reasons-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 4
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Submit exceptions for Scan Engine findings

Developers can submit exception requests for scan engine findings that don't require remediation. The finding levels available for exceptions depend on the exception reason scope configured by your system administrator.

## Before you begin

Exceptions require approval from a user with the exception approval role. Depending on re-evaluation settings, an approved exception can carry forward automatically when the same issue is found again. If approved, the finding is excluded from technical debt. See [Exception handling in Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-handling-overview.md) for additional information.

**Note:** The record under the Scanned Record field of the finding, sn\_se\_finding, record must extend the sys\_metadata table for the Create exception button, which comes from the Scan Engine Exceptions UI action, to be available. For more information on configuring exception properties, refer to [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md).

Role required: sn\_se.scan\_engine\_admin, sn\_impact\_common.Impact Developer, or sn\_impact\_common.Impact App Admin

## Procedure

1.  From a summary scan record or an update set scan, use the **Findings** related list to view all findings discovered during a scan.

2.  When a finding is detected at a level with exceptions enabled, select **View finding details** in the summary banner to open the **Findings** panel.

3.  In the **Findings** panel, select the tab for the finding level you want to submit an exception for, such as Suggest, Review, Recommend, or Act.

    \[Omitted image "real-time-findings-request-exception-new.png"\] Alt text: A finding card in the Findings panel with the Create exception button.

4.  On the finding card, select **Create exception**.

5.  Enter the reason in the **Reason for exception** field for why an exception should be made for this finding.

6.  Choose how to proceed with your exception.

<table id="exception-button-states"><thead><tr><th>

Button

</th><th>

Purpose

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

**Save as Draft**

</td><td>

-   Preserve your exception without submitting for approval.
-   You can edit and submit later.


</td><td>

Exception state set to **Not Yet Requested**. Finding card displays the Exception drafted badge. You can select **View exception reason** to update the reason, and then select **Save as Draft** or **Submit for Approval** when ready.

</td></tr><tr><td>

**Submit for Approval**

</td><td>

Send the exception to an exception approver for review and approval decision.

</td><td>

-   Exception state set to **Requested**.
-   Finding card displays the **Exception requested** badge.
-   Exception is submitted for review by an exception approver.


</td></tr></tbody>
</table>7.  Review your exception state on the finding card:

    -   **Exception drafted**: Draft created.
    -   Select **View exception reason** to modify your exception reason, or select **Submit for Approval** to send it for review.

        \[Omitted image "se-exceptions-submit-draft.png"\] Alt text: A finding card in draft state with the Exception drafted badge and View exception reason button.

    -   **Exception requested**: The finding card displays the Exception requested badge. Select **View exception reason** to see the reason you entered. The exception is read-only.

        \[Omitted image "se-exceptions-requested-card.png"\] Alt text: A finding card in the requested state with the Exception requested badge and View exception reason button.

    -   An approver approves or rejects your exception. Only an exception approver can approve or reject it, using the **Approve/reject exception** button in the **View exception** panel. See [Approve or reject exception requests for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/approving-exception-requests-scan-engine.md) for details.
    -   You receive notification of the approval decision.
<table id="table-exception-decision-outcomes"><thead><tr><th>

Decision

</th><th>

Finding card

</th><th>

Next steps

</th></tr></thead><tbody><tr><td>

**Approved**

</td><td>

Displays the **Exception approved** badge.

</td><td>

The exception reason is read-only. Select **View exception** to open it.

</td></tr><tr><td>

**Rejected**

</td><td>

Displays the **Exception rejected** badge.

</td><td>

-   Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **All exceptions**, select **Rejected** in the **State** column, and open the exception reason to view the **Rejection Comments**.
-   To resubmit, select **Update Exception Reason** on the finding card, update the reason, and select **Save as Draft** or **Submit for Approval**.


</td></tr></tbody>
</table>    \[Omitted image "exception-approved.png"\] Alt text: A finding card in the approved state with the Exception approved badge and View exception button.

    \[Omitted image "se-exception-reason-rejected-edit-reason.png"\] Alt text: A finding card in the rejected state with the Exception rejected badge and Update Exception Reason button.

    **Note:** If the exception was rejected, select **Update Exception Reason**, modify the request, and then **Submit for Approval**.

    \[Omitted image "se-exception-reason-rejected-edit.png"\] Alt text: The Create exception form with a message that the exception reason was rejected, and the Return, Save as Draft, and Submit for Approval buttons.


-   If the **Create exception** button doesn't appear on a finding card, check if the exception reason scope doesn't include the level of the finding.
-   If the requester name or email notification does not display correctly in the exception record after submission, verify your user account is properly synchronized between development and production environments. The Scan Engine exception workflow requires consistent user identification across instances.

