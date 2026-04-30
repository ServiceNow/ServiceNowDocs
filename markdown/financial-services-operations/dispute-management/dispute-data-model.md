---
title: Card disputes data model
description: This section outlines the card disputes data model and the tables installed with the disputes application.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: reference
last_updated: "2024-08-26"
reading_time_minutes: 5
breadcrumb: [Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Card disputes data model

This section outlines the card disputes data model and the tables installed with the disputes application.

## Card disputes data model

The following diagram shows the tables and their relationships within the card disputes data model.

![Diagram showing the relationships between various tables in the card disputes data model.](../../fso-deposit-operations/image/MMASSET0020606-card-dispute-data-model.png "Dispute data model")

## Card disputes tables

|Entity|Table Name|Description|
|------|----------|-----------|
|Dispute Task|sn\_bom\_credit\_card\_disputes\_task|Stores all dispute tasks. This table extends the Financial Task \[sn\_bom\_task\] table.|
|Dispute Transaction|sn\_bom\_credit\_card\_disputes\_transaction|Stores all dispute transactions.|
|Business Checking Account|sn\_bom\_b2b\_checking\_account|Stores all checking account records for consumers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Business Saving Account|sn\_bom\_b2b\_saving\_account|Stores all saving account records for business customers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Deposit Account|sn\_bom\_deposit\_account|Stores all deposit accounts – Checking and Saving records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Financial Account|sn\_bom\_financial\_account|Stores all financial accounts – deposit accounts, loan accounts, credit card account, line of credit accounts, and insurance policy accounts. Extends the Sold Product \[sn\_install\_base\_sold\_product\] table.|
|Financial Task|sn\_bom\_task|Stores all financial tasks such as inquiry tasks, claim tasks, credit tasks, and loan tasks. Extends the Industry Task \[sn\_ind\_task\] table.|
|Financial Transaction|sn\_bom\_transaction|Stores all financial transactions for deposit, loan, and credit card accounts.|
|Line of Credit|sn\_bom\_line\_of\_credit|Stores all line of credit account records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Personal Checking Account|sn\_bom\_checking\_account|Stores all checking account records for consumers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Service Definition|sn\_bom\_service\_definition|Stores all service definitions configured for all workflows across Financial Services Operations applications.|
|Card Transaction|sn\_bom\_card\_transaction|Stores all card transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Deposit Transaction|sn\_bom\_deposit\_transaction|Stores all deposit transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Credit Transaction|sn\_bom\_line\_of\_credit\_transaction|Stores all line of credit transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Visa Dispute Intake|sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire|Stores all Visa Dispute Questionnaire questions and responses. Extends the Intake Form \[sn\_evnt\_inq\_qtn\] table.|
|Visa Dispute Cardholder Intake|sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake|Stores Visa Dispute Questionnaire questions and responses submitted by consumers, such as a dispute playbook on a service portal. Extends the Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] table.|
|CRB Region Type|sn\_bom\_visa\_cp\_crb\_region\_type|Stores all Visa Card Recovery Bulletin \(CRB\) regions.|
|Mastercard Chargeback Reason Code Message|sn\_bom\_mcard\_cp\_mastercard\_chargeback\_reason\_codes|Contains the Mastercard chargeback reason codes and associated messages.|
|Sold Products|sn\_install\_base\_sold\_product|This table is used to import and provide a view into the products and services that have been sold to an account or consumer. It helps customers, consumers, and customer service agents access details about sold products.|
|Product Model|cmdb\_model|This table is used to configure product models, such as services, hardware, software, or consumables that the company sells and supports.|
|Card dispute service case|sn\_bom\_credit\_card\_disputes\_services|This table is used by agents to begin the card dispute process or report a dispute by creating a dispute case on behalf of a customer.|
|Card service model|Sn\_ent\_card\_service\_model|Model table to store card product information|
|Deposit model|sn\_ent\_deposit\_account\_model|Model table to store deposit products like Savings account, checking accounts, and so on.|
|Case|sn\_customerservice\_case|A case record includes detailed information about customers, their reported questions or issues, and the work performed to answer questions and resolve issues. E.g., Card dispute service case table.|
|Task|Task|Task table is used to store and track the progress of various work assignments on a Case.|
|Task|sn\_customerservice\_task|The sn\_customerservice\_task table in ServiceNow is designed to centralize all customer service tasks. This table helps in organizing and managing customer service tasks efficiently, ensuring that all relevant information is easily accessible and manageable.|
|Card disputes related transaction|sn\_bom\_credit\_card\_disputes\_related\_transaction|To store details of related transactions in the context of a card dispute, e.g., associated transactions with respect to a Visa dispute.|
|Service Definition|sn\_case\_type\_selection|Service definitions are used to create connections between products, services, and case types. Service definitions work with case types to provide different types of service requests, e.g., Issue final credit.|
|Intake Form|sn\_evt\_inq\_qtn|The table is designed to store questions asked during the processing of various types of requests. This table serves as a generic repository for documenting interactions related to various types of requests. It ensures that all necessary questions are asked, and responses are recorded.|
|Personal Saving Account|sn\_bom\_saving\_account|Table to store details of a type of bank account that allows customers to deposit money and earn interest on it.|
|Payment Network|sn\_bom\_payment\_network|Table to store information about the payment processing networks in the context of cards. E.g., Visa interlink, Pulse.|
|Business Credit Card|sn\_bom\_b2b\_credit\_card|Table to store details of a type of credit card that is designed for businesses to purchase goods or services on credit with benefits tailored to their needs.|
|Personal Credit Card|sn\_bom\_credit\_card|Table to store details of a type of credit card that allows individuals to purchase goods or services on credit.|
|Chargeback Reason Codes|sn\_bom\_chargeback\_reason\_codes|Chargeback reason codes are numerical codes used to categorize the reasons why a cardholder disputes a transaction. These are provided by card networks like Visa, Mastercard, American Express. The table holds details of these reason codes.|
|Financial Services Base|sn\_bom\_case|The Financial Services Base table serves as the parent table for all types of financial case records within a system. It acts as a central repository that provides a unified structure for managing various financial cases, such as disputes, fraud investigations, loan applications, and other financial inquiries or issues. Each record in this table represents a unique financial case, with associated metadata that links to more specific case details stored in related child tables.|
|Account|customer\_account|Table in ServiceNow is designed to define and manage customer accounts. This table helps in organizing and maintaining customer information, ensuring that all relevant details are easily accessible and manageable|
|Consumer|csm\_consumer|Table in ServiceNow represents a B2C customer. This table helps in organizing and maintaining consumer information, ensuring that all relevant details are easily accessible and manageable|
|Contact|customer\_contact|This table helps in organizing and maintaining contact details, ensuring that all relevant information is easily accessible and manageable.|

**Parent Topic:**[Dispute Management](../../fso-deposit-operations/concept/dispute-management.md)

