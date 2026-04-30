---
title: FSO Core Banking tables
description: This section describes the banking tables in FSO Core and shows how they store and manage banking information.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Financial Services Operations Core, Data Model, Learning and exploring, Financial Services Operations \(FSO\)]
---

# FSO Core Banking tables

This section describes the banking tables in FSO Core and shows how they store and manage banking information.

## Banking tables installed

|Label|Table name|Description|
|-----|----------|-----------|
|Auto Loan|sn\_bom\_auto\_loan|Stores all auto loans records. This table extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Bond|sn\_bom\_bond|Stores all bond information. Extends the Security \[sn\_bom\_security\] table.|
|Business Certificate of Deposit|sn\_bom\_b2b\_certificate\_of\_deposit|Table stores details of a certificate of deposit account a type of financial account that allows businesses to deposit money for a fixed period and earn a fixed interest on it.|
|Business Checking Account|sn\_bom\_b2b\_checking\_account|Stores all checking account records for consumers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Business Credit Card|sn\_bom\_b2b\_credit\_card|Table to store details of a type of credit card that is designed for businesses to purchase goods or services on credit with benefits tailored to their needs.|
|Business Line of Credit|sn\_bom\_b2b\_line\_of\_credit|Stores all line of credit records for business loan customers. Extends the Line of Credit table.|
|Business Saving Account|sn\_bom\_b2b\_saving\_account|Stores all saving account \(a type of deposit account\) records for business customers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Chargeback Reason Codes|sn\_bom\_chargeback\_reason\_codes|Chargeback reason codes are numerical codes used to categorize the reasons why a cardholder disputes a transaction. These are provided by card networks like Visa, Mastercard, American Express. The table holds details of these reason codes.|
|Commercial Real Estate Loan|sn\_bom\_commercial\_real\_estate\_loan|Stores all commercial real estate loan records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Commercial Vehicle Loan|sn\_bom\_commercial\_vehicle\_loan|Stores all commercial vehicle loan records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Covenant|sn\_bom\_b2b\_covenant|Stores all covenant records for business customers.|
|Covenant|sn\_bom\_covenant|Stores all covenant records for consumers.|
|Covenant|sn\_bom\_covenant\_base|\[sn\_bom\_b2b\_covenant\] and \[sn\_bom\_covenant\_base\] tables extend the Covenant Base table.|
|Coverage Specification|sn\_bom\_coverage\_specification|Coverage specification defines the product coverage types and their options.|
|Coverage Type|sn\_bom\_coverage\_type|Coverage type table will contain all the coverage types across all products.|
|Coverage Type Option|sn\_bom\_coverage\_type\_option|Coverage type option table will contain all the coverage options for each coverage type across all products.|
|Currency ISO Code Association|currency\_iso\_code\_association| |
|Customer Property|sn\_bom\_customer\_property|Customer property table holds the details of the properties that a customer has. For example, it holds the vehicles and property locations that a customer holds.|
|Data Fix Backup|sn\_bom\_data\_fix\_backup|Table to backup records during data migration from one table to another|
|Deposit Account|sn\_bom\_deposit\_account|Stores all deposit accounts – Checking and Saving records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Equipment Loan|sn\_bom\_equipment\_loan|Stores all equipment loan records. This table extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|ETF|sn\_bom\_etf|Stores all ETF information. This table extends the Security \[sn\_bom\_security\] table.|
|Exchange|sn\_bom\_exchange| |
|Financial Account|sn\_bom\_financial\_account|Stores all financial accounts – deposit accounts, loan accounts, credit card account, line of credit accounts, and insurance policy accounts. Extends the Sold Product \[sn\_install\_base\_sold\_product\] table.|
|Financial Institution|sn\_bom\_financial\_institution|Stores all financial institution records. Extends the Company \[core\_company\] table.|
|Financial Service|sn\_bom\_service|Stores all financial services – RDC service and wire transfer service. Extends the Sold Product \[sn\_install\_base\_sold\_product\] table.|
|Financial Service Financial Account|sn\_bom\_m2m\_service\_financial\_account|Stores all financial accounts – deposit accounts, loan accounts, credit card account, line of credit accounts, and insurance policy accounts. Extends the Sold Product \[sn\_install\_base\_sold\_product\] table|
|Financial Service User|sn\_bom\_m2m\_service\_user|Stores details of users for a financial service account|
|Financial Services Base|sn\_bom\_case|The Financial Services Base table serves as the parent table for all types of financial case records within a system. It acts as a central repository that provides a unified structure for managing various financial cases, such as disputes, fraud investigations, loan applications, insurance servicing, claims and other financial inquiries or issues. Each record in this table represents a unique financial case, with associated metadata that links to more specific case details stored in related child tables.|
|Financial Services Case|sn\_bom\_financial\_service|Stores all financial services cases. Extends the financial services base Case \[sn\_bom\_case\] table.|
|Financial Services Task|sn\_bom\_financial\_task|Stores all financial services tasks. Extends the Financial Task \[sn\_bom\_task\] table.|
|Financial Task|sn\_bom\_task|Stores all financial tasks such as inquiry tasks, claim tasks, credit tasks and loan tasks. Extends the Industry Task \[sn\_ind\_task\] table.|
|Financial Transaction|sn\_bom\_transaction|Stores all financial transactions for deposit, loan, and credit card accounts. Extends the Industry Data Entity \[sn\_ind\_data\_entity\] table.|
|Group Member Info|sn\_bom\_group\_member\_info|Group member info table is an extension of customer property table which can contain the group member details applicable to a customer. For example, in employer provided life insurance policy scenario, this table can hold the group member details of the employer.|
|Holding|sn\_bom\_holding|Stores holding information.|
|Holding lot|sn\_bom\_holding\_lot|Stores holding lot information.|
|Insured Property|sn\_bom\_insured\_property|Insured property table references customer property and will contain the properties of a customer which are covered by an insurance policy.|
|Investment account|sn\_bom\_investment\_account|Stores all investment account records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Line|sn\_bom\_line|This is a parent table which holds the case lines of a case when requests are made on the line items belonging to a sold product. For example, in an insurance servicing case, when a request is made to change policy coverages , the coverage line items for the policy can be held in the line tables extended from this table in the servicing app. This ensures that the changes are not made directly on the insurance policy coverage records when the case is being processed and the updates are made only after the case is approved and closed.|
|Line of Credit|sn\_bom\_line\_of\_credit|Stores all line of credit account records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Loan Account|sn\_bom\_loan\_account|Stores all loan account records. Extends the Financial Account \[sn\_bom\_financial\_account\] table.|
|Location|sn\_bom\_location|Customer Property|
|Merchant Category Code|sn\_bom\_merchant\_category\_code| |
|Mortgage|sn\_bom\_mortgage|Stores all mortgage account records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Operating instruction|sn\_bom\_b2b\_operating\_instruction|Table to store the operating instructions on a business account.E.g on a business checking account who are the signatories who are allowed to sign and their financial limits.|
|Operating instruction|sn\_bom\_operating\_instruction|Table to store the operating instructions on a personal account.E.g on a personal checking account who are the signatories who are allowed to sign or provide instructions to operate the account.|
|Option|sn\_bom\_option|Stores all options information. Extends the Security \[sn\_bom\_security\] table.|
|Payment Network|sn\_bom\_payment\_network|Table to store information about the payment processing networks in the context of cards. E.g., Visa interlink, Pulse.|
|Personal Certificate of Deposit|sn\_bom\_certificate\_of\_deposit|Table stores details of a certificate of deposit account a type of financial account that allows individuals to deposit money for a fixed period and earn a fixed interest on it.|
|Personal Checking Account|sn\_bom\_checking\_account|Stores all checking account records for consumers. Extends the Deposit Account \[sn\_bom\_deposit\_account\] table.|
|Personal Credit Card|sn\_bom\_credit\_card|Table to store details of a type of credit card that allows individuals to purchase goods or services on credit.|
|Personal Line of Credit|sn\_bom\_b2c\_line\_of\_credit|Stores all line of credit records for consumers.|
|Personal Loan|sn\_bom\_personal\_loan|Stores all personal loan account records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Personal Saving Account|sn\_bom\_saving\_account|Table to store details of a type of bank account that allows customers to deposit money and earn interest on it.|
|Policy Coverage|sn\_bom\_policy\_coverage|Policy coverage table will contain the defined coverages on the insurance policy.|
|Policy Participant|sn\_bom\_policy\_participant|Policy participant table will contain the defined participants on the insurance policy.|
|Policy Participant Role|sn\_bom\_policy\_participant\_insured\_property|Policy participant role table will contain the roles played by the participants who have been defined on the insurance policy.|
|Product Coverage Type|sn\_bom\_product\_coverage\_type|Product coverage type table will contain the product coverage types defined for the product|
|Product Coverage Type Option|sn\_bom\_product\_coverage\_type\_option|Product coverage type option table will contain the product coverage type options defined for a coverage type within the product|
|RDC Financial Account|sn\_bom\_m2m\_rdc\_financial\_account|Financial Service Financial Account|
|RDC Service|sn\_bom\_rdc|Stores all RDC treasury service records. Extends the Financial Service \[sn\_bom\_service\] table.|
|RDC User|sn\_bom\_m2m\_rdc\_user|Stores details of users who are authorized to request for a remote deposit capture facility on a business deposit account|
|Renters Policy|sn\_bom\_renters\_ins\_policy|Insurance personal renters policy table extended from insurance policy.|
|SBA Loan|sn\_bom\_sba\_loan|Stores all SBA \(Small Business Administration\) loan account records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Security|sn\_bom\_security|Stores all security information. Extends the Security \[sn\_bom\_security\] table.|
|Security Exchange|sn\_bom\_m2m\_security\_exchange|Table to store details of security exchange \(a marketplace where securities, such as stocks, bonds, and derivatives, are bought and sold\). E.g. NYSE- New York Stock Exchange, Nasdaq|
|Service Definition|sn\_bom\_service\_definition|Stores all service definitions configured for all workflows across Financial Services Operations applications.|
|Service Definition has Agent Criteria|sn\_bom\_m2m\_service\_definition\_user\_criteria|An m2m table between Service Definition and Agent Criteria \(user\_criteria\)|
|Service Definition has Entity Criteria|sn\_bom\_m2m\_service\_definition\_customer\_condition|An m2m table between Service Definition and Entity Criteria \(sn\_req\_criteria\_customer\_condition\).|
|Standing Order|sn\_bom\_b2b\_standing\_order|Table to store standing instructions which is pre-authorized payment instruction given by a business customer to the bank. E.g. Auto bill payments|
|Standing Order|sn\_bom\_standing\_order|Table to store standing instructions which is pre-authorized payment instruction given by a individual customer to the bank. E.g. Auto bill payments|
|Stock|sn\_bom\_stock|Stores all stock information. Extends the Security \[sn\_bom\_security\] table.|
|Student Loan|sn\_bom\_student\_loan|Stores all student loan account records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Term Loan|sn\_bom\_term\_loan|Stores all term loan account records. Extends the Loan Account \[sn\_bom\_loan\_account\] table.|
|Trade|sn\_bom\_trad|To store information related to individual stock orders placed by investors.|
|Transaction|sn\_bom\_card\_transaction|Stores all card transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Transaction|sn\_bom\_deposit\_transaction|Stores all deposit transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Transaction|sn\_bom\_ins\_policy\_transaction|Stores all policy transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Transaction|sn\_bom\_investment\_transaction|Stores all investment transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Transaction|sn\_bom\_line\_of\_credit\_transaction|Stores all line of credit transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Transaction|sn\_bom\_loan\_transaction|Stores all loan transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|
|Vehicle|sn\_bom\_vehicle|Customer Property|
|Wire Transfer Financial Account|sn\_bom\_m2m\_wire\_transfer\_financial\_account|Financial Service Financial Account|
|Wire Transfer Service|sn\_bom\_wire\_transfer|Stores all wire transfer treasury service records. Extends the Financial Service \[sn\_bom\_service\] table.|
|Wire Transfer User|sn\_bom\_m2m\_wire\_transfer\_user|Stores details of users who are authorized to request for a wire transfer facility on a business deposit account|

**Parent Topic:**[Financial Services Operations Core](financial-services-operations-core-data-model.md)

