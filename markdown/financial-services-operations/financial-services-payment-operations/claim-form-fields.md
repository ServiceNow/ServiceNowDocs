---
title: Field descriptions for a claim case
description: Claim cases help the claim agents resolve payment claim requests that they receive from the bank's customers or third-party banks.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Financial Services Payment Operations reference, Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Field descriptions for a claim case

Claim cases help the claim agents resolve payment claim requests that they receive from the bank's customers or third-party banks.

When a claim request is submitted, it creates a claim case. Some of the fields on the case form are populated from the request from which the claim is created.

After the case is assigned, a claim agent fills out the fields on the case when dealing with the next steps. The next steps could include investigating the case, requesting a refund from a bank or customer, and completing the refund.

## Details tab fields for a claim case

The **Details** tab on the form provides case-related information.

<table id="table_xw5_vpd_pkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the case.-   **Internal**: Comes from a customer of the bank.
-   **External**: Comes from a third-party bank

</td></tr><tr><td>

Claim type

</td><td>

Type of claim case. -   **Internal**: Request came from a customer of the bank.
-   **External**: Request came from a third-party bank.

 The claim type determines which flow to trigger and the form view to show.

</td></tr><tr><td>

Refund type

</td><td>

Option to indicate from where to get the refund for the claim.-   **Internal**: Refund is made by the bank internally such as by a customer or the bank itself.
-   **External**: Refund comes from a third-party bank.

</td></tr><tr><td>

Error type

</td><td>

Type of error indicating if it was due to the customer or bank. Usually, this field determines the best course for resolving the claim.

</td></tr><tr><td>

Error category

</td><td>

Error category for the claim. This list contains the industry-standard error categories that are based on the selected error type.

</td></tr><tr><td>

Error subcategory

</td><td>

Error subcategory for the claim. This list contains the industry-standard error subcategories that are based on the selected error category.

</td></tr><tr><td>

State

</td><td>

State of the case.

</td></tr><tr><td>

Assignment group

</td><td>

User group that can work on the case. If the case is not assigned to a user yet, any member of the this group can work on the case.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the case.

</td></tr><tr><td>

Payment inquiry

</td><td>

Reference number of the payment inquiry case and indicates that the claim was created from that inquiry. This field appears only when the **Claim type** field is set to **Internal** and is auto-populated when the claim is created from an inquiry.

</td></tr><tr><td>

Requested treatment

</td><td>

Requested treatment for the claim either from the internal claims team or a third-party bank. This list contains the industry-standard treatments.

</td></tr><tr><td>

Actual treatment

</td><td>

Actual treatment for the claim either from the internal claims team or a third-party bank.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the case. This field is auto-populated from the selected request type. However, you can modify this description.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the case.

</td></tr><tr><td class="sub-head" colspan="2">

Claim Details section

</td></tr><tr><td>

Claim bank

</td><td>

Bank that is associated to the claim. The list of financial institutions that appears in this field depends on the following:-   Claim type – Internal or External.
-   Banks that are listed in the Financial Institution \[sn\_bom\_financial\_institution\] table.

</td></tr><tr><td>

External claim ID

</td><td>

Unique ID for the claim provided by the third-party bank. This field appears only when the **Claim type** field is set to **External**.

</td></tr><tr><td>

Claim customer

</td><td>

Consumer who opened the claim. This field appears only when the **Claim type** field is set to **Internal**. The field doesn't appear when a business customer is selected in the **Claim account** field.

</td></tr><tr><td>

Claim account

</td><td>

Business customer who opened the claim. This field appears only when the **Claim type** field is set to **Internal**. The field doesn't appear when a consumer is selected in the **Claim customer** field.

</td></tr><tr><td>

Claim contact

</td><td>

Contact of the business customer who opened the claim. This field appears only when the **Claim type** field is set to **Internal**. The field doesn't appear when a consumer is selected in the **Claim customer** field.

</td></tr><tr><td>

Claim financial account

</td><td>

Deposit account that the claim customer used. This field appears only when the **Claim type** field is set to **Internal**.

</td></tr><tr><td>

Claim transaction

</td><td>

