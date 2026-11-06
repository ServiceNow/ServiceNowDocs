---
title: Submit exceptions for Scan Engine findings
description: Developers can submit exception requests for Suggest, Review, Recommend, and Act level findings if they determine the finding should not be considered an issue to deter development. The availability of each finding level depends on the exception reason scope configured by your system administrator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/submitting-exception-reasons-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 3
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Submit exceptions for Scan Engine findings

Developers can submit exception requests for Suggest, Review, Recommend, and Act level findings if they determine the finding should not be considered an issue to deter development. The availability of each finding level depends on the exception reason scope configured by your system administrator.

## Before you begin

Exceptions can be submitted for any finding level, Suggest, Review, Recommend, or Act, depending on the exception reason scope configured by your system administrator. Exceptions generally require approval from a user with the exception approval role. Certain settings configured by a system administrator can determine whether an exception is approved or rejected automatically. If the exception is approved, the finding is excluded from technical debt.

**Note:** The record under the Scanned Record field of the finding, sn\_se\_finding, record must extend the sys\_metadata table for the Create exception button, which comes from the Scan Engine Exceptions UI action, to be available. For more information on configuring exception properties, refer to [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-properties.md).

Role required: sn\_se.scan\_engine\_admin, sn\_impact\_common.Impact Developer, or sn\_impact\_common.Impact App Admin

## Procedure

1.  From a summary scan record or an update set scan, use the **Findings** related list to view all findings discovered during a scan.

2.  When a finding is detected at a level with exceptions enabled, select **View finding details** in the summary banner to open the **Findings** panel.

3.  In the **Findings** panel, select the tab for the finding level you want to submit an exception for, such as Suggest, Review, Recommend, or Act.

    \[Omitted image "real-time-findings-request-exception-new.png"\] Alt text: A finding card in the Findings panel with the Create exception button.

4.  On the finding card, select **Create exception**.

5.  Enter the reason in the **Exception Reason** field for why an exception should be made for this finding.

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

Exception state set to **Draft**. Finding card displays the Exception drafted badge. You can select **View exception reason** to update the reason, and then select **Save as Draft** or **Submit for Approval** when ready.

</td></tr><tr><td>

**Submit for Approval**

</td><td>

Send the exception to an exception approver for review and approval decision.

</td><td>

-   Exception state set to **Pending**.
-   Finding card displays the **Exception requested** badge.
-   Exception is submitted for review by an exception approver.


</td></tr></tbody>
</table>7.  Review your exception state on the finding card:

    -   **Exception drafted**: Draft created.
    -   Select **View exception reason** to modify your exception reason, or select **Submit for Approval** to send it for review. \[Omitted image "se-exceptions-submit-draft.png"\] Alt text: A finding card in draft state with the Exception drafted badge and View exception reason button.
    -   **Exception requested**: The finding card displays the Exception requested badge. Select **View exception reason** to see the reason you entered. The exception is read-only, and only an exception approver can open the exception record, using the **View exception record** button, to approve or reject it.
    -   An approver approves or rejects your exception.
    You receive notification of the approval decision. If approved, the finding card displays the **Exception approved** badge. The exception reason is read-only, and you can open it with the **View exception** button. If rejected, open the exception record and read **Rejection Comments** to see why. Then select **Update Exception Reason** to resubmit, or work to resolve the finding.

    **Note:** If the requester name or email notification does not display correctly in the exception record after submission, verify your user account is properly synchronized between development and production environments. The Scan Engine exception workflow requires consistent user identification across instances.


If the **Create exception** button doesn't appear on a finding card, check the following:

-   The Scan Engine Exceptions UI action was modified.
-   The exception reason scope doesn't include the level of the finding.
-   The scanned record of the finding was deleted.

