---
title: Supplier credit card enablement playbook
description: Source-to-Pay Workspace includes a playbook to complete the supplier cases for initiating credit card acceptance requests.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Supplier Payment Optimization, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier credit card enablement playbook

Source-to-Pay Workspace includes a playbook to complete the supplier cases for initiating credit card acceptance requests.

The Supplier credit card enablement playbook provides step-by-step guidance for completing the request. The playbook includes a customized supplier case flow including reviewing the case by checking the propensity score, creating the credit card acceptance task for the supplier contact, and notifying the supplier through email. Once the supplier contact accepts the credit card as the payment method, the case can be closed. For more information, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Supplier credit card enablement playbook stages and activities

The playbook contains the following stages and activities.

<table id="table_bgd_tzx_ztb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td rowspan="2">

Review the case

</td><td>

Assign case

</td><td>

As a supplier manager or fulfiller, you can assign the case to a different person or keep the case assigned to you.You can do the following:

1.  In the **Assigned to** search field, search for and select the person that you want to assign the case to.
2.  In the **Short description** field, update the description for the case.
3.  Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.

 ![Supplier credit card enablement playbook assign and review step.](../image/credit-card-playbook1.png)

</td></tr><tr><td>

Review supplier propensity score

</td><td>

As a supplier manager or fulfiller, you can approve or cancel the case after reviewing the propensity score available for this supplier.![Supplier credit card enablement playbook review propensity score step.](../image/credit-card-playbook2.png)

</td></tr><tr><td rowspan="2">

Notify the supplier

</td><td>

Create credit card acceptance task

</td><td>

A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text informing them about the benefits of accepting credit card payments. Ensure that the email template remains editable.![Supplier credit card enablement playbook review propensity score step.](../image/credit-card-playbook3.png)

**Note:** Do not modify the task button, as any changes may cause the link to stop functioning.

</td></tr><tr><td>

Notify the supplier

</td><td>

Send an email to the supplier informing that the credit card acceptance request has been initiated.Once the email is sent, a task is created for the supplier contact to review and approve the credit card acceptance request.

</td></tr><tr><td>

Waiting for the supplier to decide on credit card acceptance

</td><td>

Check the status

</td><td>

The supplier contact reviews and approves the credit card acceptance request from the Supplier Collaboration Portal after providing the terminal ID and uploading the bank account proof document.![Supplier accepts or rejects credit card request from Collaboration portal](../image/supplier-accept-cc.png)

</td></tr><tr><td>

Process change request

</td><td>

Close case

</td><td>

You can select **Mark complete** and **Complete case** to close the request. Updates the case to Closed Completed.![Supplier credit card enablement playbook review propensity score step.](../image/credit-card-playbook4.png)

</td></tr></tbody>
</table>**Parent Topic:**[Using Supplier Payment Optimization](using-supp-payment-opt.md)

**Related topics**  


[Manage supplier cases from the Source-to-Pay Workspace](managing-cases.md)

[Configure due dates for supplier cases](../task/configure-case-due-date.md)

[Playbook for updating the supplier primary data](primary-playbook-cases.md)

[Create a case on behalf of a supplier from the Source-to-Pay Workspace](../task/create-new-supplier-case.md)

