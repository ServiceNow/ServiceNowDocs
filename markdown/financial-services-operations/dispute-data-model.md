---
title: Card Disputes data model
description: This section outlines the card disputes data model and the tables installed with the disputes application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Card Disputes data model

This section outlines the card disputes data model and the tables installed with the disputes application.

## Card disputes data model

The following diagram shows the tables and their relationships within the card disputes data model.

![Diagram showing the relationships between tables in the card disputes data model.](../../fso-deposit-operations/image/MMASSET0020606-card-dispute-data-model.png "Disputes data model")

## Card disputes tables

|Entity|Table name|What you can do|
|------|----------|---------------|
|Dispute Task|sn\_bom\_credit\_card\_disputes\_task|Track and manage dispute tasks; extends the Financial Task table \[sn\_bom\_task\].|
|Dispute Transaction|sn\_bom\_credit\_card\_disputes\_transaction|Store all credit card dispute transactions.|
|Business Checking Account|sn\_bom\_b2b\_checking\_account|Store checking account data for business customers; extends Deposit Account table \[sn\_bom\_deposit\_account\].|
|Business Saving Account|sn\_bom\_b2b\_saving\_account|Store saving account data for business customers; extends Deposit Account table \[sn\_bom\_deposit\_account\].|
|Deposit Account|sn\_bom\_deposit\_account|Manage all checking and saving account records; extends Financial Account table \[sn\_bom\_financial\_account\].|
|Financial Account|sn\_bom\_financial\_account|Store deposit, loan, credit card, line of credit, and insurance policy accounts; extends Sold Product table \[sn\_install\_base\_sold\_product\].|
|Financial Task|sn\_bom\_task|Manage financial tasks such as inquiries, claims, credits, and loans; extends Industry Task table \[sn\_ind\_task\].|
|Financial Transaction|sn\_bom\_transaction|Track all financial transactions across deposit, loan, and credit card accounts.|
|Line of Credit|sn\_bom\_line\_of\_credit|Store line of credit account records; extends Financial Account table \[sn\_bom\_financial\_account\].|
|Personal Checking Account|sn\_bom\_checking\_account|Store checking account data for individual consumers; extends Deposit Account table \[sn\_bom\_deposit\_account\].|
|Service Definition|sn\_bom\_service\_definition|Configure service definitions used across workflows; extends Service Definition table \[sn\_case\_type\_selection\].|
|Card Transaction|sn\_bom\_card\_transaction|Store card-based transaction records; extends Financial Transaction table \[sn\_bom\_transaction\].|
|Deposit Transaction|sn\_bom\_deposit\_transaction|Store deposit transaction records; extends Financial Transaction table \[sn\_bom\_transaction\].|
|Credit Transaction|sn\_bom\_line\_of\_credit\_transaction|Store line of credit transactions; extends Financial Transaction table \[sn\_bom\_transaction\].|
|Visa Dispute Intake|sn\_bom\_credit\_card\_dispute\_intake|Capture Visa dispute questionnaire questions and responses; extends Intake Form table \[sn\_evnt\_inq\_qtn\].|
|Visa Dispute Cardholder Intake|sn\_bom\_credit\_card\_cardholder\_dispute\_intake|Store Visa dispute responses from consumers; extends Visa Dispute Intake table \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\].|
|CRB Region Type|sn\_bom\_visa\_cp\_crb\_region\_type|Store Visa Card Recovery Bulletin \(CRB\) region details.|
|Mastercard Chargeback Reason Code Message|sn\_bom\_mcard\_cp\_mastercard\_chargeback\_reason\_codes|Store Mastercard chargeback reason codes and messages.|
|Sold Products|sn\_install\_base\_sold\_product|Track products and services sold to accounts or consumers.|
|Product Model|cmdb\_model|Configure product models for services, hardware, software, and consumables.|
|Card dispute service case|sn\_bom\_credit\_card\_disputes\_services|Create and track card dispute cases initiated by agents.|
|Card service model|Sn\_ent\_card\_service\_model|Store card product information.|
|Deposit model|sn\_ent\_deposit\_account\_model|Define deposit product models like savings or checking accounts.|
|Case|sn\_customerservice\_case|Manage customer questions, issues, and resolutions, such as card dispute cases.|
|Task|Task|Track work progress related to case management.|
|Task|sn\_customerservice\_task|Centralize and manage customer service-related tasks.|
|Card disputes related transaction|sn\_bom\_credit\_card\_disputes\_related\_transaction|Store transactions associated with a card dispute.|
|Service Definition|sn\_case\_type\_selection|Link services to case types and define request types.|
|Intake Form|sn\_evt\_inq\_qtn|Store request-related questions and responses.|
|Personal Saving Account|sn\_bom\_saving\_account|Store individual saving account data.|
|Payment Network|sn\_bom\_payment\_network|Store payment processing network info such as Visa Interlink, Pulse.|
|Business Credit Card|sn\_bom\_b2b\_credit\_card|Store business credit card details and usage data.|
|Personal Credit Card|sn\_bom\_credit\_card|Store individual credit card details.|
|Chargeback Reason Codes|sn\_bom\_chargeback\_reason\_codes|Categorize and store chargeback reasons per card network.|
|Financial Services Base|sn\_bom\_case|Manage all financial case records, including disputes and fraud investigations.|
|Account|customer\_account|Store and manage customer account records.|
|Consumer|csm\_consumer|Store information for B2C \(individual\) customers.|
|Contact|customer\_contact|Maintain customer contact information.|

-   **[Dispute decision tables](../concept/dispute-decision-tables.md)**  
Decision tables in Dispute Management provide decision logic for card dispute processing.

**Parent Topic:**[Data Models](../../fso-common/reference/data-models.md)

