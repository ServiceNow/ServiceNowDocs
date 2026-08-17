---
title: Close an invoice inquiry case
description: Close an invoice inquiry case when all the activities and tasks for resolving the case are completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/close-inquiry-case.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Invoice inquiry cases, Using Invoice Case Management, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Close an invoice inquiry case

Close an invoice inquiry case when all the activities and tasks for resolving the case are completed.

## Before you begin

Role required: sn\_ap\_cm.agent or sn\_ap\_cm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My Work** &gt; **Open cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **Cases**.
4.  In the Number column, select the link to the case to open it.

5.  Do one of the following:

    -   Select **Close inquiry**.

        The Close inquiry dialog box is displayed.

    -   Select the down arrow icon \(\[Omitted image "down-arrow-icon.png"\] Alt text: Down arrow icon\) and then select **Close incomplete**.\[Omitted image "apo-close-invoice-inquiry-case.png"\] Alt text: Close an invoice inquiry case

        The Closure details dialog box is displayed.

6.  From the Closure code list, select one of the following options:

    -   **Duplicate request**
    -   **Canceled/False inquiry**
    -   **Canceled by requester**
    -   **Information provided**
    -   **Exceptions resolved**
7.  In the **Closure details** field, enter the reason why you're closing the case.

    **Note:** This field is required when you close an invoice inquiry case as **Close incomplete**.

8.  Select **OK**.

    Depending on the option that you selected in step 5, the state of the case updates to Close complete or Closed incomplete.


## Result

The invoice inquiry case is closed after completing all activities and tasks required for resolution.

**Parent Topic:**[Invoice inquiry cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-inquiry-cases.md)

**Related topics**  


[Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md)

[Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-workspace.md)

[Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/apo-docintel-integration.md)

[Use ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/using-now-assist-apo.md)

[Using Supplier Collaboration Portal in APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/using-supplier-collaboration-portal.md)