Financial \(Deposit\) transaction that is used for the claim. This field appears only when the **Claim type** field is set to **Internal**.You can associate multiple transactions with a claim. These transactions also get listed in the **Claim Transactions** tab of the claim where you can view additional information about them.

 For any changes in transactions, both the **Claim Transaction** field and the **Claim Transactions** tab are updated.

</td></tr><tr><td>

Transaction ID

</td><td>

Unique identifier for the payment transaction that is to be shared with third-party banks.

</td></tr><tr><td>

Total amount

</td><td>

Total amount of the payment that is associated with the claim. Select the currency in which the payment was made.The **Claim Transaction** field sets the total amount based on the amount field in the transaction. If there are multiple transactions associated with the claim, amount of all are added to set the total amount.

</td></tr><tr><td>

Payment processor

</td><td>

Method of how the payment was made. The payment processor is region-specific.

</td></tr><tr><td>

Payment date

</td><td>

Date when the payment was made.

</td></tr><tr><td>

Recurring payment

</td><td>

Option to indicate if the payment was part of a recurring payment schedule.

</td></tr><tr><td>

International payment

</td><td>

Option to indicate if the payment was international.

</td></tr><tr><td class="sub-head" colspan="2">

Refund Details section

</td></tr><tr><td>

Refund bank

</td><td>

Bank that is associated to the refund. The list of financial institutions that appear in this field depends on the following:-   Claim type – Internal or External.
-   Banks that are listed in the Financial Institution \[sn\_bom\_financial\_institution\] table.

</td></tr><tr><td>

Tracking ID

</td><td>

Unique ID for the claim that is provided by the third-party bank. This field appears only when the **Claim type** field is set to **External**.

</td></tr><tr><td>

Outcome

</td><td>

Refund outcome for the claim. This field is auto-updated from the debit approval case when the **Refund type** field is set to **Internal**.

</td></tr><tr><td>

Refund amount

</td><td>

Total amount that is refunded based on the outcome of the refund. This field is auto-updated from the debit approval case when the **Refund type** field is set to **Internal**.Select the currency in which the refund is made.

</td></tr><tr><td>

Outcome notes

</td><td>

Additional notes about the refund outcome. This field is auto-updated from the debit approval case when the **Refund type** field is set to **Internal**.

</td></tr><tr><td class="sub-head" colspan="2">

Comments &amp; Activities section

</td></tr><tr><td>

Additional comments

</td><td>

Agent's comments about the case progress.

</td></tr></tbody>
</table>## Refund fields that are specific to claims with the Internal refund type

For claims with an internal refund type, the claim agent creates a debit approval case to request a refund internally from a bank or customer and fills out these fields.

**Note:** These fields appear only when the **Refund type** field is set to **Internal**.

<table id="table_nz4_243_gmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Refund Details section

</td></tr><tr><td>

Debit customer

</td><td>

Customer who refunds the claim, if the agent determines that the refund should come from a customer.

</td></tr><tr><td>

Debit financial account

</td><td>

Deposit account of the debit customer that is used for the refund. **Note:** This account might not be the same that received the money from the receiving transaction.

</td></tr><tr><td>

Debit account

</td><td>

Business customer who refunds the claim. This field doesn't appear when a consumer is selected in the **Debit customer** field.

</td></tr><tr><td>

Debit contact

</td><td>

Contact of the business customer who refunds the claim. This field doesn't appear when a consumer is selected in the **Debit customer** field.

</td></tr><tr><td>

Receiving transaction

</td><td>

Financial \(deposit\) transaction that the customer received and is used for the refund.You can associate multiple receiving transactions with a claim. These transactions also get listed in the **Receiving Transactions** tab of the claim where you can view additional information about them.

 For any changes in transactions, both the **Receiving Transaction** field and the **Receiving Transactions** tab are updated.

</td></tr><tr><td>

Debit approval

</td><td>

Debit approval case number that is created to request the refund internally from a bank or customer. This field is auto-populated when you create a debit approval case for the claim.

 For more information, see [Create a debit approval case for an internal refund](../task/create-debit-approval-case.md).

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Payment Operations reference](../concept/payment-operations-reference.md)

