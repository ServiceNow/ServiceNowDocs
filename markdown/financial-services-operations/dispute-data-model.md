---
title: Card Disputes data model
description: This section outlines the card disputes data model and the tables installed with the disputes application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Card Disputes data model

This section outlines the card disputes data model and the tables installed with the disputes application.

## Card disputes data model

The following diagram shows the tables and their relationships within the card disputes data model.

\[Omitted image "MMASSET0020606-card-dispute-data-model.png"\] Alt text: Diagram showing the relationships between tables in the card disputes data model.

## Card disputes tables

<table id="table_bvp_v5f_ncc"><thead><tr><th>

Entity

</th><th>

Table name

</th><th>

What you can do

</th></tr></thead><tbody><tr><td>

Product Model

</td><td>

cmdb\_model

</td><td>

Configure product models for services, hardware, software, and consumables.

</td></tr><tr><td>

Consumer

</td><td>

csm\_consumer

</td><td>

Store information for B2C \(individual\) customers.

</td></tr><tr><td>

Account

</td><td>

customer\_account

</td><td>

Store and manage customer account records.

</td></tr><tr><td>

Contact

</td><td>

customer\_contact

</td><td>

Maintain customer contact information.

</td></tr><tr><td>

Card service model

</td><td>

Sn\_ent\_card\_service\_model

</td><td>

Store card product information.

</td></tr><tr><td>

Deposit model

</td><td>

sn\_ent\_deposit\_account\_model

</td><td>

Define deposit product models like savings or checking accounts.

</td></tr><tr><td>

Intake Form

</td><td>

sn\_evt\_inq\_qtn

</td><td>

Store request-related questions and responses.

</td></tr><tr><td>

Business Credit Card

</td><td>

sn\_bom\_b2b\_credit\_card

</td><td>

Store business credit card details and usage data.

</td></tr><tr><td>

Business Checking Account

</td><td>

sn\_bom\_b2b\_checking\_account

</td><td>

Store checking account data for business customers; extends Deposit Account table \[sn\_bom\_deposit\_account\].

</td></tr><tr><td>

Business Saving Account

</td><td>

sn\_bom\_b2b\_saving\_account

</td><td>

Store saving account data for business customers; extends Deposit Account table \[sn\_bom\_deposit\_account\].

</td></tr><tr><td>

Card Transaction

</td><td>

sn\_bom\_card\_transaction

</td><td>

Store card-based transaction records; extends Financial Transaction table \[sn\_bom\_transaction\].

</td></tr><tr><td>

Financial Services Base

</td><td>

sn\_bom\_case

</td><td>

Manage all financial case records, including disputes and fraud investigations.

</td></tr><tr><td>

Chargeback Reason Codes

</td><td>

sn\_bom\_chargeback\_reason\_codes

</td><td>

Categorize and store chargeback reasons per card network.

</td></tr><tr><td>

Personal Checking Account

</td><td>

sn\_bom\_checking\_account

</td><td>

Store checking account data for individual consumers; extends Deposit Account table \[sn\_bom\_deposit\_account\].

</td></tr><tr><td>

Personal Credit Card

</td><td>

sn\_bom\_credit\_card

</td><td>

Store individual credit card details.

</td></tr><tr><td>

Visa Dispute Cardholder Intake

</td><td>

sn\_bom\_credit\_card\_cardholder\_dispute\_intake

</td><td>

Store Visa dispute responses from consumers; extends Visa Dispute Intake table \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\].

</td></tr><tr><td>

Visa Dispute Intake

</td><td>

sn\_bom\_credit\_card\_dispute\_intake

</td><td>

Capture Visa dispute questionnaire questions and responses; extends Intake Form table \[sn\_evnt\_inq\_qtn\].

</td></tr><tr><td>

Card disputes related transaction

</td><td>

sn\_bom\_credit\_card\_disputes\_related\_transaction

</td><td>

Store transactions associated with a card dispute.

</td></tr><tr><td>

Card dispute service case

</td><td>

sn\_bom\_credit\_card\_disputes\_services

</td><td>

Create and track card dispute cases initiated by agents.

</td></tr><tr><td>

Dispute Task

