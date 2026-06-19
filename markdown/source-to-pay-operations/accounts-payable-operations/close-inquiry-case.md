---
title: Close an invoice inquiry case
description: Mark an invoice inquiry case as resolved after completing all necessary activities and tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/close-inquiry-case.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, invoice inquiry case]
breadcrumb: [Invoice inquiry cases, Using Invoice Case Management, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Close an invoice inquiry case

Mark an invoice inquiry case as resolved after completing all necessary activities and tasks.

## Before you begin

Role required: sn\_ap\_cm.agent or sn\_ap\_cm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice inquiry cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice inquiry cases**.
4.  In the Number column, select the link to the case to open it.

5.  Do one of the following:

    -   Select **Close inquiry**.

        The Close inquiry dialog box is displayed.

    -   Select the down arrow icon \(\[Omitted image "down-arrow-icon.png"\] Alt text: Down arrow icon\) and then select **Close incomplete**.

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


**Parent Topic:**[Invoice inquiry cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-inquiry-cases.md)

