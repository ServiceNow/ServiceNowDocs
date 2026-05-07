---
title: Initiate a dispute
description: Create a dispute case and initiate the dispute for a transaction associated with an account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Intake, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Initiate a dispute

Create a dispute case and initiate the dispute for a transaction associated with an account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

You can dispute one or more transactions that are associated with an account by creating a dispute case.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Create a case from the dispute service case list or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d34452e124">

Option

</th><th align="left" id="d34452e127">

Steps

</th></tr></thead><tbody><tr><td id="d34452e133">

**Dispute case from the dispute case list**

</td><td>

1.  In the **Lists** tab, under **Card disputes service cases**, select **All**.
2.  Select **New**.


</td></tr><tr><td id="d34452e163">

**Dispute case from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, select **My Interactions**.
2.  Open the required interaction record for the customer.
3.  Select **Create Case**.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  In the **Create a new case** dialog box, select **Card disputes services** from the category list.

5.  From the **Select service** list, select **Dispute card transactions**.

6.  Select **Create case**.

    A dispute service case is created in the New state.

7.  Under the **Initiate** playbook stage, fill in the required fields and any other related information.

<table id="choicetable_kl5_cxp_cbc"><thead><tr><th align="left" id="d34452e252">

Activity

</th><th align="left" id="d34452e255">

Description

</th></tr></thead><tbody><tr><td id="d34452e261">

**Select transaction**

</td><td>

Provide information on the account or consumer and the dispute, such as:

-   The account or consumer name
-   The account that was used for the disputed transaction
-   The transaction being disputed
 Use the transaction table filters to narrow down transactions by name, transaction category, and start and end dates.

 Select the transaction description to view more detailed information on the transaction.

 If one or more disputes cases exist that include the current transaction, they’ll display under **Duplicate transactions**.

 **Note:** If the transaction is part of another dispute case, it is flagged with a link to the case and information on the case outcome.

</td></tr><tr><td id="d34452e302">

**Select dispute reason**

</td><td>

Fill out a series of questions to arrive at the category and reason code.

 **Note:** In case of integration with Visa and Mastercard APIs, if an error displays, refer to the **Activity stream** to see the error cause, resolve it and then select **Retrigger** to reload the activity.

</td></tr><tr><td id="d34452e329">

**Add more transactions**

</td><td>

If the dispute category is **Fraud**, this activity displays. You may select additional transactions in the transactions list if there’s more than one transaction being disputed. If there are no other disputed transactions, select **Continue**.

If one or more disputes cases exists that include the current transaction, they’ll display under **Duplicate transactions**.

Only transactions valid to the dispute will display in this view \(for instance, based on the underlying reason code or transaction state.\)

**Note:** If the transaction is part of another dispute case, it will be flagged with a link to the case and information on the case outcome.

As transactions are added, they are updated in the **State of transactions** widget.

For ACH disputes, the **Transaction category** allows you to filter transactions by the following:

-   ACH
-   Wire
-   ATM
-   Check
-   Others
The **Fill additional transaction questions** activity is displayed if you add additional transactions.

**Note:** In case of integration with Visa and Mastercard APIs, if an error displays, refer to the **Activity stream** to see the error cause, resolve it, then select **Continue** to proceed to the next activity.

</td></tr><tr><td id="d34452e401">

**Resume dispute case**

</td><td>

This activity is displayed if the case was created using Now Assist for Financial Services Operations \(FSO\) with the Dispute intake via Virtual Agent skill.When a customer initiates a conversation with the Virtual Agent chatbot and selects Report a dispute, a dispute case is created.

If the conversation ends before the case is submitted, an agent can resume the intake and review or select the dispute's account and transaction details in this activity.

</td></tr><tr><td id="d34452e424">

**Fill dispute questionnaire**

</td><td>

Continue completing the dispute questionnaire in this activity.

</td></tr><tr><td id="d34452e433">

**Fill additional transaction questions**

</td><td>

This activity displays if multiple transactions are selected.

</td></tr><tr><td id="d34452e442">

**Document upload**

</td><td>

Upload any supporting documentation at this step, such as order details, invoices, and conversations between parties.

</td></tr><tr><td id="d34452e451">

**Customer signature required**

</td><td>

**Note:** This activity only occurs for ACH transactions with specified reason codes.

 For compliance purposes, inform the customer to sign a written statement for the unauthorized ACH debit and submit the document emailed to them.

 According to NACHA guidelines, customer must send a signed acknowledgment to the bank acknowledging they are disputing an unauthorized ACH debit transaction under certain reason codes.

 According to Nacha guidelines, customers must send a signed acknowledgment to the bank acknowledging they are disputing an unauthorized ACH debit transaction.

 A pre-written email template is sent to the customer. This email can be e-signed and can be amended by your organization as needed.

 Once the customer completes this, the signed statement is added as an attached document on the case.

 **Note:** In order for users to view the Written Statement of Unauthorized Debit \(WSUD\) document, the Document Templates \[sn\_doc\] plugin must be activated.

</td></tr><tr><td id="d34452e485">

**Submit dispute**

</td><td>

Confirm the dispute amount and add any other comments regarding the disputed transaction.For those using a Dispute Content Pack for US Regulations pack, there might be an option to indicate whether this is a new financial account, which impacts the applicability of the Service Level Agreement \(SLA\).

Select the checkbox to acknowledge that you have read and understood the disclaimer.

</td></tr></tbody>
</table>8.  Close the task from the playbook.

    |Action|Dispute Activity|
    |------|----------------|
    |**__Save changes__**|Save the dispute information task.|
    |**__Submit__**|When you select **Submit** for card disputes, the system executes the chargeback eligibility rules in the background. These rules determine if the transaction is eligible for a chargeback, which is based on the answers that were provided in the questionnaire and the reason code. The chargeback eligibility information is recorded in the disputes transaction.|


## Result

The case moves into the Processing stage.

The case is set to high priority in the following situations:

-   When the dispute category is Fraud.
-   If the transaction category is ACH and the SEC code is either CCD or CTX.

**Related topics**  


[Managing Disputes](../concept/managing-disputes.md)

[Written Statement for Unauthorized Debit \(WSUD\) Troubleshooting](../concept/wsud-troubleshooting-reference.md)

