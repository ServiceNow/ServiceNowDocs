---
title: Configuring additional questions for Dispute Intake
description: Configure the questionnaire that appears for dispute agents or cardholders when they intiate a dispute.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-10-28"
reading_time_minutes: 1
breadcrumb: [Dispute intake, About Dispute Management, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Configuring additional questions for Dispute Intake

Configure the questionnaire that appears for dispute agents or cardholders when they intiate a dispute.

## Before you begin

Role required: `admin` and `sn_bom_credit_card.admin`.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for the **Event Inquiry** application.

    The Event Inquiry application stores all questions and automates the intake process, which helps gather detailed information for specific requests. For more information, see [Dispute intake](../concept/dispute-questionnaire.md). Within this application, you will find two tables:

    -   Intake Form \[sn\_evnt\_inq\_qtn\]
    -   Intake Form Label \[sn\_evnt\_inq\_question\]
3.  Select the **Intake Form Label** table.

4.  Select **Show List** from the **Related Links** section.

5.  Search for `is_cardholder_denies_authorizing_ind` within the **Column name** field to demonstrate how the table works.

    You will see two Table name entries within the Intake Form Label table:

    -   The label tied to the **Dispute Intake** table appears to the dispute agent from the Financial Services Workspace.
    -   The label tied to the **Cardholder Dispute Intake** table appears to the cardholder during intake on the portal.
    This example lets you change the wording for different users but keeps both labels connected to the same column, `is_cardholder_denies_authorizing_ind`, in this case.

6.  Select **New** to add new labels for questionnaire.

7.  Complete the required fields for the new label and select **Submit**.


**Parent Topic:**[Dispute intake](../concept/dispute-questionnaire.md)

