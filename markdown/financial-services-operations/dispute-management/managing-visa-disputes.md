---
title: Managing Visa disputes
description: This page provides issuers the ability to understand the process of implementing the integration of ServiceNow Financial Services Card Operations \(card dispute playbook\) with the Dispute Rules Content Pack for Visa application.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Managing Visa disputes

This page provides issuers the ability to understand the process of implementing the integration of ServiceNow® Financial Services Card Operations \(card dispute playbook\) with the Dispute Rules Content Pack for Visa application.

## Creating card dispute case

Agents can manage dispute cases for their customers by using the dispute service case and its tasks. To learn on how to create a card dispute case, see [Creating a card dispute case](../task/create-dispute-service-case.md).

This process includes various stages. For more details on these stages, see [Managing dispute workflows](dispute-management-workflows.md).

## Dispute categories

Dispute categories include Fraud, Authorization, Processing Error, and Consumer Disputes. Each card network has its own set of rules and reason codes, but they generally fit into the following dispute categories:

-   **Fraud**

    This applies when the cardholder did not authorize or participate in the transaction.

-   **Authorization**

    This applies when a transaction required authorization but the merchant completed it without receiving it.

-   **Processing Error**

    This applies when a transaction is processed incorrectly due to a technical or operational mistake by the merchant, or when it’s processed correctly but not according to card network rules.

-   **Consumer**

    This applies when the cardholder disputes an issue with a merchant regarding the quality or receipt of goods or services.


## Dispute reason

Reason codes indicate the reason for a dispute.

## Dispute questionnaire

When a dispute agent or cardholder opens a dispute, they are presented with a corresponding set of questions. Designing clear, simple questions streamlines information gathering, helping customers or front-office agents understand and respond easily. For more details on configuring the questionnaire, see [Processing dispute intake](dispute-questionnaire.md).

## Dispute decision tables

The following table lists the decision tables used in Dispute Rules Content Pack for Visa.

<table id="table_u14_5q2_5cc"><thead><tr><th>

Decision table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visa Chargeback Eligibility Rules Subflow Mapping

</td><td>

Determines which chargeback eligibility subflow to call.

</td></tr><tr><td>

Determine chargeback dispute reason code 

</td><td>

Determines the chargeback reason code for Visa disputes based on the case categorization and the responses to the following questions:-   What is incorrect about this transaction? 
-   This dispute is due to?

</td></tr></tbody>
</table>For more information on the Decision tables that provide the logic for processing card disputes, see [Configuring dispute decision tables](dispute-decision-tables.md)

## Chargeback reason code

Data captured in Dispute Management is used to determine a reason code. These codes help the issuing bank decide if the dispute is eligible for a chargeback.

Reason codes are sent to Visa, which uses this information to process disputes through Visa Resolve Online \(VROL\).

Using ServiceNow to access all dispute details allows for more efficient management of disputes with Visa, saving time and money by reducing incorrectly processed cases.

## Chargeback eligibility rules

Dispute Management content packs can take all the data that was collected during the intake process, and then run it against the Visa chargeback eligibility rules.

This is to determine if the dispute is eligible for chargeback, or ineligible and the user has no chargeback rights. If the user doesn't have chargeback rights, then the system determines the reasons why the transactions are ineligible for chargeback.

ServiceNow will maintain the annual changes to these rules, removing the manual and time-consuming responsibility from banks. Note that the content in these packs, which includes the questions, eligibility rules and other information, will be in a read-only format.

## About the Dispute Rules Content Pack for Visa

The Dispute Rules Content Pack for Visa includes an intake questionnaire, chargeback eligibility determination based on Visa rules, and mapping of dispute reason codes. These features helps issuing banks enhance the data quality of dispute transactions, reduce the need for manual data entry, and apply chargeback eligibility rules through a connected system.

-   **[Dispute Rules Content Pack for Visa](../../dispute-content-pack-for-visa/concept/dispute-rules-content-pack-for-visa-landing-page-1.md)**  
The ServiceNow® Dispute Rules Content Pack for Visa provides questionnaires for the intake of dispute related information under various dispute categories as per Visa guidelines.

**Parent Topic:**[Dispute Management](../../fso-deposit-operations/concept/dispute-management.md)

