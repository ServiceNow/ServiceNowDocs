---
title: Field descriptions for a payment inquiry case
description: Payment inquiry cases help the inquiry agents resolve inquiries that they receive from the bank's customers or third-party banks.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Financial Services Payment Operations reference, Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Field descriptions for a payment inquiry case

Payment inquiry cases help the inquiry agents resolve inquiries that they receive from the bank's customers or third-party banks.

When a payment inquiry request is submitted, it creates an inquiry case. Some of the fields on the case form are populated from the request from which the inquiry case is created.

After the case is assigned, an inquiry agent fills out the fields on the case when dealing with the next steps. The next steps could include investigating the case, sending emails requesting information from the recipient bank, and proposing a solution for the case.

## Details tab fields for a payment inquiry case

The **Details** tab on the form provides case-related information.

<table id="table_xw5_vpd_pkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the case.

</td></tr><tr><td>

Inquiry type

</td><td>

Type of the payment inquiry case, such as Payment in Error and Beneficiary Claim Non-Receipt. The inquiry type determines which flow to trigger and the form view to show.

</td></tr><tr><td>

Sender customer

</td><td>

Consumer who sent the payment. This field appears only for internal payment inquiries.The field doesn't appear when a business customer is selected in the **Sender account** field.

</td></tr><tr><td>

Sender account

</td><td>

Business customer who sent the payment. This field appears only for internal payment inquiries. The field doesn't appear when a consumer is selected in the **Sender customer** field.

</td></tr><tr><td>

Sender contact

</td><td>

Contact of the business customer who sent the payment. This field appears only for internal payment inquiries. The field doesn't appear when a consumer is selected in the **Sender customer** field.

</td></tr><tr><td>

Sender financial account

</td><td>

Financial account that the sender used to make the payment. This field appears only for internal payment inquiries and shows only the deposit accounts for the selected sender customer or account.

</td></tr><tr><td>

Sender transactions

</td><td>

Financial transaction that the sender customer sent. This field appears only for internal payment inquiries and shows only the deposit transactions for the selected sender financial account.You can associate multiple transactions with an inquiry. These transactions also get listed in the **Sender Transactions** tab of the inquiry where you can view additional information about them.

 For any changes in transactions, both the **Sender Transaction** field and the **Sender Transactions** tab are updated.

</td></tr><tr><td>

State

</td><td>

State of the case.

</td></tr><tr><td>

Assignment group

</td><td>

User group that can work on the case. If the case is not assigned to a user yet, any member of this group can work on the case.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the case.

</td></tr><tr><td>

Channel

</td><td>

Communication channel that the customer used to reach out for the inquiry.

</td></tr><tr><td>

Error type

</td><td>

Type of payment error to identify whether it was the customer’s or bank’s fault. This field appears only for Beneficiary Claim Non-Receipt - External and Payment in Error payment inquiries.

</td></tr><tr><td>

Valid claim

</td><td>

Option used by the inquiry agent when the agent determines that the inquiry should create a claim and the customer is entitled to a refund. Selecting this option shows the **Create Claim** button after you save.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the case. This field is auto-populated from the selected request type.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the case.

</td></tr><tr><td class="sub-head" colspan="2">

Payment information

</td></tr><tr><td>

Recipient type

</td><td>

Recipient that is either internal or external to the bank. This field appears only for Beneficiary Claim Non-Receipt - External and Beneficiary Claim Non-Receipt - Internal inquiry types.

</td></tr><tr><td>

Sent to – Beneficiary name

</td><td>

Name of the beneficiary to whom the payment was sent. This field appears only for internal inquiries such as Beneficiary Claim Non-Receipt - Internal and Payment in Error.

</td></tr><tr><td>

Sent to – Account number

</td><td>

Account number of the beneficiary to which the payment was sent. This field appears only for internal inquiries such as Beneficiary Claim Non-Receipt - Internal and Payment in Error.

</td></tr><tr><td>

Sent to – Sort/Routing number

</td><td>

Sorting or routing number that the payment was sent to. This field appears only for internal inquiries such as Beneficiary Claim Non-Receipt - Internal and Payment in Error.

</td></tr><tr><td>

Payment processor

</td><td>

Method of how the payment was made. The payment processor is region-specific.

</td></tr><tr><td>

