---
title: Submit exceptions for Scan Engine findings
description: Developers can submit exception requests for Suggest, Review, Recommend, and Act level findings if they determine the finding should not be considered an issue to deter development. The availability of each finding level depends on the exception reason scope configured by your system administrator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/submitting-exception-reasons-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-21"
reading_time_minutes: 2
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Submit exceptions for Scan Engine findings

Developers can submit exception requests for Suggest, Review, Recommend, and Act level findings if they determine the finding should not be considered an issue to deter development. The availability of each finding level depends on the exception reason scope configured by your system administrator.

## Before you begin

Exceptions can be submitted for any finding level, Suggest, Review, Recommend, or Act, depending on the exception reason scope configured by your system administrator. Exceptions require approval from a user with the approval role. If the exception is approved, the finding is excluded from technical debt.

**Note:** The record under the Scanned Record field of the finding, sn\_se\_finding, record should be extending sys\_metadata table in order for the Scan Engine Exceptions UI action button to be available. For more information on configuring exception properties, refer to [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md).

Role required: sn\_se.scan\_engine\_admin, sn\_impact\_common.Impact Developer, or sn\_impact\_common.Impact App Admin

## Procedure

1.  From a summary scan record or an update set scan, use the **Findings** related list to view all findings discovered during a scan.

2.  When a finding is detected at a level with exceptions enabled, select **View finding details** in the summary banner to open the **Findings** panel.

3.  In the **Findings** panel, select the tab for the finding level you want to submit an exception for, such as Suggest, Review, Recommend, or Act.

    \[Omitted image "real-time-findings-request-exception-new.png"\] Alt text: A finding card in the Findings panel with the Create exception button.

4.  On the finding card, select **Create exception**.

5.  Enter the reason in the **Exception Reason** field for why an exception should be made for this finding.

6.  Choose how to proceed with your exception:

<table id="exception-button-states"><thead><tr><th>

Button

</th><th>

Purpose

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

**Save as draft**

</td><td>

-   Preserve your exception without submitting for approval.
-   You can edit and submit later.


</td><td>

Exception state set to Draft. Finding card displays the Draft badge. You can select **Update draft** or **Submit for approval** when ready.

</td></tr><tr><td>

**Submit for approval**

</td><td>

Send the exception to an exception approver for review and approval decision.

</td><td>

-   Exception state set to **Requested**.
-   Finding card displays the **Exception drafted** badge.
-   Exception is submitted for review and you can withdraw the request, if needed.


</td></tr></tbody>
</table>7.  Review your exception state on the finding card:

    -   **Exception drafted**: Draft created.
    -   Select **View exception reason** to modify your exception reason. or Submit for approval to send it for review. \[Omitted image "se-exceptions-submit-draft.png"\] Alt text: A finding card in draft state with the Exception drafted badge and View exception reason buttons.
    -   **Pending approval**: The finding card displays the Pending approval badge with the submission date.
    -   An approver will either approve or reject your exception. You can select **Withdraw request** to cancel the submission.

        \[Omitted image "se-exceptions-pending-withdraw-request.png"\] Alt text: A finding card in the pending approval state with the Pending approval badge and Withdraw request button.

    You receive notification of the approval decision. If approved, the finding card displays the **Approved** badge with the approval date and is excluded from technical debt calculations. If rejected, you can submit a new exception request or work to resolve the finding.

    **Note:** If the requester name or email notification does not display correctly in the exception record after submission, verify your user account is properly synchronized between development and production environments. The Scan Engine exception workflow requires consistent user identification across instances.


