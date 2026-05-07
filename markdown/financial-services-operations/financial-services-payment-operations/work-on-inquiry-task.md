---
title: Work on an inquiry task
description: Work on a payment inquiry task to request additional information that is related to an inquiry case from the recipient bank.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigate an inquiry case, Managing payment inquiries, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on an inquiry task

Work on a payment inquiry task to request additional information that is related to an inquiry case from the recipient bank.

## Before you begin

Role required: sn\_bom\_payment.inquiry\_agent or sn\_bom\_payment.inquiry\_agent\_connector

## About this task

An inquiry task is automatically generated for a Beneficiary Claim Non-Receipt - Internal case with an external recipient and assigned to the inquiry agent working on the case. However, for any internal follow-up, you can also create an ad hoc inquiry task for any type of inquiry.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Open the inquiry task from a payment inquiry case or from the **Inquiry Tasks** list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d73286e99">

Option

</th><th align="left" id="d73286e102">

Steps

</th></tr></thead><tbody><tr><td id="d73286e108">

**From a payment inquiry case**

</td><td>

1.  In the **Lists** tab, under **Payment Inquiry Cases**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Inquiry Tasks** tab and click the inquiry task.


</td></tr><tr><td id="d73286e141">

**From the __Inquiry Tasks__ list**

</td><td>

1.  In the **Lists** tab, under **Inquiry Tasks**, click **Assigned to me**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress** and send an email to the recipient bank requesting the required information for the case.

5.  If you've received the required information from the recipient bank via emails or any other interactions, attach these artifacts to the case.

6.  In the **Work notes** field, enter any comments or received information.

7.  In the **State** field, change the state of the task to **Closed Complete** to close the task.

8.  Click **Save**.


## What to do next

-   After you've received the requested information from the recipient bank and you've closed the inquiry task, update the associated inquiry case as per the received information.
-   Change the state of the associated case to **Work in Progress** and work on the case to resolve it.

    **Note:** If the inquiry case is not resolved or closed within the number of days that are mentioned in the **sn\_bom\_payment.inquiry\_task\_folow\_up\_interval\_in\_days** [payment property](../reference/properties-installed-with-payment-operations.md), the system creates another follow-up inquiry task for the case.


**Parent Topic:**[Investigate a payment inquiry case](investigate-payment-inquiry-case.md)