Transaction ID

</td><td>

Unique identifier for the payment transaction and to be shared with third-party banks.

</td></tr><tr><td>

Payment date

</td><td>

Date when the payment was made.The **Sender transactions** field sets this date based on the date field in the transaction. If there are multiple transactions associated with the inquiry, the earliest transaction date of all is set as the payment date.

</td></tr><tr><td>

Total amount

</td><td>

Total amount of the payment. Select the currency in which the payment was made.The **Sender transactions** field sets the total amount based on the amount field in the transaction. If there are multiple transactions associated with the inquiry, amount of all are added to set the total amount.

</td></tr><tr><td>

Sender bank

</td><td>

Bank that is associated to the sender’s financial account. The list of financial institutions in this field depends on whether the sender is internal or external.

</td></tr><tr><td>

Recipient bank

</td><td>

Bank that is associated to the receiver’s financial account. The list of financial institutions in this field depends on whether the Recipient type is internal or external.

</td></tr><tr><td>

External inquiry ID

</td><td>

Unique ID for the case that was received from a third-party bank. This field appears only when the Recipient type is external.

</td></tr><tr><td>

International payment

</td><td>

Option to indicate if the payment was international.

</td></tr><tr><td>

Recurring payment

</td><td>

Option to indicate if the payment was part of a recurring payment schedule.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution information

</td></tr><tr><td>

Resolved by

</td><td>

Name of the agent who proposed the solution to resolve the case.

</td></tr><tr><td>

Resolved

</td><td>

Date when the agent proposed a solution for the case and the case state moved to the Resolved state.

</td></tr><tr><td>

Closed by

</td><td>

Name of the agent who closed the case after the customer accepted the proposed solution.

</td></tr><tr><td>

Closed

</td><td>

Date when the case closed after the agent received the customer's acceptance for the proposed solution and the case state moved to the Closed state.

</td></tr><tr><td>

Resolution code

</td><td>

Type of the proposed solution.

</td></tr><tr><td>

Resolution notes

</td><td>

Agent's notes on the proposed solution.

</td></tr><tr><td>

Add resolution notes to comments

</td><td>

Option to copy the resolution notes to comments.

</td></tr><tr><td class="sub-head" colspan="2">

Comments &amp; Activities

</td></tr><tr><td>

Additional comments

</td><td>

Agent's comments about the case progress.

</td></tr></tbody>
</table>## Fields specific to the Beneficiary Claim Non-Receipt case with an internal payment recipient

<table id="table_a5k_psv_s4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Receiving customer

</td><td>

Consumer who received the payment.The field doesn't appear when a business customer is selected in the **Receiving account** field.

</td></tr><tr><td>

Receiving account

</td><td>

Business customer who received the payment. The field doesn't appear when a consumer is selected in the **Receiving customer** field.

</td></tr><tr><td>

Receiving contact

</td><td>

Contact of the business customer who received the payment. The field doesn't appear when a consumer is selected in the **Receiving customer** field.

</td></tr><tr><td>

Receiving financial account

</td><td>

Financial account of the receiver that got the payment.

</td></tr><tr><td>

Receiving transactions

</td><td>

Financial transaction that the receiving customer or account received.You can associate multiple receiving transactions with an inquiry. These transactions also get updated in the **Receiving Transactions** tab of the inquiry where you can view additional information about them.

 For any changes in transactions, both the **Receiving Transaction** field and the **Receiving Transactions** tab are updated.

</td></tr></tbody>
</table>## Fields specific to the Payment in error case

|Field|Description|
|-----|-----------|
|Attempted to recover fund|Option to identify if the customer attempted to recover the payment before opening the inquiry.|
|Correct send to – Beneficiary name|Name of the beneficiary to whom the payment was supposed to be sent. This field appears only for the Payment in Error inquiry type.|
|Correct send to – Account number|Account number of the beneficiary to which the payment was supposed to be sent. This field appears only for the Payment in Error inquiry type.|
|Correct send to – Sort/Routing number|Sort or routing number the payment was supposed to be sent to. This field appears only for the Payment in Error inquiry type.|
|Customer reason|List of reasons why the customer opened the payment inquiry.|

**Parent Topic:**[Financial Services Payment Operations reference](../concept/payment-operations-reference.md)