</td><td>

sn\_bom\_credit\_card\_disputes\_task

</td><td>

Track and manage dispute tasks; extends the Financial Task table \[sn\_bom\_task\].

</td></tr><tr><td>

Dispute Transaction

</td><td>

sn\_bom\_credit\_card\_disputes\_transaction

</td><td>

Store all credit card dispute transactions.

</td></tr><tr><td>

Deposit Account

</td><td>

sn\_bom\_deposit\_account

</td><td>

Manage all checking and saving account records; extends Financial Account table \[sn\_bom\_financial\_account\].

</td></tr><tr><td>

Deposit Transaction

</td><td>

sn\_bom\_deposit\_transaction

</td><td>

Store deposit transaction records; extends Financial Transaction table \[sn\_bom\_transaction\].

</td></tr><tr><td>

Financial Account

</td><td>

sn\_bom\_financial\_account

</td><td>

Store deposit, loan, credit card, line of credit, and insurance policy accounts; extends Sold Product table \[sn\_install\_base\_sold\_product\].

</td></tr><tr><td>

Line of Credit

</td><td>

sn\_bom\_line\_of\_credit

</td><td>

Store line of credit account records; extends Financial Account table \[sn\_bom\_financial\_account\].

</td></tr><tr><td>

Credit Transaction

</td><td>

sn\_bom\_line\_of\_credit\_transaction

</td><td>

Store line of credit transactions; extends Financial Transaction table \[sn\_bom\_transaction\].

</td></tr><tr><td>

Mastercard Chargeback Reason Code Message

</td><td>

sn\_bom\_mcard\_cp\_mastercard\_chargeback\_reason\_codes

</td><td>

Store Mastercard chargeback reason codes and messages.

</td></tr><tr><td>

Merchant Category Code

</td><td>

sn\_bom\_merchant\_category\_code

</td><td>

Store the ISO-certified Merchant Category Code \(MCC\) list used to categorize merchants on a transaction. **Note:** A transaction referencing an MCC that isn't in this table can cause a lookup subflow to error; before treating this as a product gap, confirm whether the transaction data is valid production data.

</td></tr><tr><td>

Payment Network

</td><td>

sn\_bom\_payment\_network

</td><td>

Store payment processing network info such as Visa Interlink, Pulse.

</td></tr><tr><td>

Personal Saving Account

</td><td>

sn\_bom\_saving\_account

</td><td>

Store individual saving account data.

</td></tr><tr><td>

Service Definition

</td><td>

sn\_bom\_service\_definition

</td><td>

Configure service definitions used across workflows; extends Service Definition table \[sn\_case\_type\_selection\].

</td></tr><tr><td>

Financial Task

</td><td>

sn\_bom\_task

</td><td>

Manage financial tasks such as inquiries, claims, credits, and loans; extends Industry Task table \[sn\_ind\_task\].

</td></tr><tr><td>

Financial Transaction

</td><td>

sn\_bom\_transaction

</td><td>

Track all financial transactions across deposit, loan, and credit card accounts.

</td></tr><tr><td>

CRB Region Type

</td><td>

sn\_bom\_visa\_cp\_crb\_region\_type

</td><td>

Store Visa Card Recovery Bulletin \(CRB\) region details.

</td></tr><tr><td>

Service Definition

</td><td>

sn\_case\_type\_selection

</td><td>

Link services to case types and define request types.

</td></tr><tr><td>

Case

</td><td>

sn\_customerservice\_case

</td><td>

Manage customer questions, issues, and resolutions, such as card dispute cases.

</td></tr><tr><td>

Task

</td><td>

sn\_customerservice\_task

</td><td>

Centralize and manage customer service-related tasks.

</td></tr><tr><td>

Sold Products

</td><td>

sn\_install\_base\_sold\_product

</td><td>

Track products and services sold to accounts or consumers.

</td></tr><tr><td>

Task

</td><td>

Task

</td><td>

Track work progress related to case management.

</td></tr></tbody>
</table>-   **[Dispute decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-decision-tables.md)**  
Decision tables in Dispute Management provide decision logic for card dispute processing.

**Parent Topic:**[Data Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/data-models.md)

