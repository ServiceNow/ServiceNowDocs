---
title: Initiate a dispute
description: Begin a dispute case in Financial Services Card Operations for a transaction associated with a card account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Initiate a dispute

Begin a dispute case in Financial Services Card Operations for a transaction associated with a card account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

You can dispute one or more transactions that are associated with a card account by creating a dispute case.

To create a new dispute service case, see [Create a card dispute service case](create-dispute-service-case.md), and then continue this procedure from step 6 to initiate the case.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![Lists icon.](../../../common/image/icon-list.png)\).

3.  On the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

5.  Select the **Playbook** tab.

    The case playbook guides fulfillers through the steps that are involved in resolving a case.

6.  Under the **Initiate** playbook stage, fill in the required fields and any other related information.

<table id="choicetable_kl5_cxp_cbc"><thead><tr><th align="left" id="d46131e171">

Activity

</th><th align="left" id="d46131e174">

Description

</th></tr></thead><tbody><tr><td id="d46131e180">

**Select transaction**

</td><td>

Provide information on the cardholder and the dispute, such as:-   The account or consumer name
-   The category of the dispute
-   The card account that was used for the disputed transaction
-   The transaction being disputed


</td></tr><tr><td id="d46131e203">

**Add more transactions**

</td><td>

If the dispute category is Fraud, this activity appears. You may select additional transactions in the transactions list if there is more than one transaction being disputed.

As transactions are added, they are updated in the **State of transactions** panel.

</td></tr><tr><td id="d46131e219">

**Fill dispute questionnaire**

</td><td>

Complete the dispute questionnaire by answering the questions.**Note:** This step appears if you have the Dispute Rules Content Pack for Visa or Dispute Rules Content Pack for Mastercard installed, and the disputed transaction took place on the respective card network.

</td></tr><tr><td id="d46131e236">

**Document upload**

</td><td>

Upload any supporting documentation at this step, such as order details, invoices, and conversations between parties.

</td></tr><tr><td id="d46131e246">

**Submit dispute**

</td><td>

Confirm the dispute amount and add any other comments regarding the disputed transaction.If you are using a dispute content pack, you may also see the reason code field available based on the submitted responses.

For those using a Dispute Content Pack for US Regulations pack, there might be an option to indicate whether this is a new financial account, which impacts the applicability of the Service Level Agreement \(SLA\).

Select the checkbox to acknowledge that you have read and understood the disclaimer.

</td></tr></tbody>
</table>7.  Close the task from the playbook.

    |Action|Dispute Activity|
    |------|----------------|
    |**__Save changes__**|Save the dispute information task.|
    |**__Submit__**|When you select **Submit**, the system executes the chargeback eligibility rules in the background. These rules determine if the transaction is eligible for a chargeback, which is based on the answers that were provided in the questionnaire and the reason code. The chargeback eligibility information is recorded in the card disputes transaction.|


**Parent Topic:**[Work on a dispute case](work-dispute-case.md)

