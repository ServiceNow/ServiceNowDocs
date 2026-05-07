---
title: Accounts Payable Operations glossary
description: Learn about the terms and concepts used in Accounts Payable Operations \(APO\).
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
keywords: [glossary terms, Account Number, Invoice Stage Field, Agent, Accounts Payable Invoice Processing, Accounts Payable Operations \(APO\), Accounts Payable Operations Integration with Document Intelligence, Accounts Payable Specialist, ACH Routing Number, Invoice Stage Field, AR Invoice, Business Object, AR Invoice Line, Business Object, Awaiting Internal Info, Invoice Case State, Awaiting Requester Info, Invoice Case State, glossary terms, Business Owner, glossary terms, Credit Memo, Cost Allocation, Cost Center, cXML, glossary terms, Distribution Lines, Distribution Set, Duplicate Invoice Detection, glossary terms, ERP, ERP Integration Framework, ERP Source, Exception Engine, Exception Monitoring Job, Exception Task, Extraction Confidence, glossary terms, GL, glossary terms, Inbound Staging Tables, Inquiry Case, Integration Error, Interaction Record, Invoice approval, Invoice Automation, Invoice Case, Invoice Ingestion API, Invoice Line, Invoice Line Mapping, Invoice Processing Case, Invoice Table Restructuring, ITAM, ITAM Integration, glossary terms, Ledger Account \(General Ledger Account/GL Account\), Legal Entity, glossary terms, Natural Language Understanding \(NLU\), NLU, Non-PO Invoice, glossary terms, Outbound Staging Table, glossary terms, Playbook, PO Invoice, PO Matching, PSM, glossary terms, Receipt Task, Receiving Slip, Rules-Based Engine, glossary terms, Staging Tables, Supplier, Supplier Collaboration Portal, Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\), Supplier Tax, Source-to-Pay Workspace, System Tax, glossary terms, Tax Calculation, Tax Line, Tax Type, Tolerance Type, Transformation Process, glossary terms, Universal Request \(UR\), UR, glossary terms, Virtual Agent Flows, glossary terms, Workflow, Work Item]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Accounts Payable Operations glossary

Learn about the terms and concepts used in Accounts Payable Operations \(APO\).

Glossary terms are grouped alphabetically.

[A](apo-glossary.md#) \| [B](apo-glossary.md#)\| [C](apo-glossary.md#)\| [D](apo-glossary.md#) \| [E](apo-glossary.md#) \| [G](apo-glossary.md#) \| [I](apo-glossary.md#) \| [L](apo-glossary.md#) \| [N](apo-glossary.md#) \| [O](apo-glossary.md#) \| [P](apo-glossary.md#) \| [R](apo-glossary.md#) \| [S](apo-glossary.md#) \| [T](apo-glossary.md#) \| [U](apo-glossary.md#) \| [V](apo-glossary.md#) \| [W](apo-glossary.md#)

**Parent Topic:**[Accounts Payable Operations reference](../reference/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties](../reference/acc-pay-properties.md)

[Create New Invoice Line form](../reference/create-invoice-line-form.md)

[Create invoice cost allocation form](../reference/create-invoice-cost-allocation-form.md)

[Outbound cost allocation staging table](../reference/outbound-cost-allocation-table.md)

[Distribution set form](../reference/distribution-set-form.md)

[Create New Invoice case form](../reference/create-new-ap-case-form.md)

[Create New Invoice task form](../reference/create-apm-task-form.md)

[Invoice processing case form](../reference/invoice-processing-case-form.md)

[Tax lines](../reference/create-tax-lines-apo.md)

[Invoice exception form](../reference/exception-form-fields.md)

[Request Help form](../reference/ur-request-help-form.md)

[Master data table for Accounts Payable Operations](../reference/master-data-table-apo.md)

[Invoice exception definition form](../reference/invoice-exception-definition-form.md)

[Approval Rule form](../reference/new-approval-rule-form.md)

[Approval Plan form](../reference/approval-plan-form.md)

## A

### account number

The supplier's bank account number for payment processing. Displayed when capturing invoice details from documents.

### Accounts Payable

The process of managing and paying invoices from suppliers.

### Accounts payable agent

User role \(sn\_ap\_cm.agent\) who handles inquiry cases from suppliers or employees in the Source-to-Pay workspace.

### Accounts payable invoice processing

Application that identifies invoice duplicates, matches invoices to purchase orders and goods receipts, enables invoice approval management, and provides invoice exception management.

### Accounts Payable Operations \(APO\)

A ServiceNow application that enables automated invoice processing, case management, and supplier inquiry handling from invoice ingestion to approval and payment.

### Accounts Payable Operations Integration with Document Intelligence

Application \(com.sn\_ap\_ic\) that automatically captures data from incoming invoices using Document Intelligence capabilities to reduce manual data entry effort.

### Accounts payable specialist

User role \(sn\_ap\_apm.accounts\_payable\_specialist\) who processes invoices, resolves exceptions, and manages invoice cases in the Source-to-Pay workspace.

### ACH Routing Number

The Automated Clearing House routing number used for electronic payment transfers to suppliers. Captured during invoice ingestion.

### Approval workflow

The sequence of steps required to approve an invoice.

### Advanced work assignment for Accounts Payable Operations

An application that automatically assigns work items to agents based on their availability, capacity, and skills to resolve invoice cases within Accounts Payable Operations.

### Agent workspace

A suite of tools that provides agents, case managers, help desk professionals, and managers quick access to what they need to help answer customer questions and resolve customer problems.This is the unified interface where accounts payable teams manage their day-to-day operations.

### AI agents

AI agents are autonomous digital workers that use LLMs, tools, and workflows to complete tasks across ITSM, HR, and CSM on behalf of users. They can reason, plan, and act independently or collaboratively. You can create and manage them using AI Agent Studio and orchestrate them in AI Agent Orchestrator. These agents are embedded in Now Assist panels, Virtual Agent, and custom workflows.

The AI agent is a virtual worker that performs specific tasks leveraging tools from the ServiceNow AI Platform such as workflow, skill, script, knowledge base, etc.

### Assignment rules

Guidelines that determine how work items are assigned.

### AR invoice

An Accounts Receivable invoice record representing amounts owed by customers. Also referred to as "Invoice" in the system.

### AR invoice line

Individual line items within an accounts receivable invoice, representing specific goods or services billed.

### Awaiting Internal Info

A case state indicating that resolution is pending because additional information is needed from internal teams.

### Awaiting Requester Info

A case state indicating that the case is waiting for additional information from the person who submitted the inquiry.

## B

### Business owner

Individual responsible for approving invoice or managing exceptions; must be valid and active, matching purchase order if invoice is PO type.

## C

### case

A record that is used to track and manage a specific customer issue, request, or incident. It is commonly used in resolving issues through customer support and helpdesk systems.

### Credit memo

Invoice type issued when there is a reduction or offset in amount payable to supplier; can be PO or Non-PO type and must contain original invoice, original invoice number, or purchase order reference.

### cost allocation

Process of identifying and allocating invoice line costs across different cost centers or ledger accounts for accurate cost analysis and invoice processing.

### cost center

Business unit or department to which invoice costs are allocated; used in cost allocation records for expense tracking and reporting.

### cXML

Commerce XML- one of the supported formats for invoice ingestion via API.

## D

### data capture

The process of collecting and digitizing invoice data.

### Document Intelligence

ServiceNow® AI-powered tool for extracting data from invoices.

### data security

Measures to protect sensitive information within the system.

### distribution lines

Individual allocation records within a distribution set that specify percentages or amounts to distribute across cost centers or general ledger accounts.

### distribution set

Collection of predefined rules and templates designed to automate cost allocation for invoice lines across cost centers and GL accounts, eliminating manual cost splitting.

### Duplicate invoice detection

Automated process that identifies invoices that may have already been submitted to prevent the same invoice from being paid twice.

## E

### Enterprise resource planning systems

Enterprise resource planning \(ERP\) systems used for managing business processes.

### ERP

Enterprise Resource Planning - external system integrated with APO for invoice posting and payment processing.

### ERP integration framework

Framework enabling APO to post invoices to external ERP systems and track integration errors when posting fails due to data issues or connectivity problems.

### ERP Source

External ERP system reference that ensures consistent data sourcing for invoice fields like purchase order, legal entity, supplier to prevent integration errors.

### Exception engine

Automated system component that identifies discrepancies in invoices during processing and creates invoice exception records for review and resolution.

### Exception management

Handling and resolving issues that arise during Accounts Payable Operations invoice processing.

### Exception monitoring job

Scheduled job running every five minutes, by default, to automatically check invoices for exceptions; can be activated or run manually.

### Exception task

Task created to resolve specific invoice exceptions; can be auto-created by the system \(for example, receipt tasks\) or manually created by Accounts Payable Specialists.

### Extraction confidence

Confidence level score assigned by Document Intelligence when extracting data from invoice documents; determines if manual review is required.

## G

### GL

Acronym for General Ledger.

## I

### Inbound staging tables in APO

Temporary tables that store invoice data received from external systems before transformation and creation of primary invoice records in APO.

### Inquiry case

Case type submitted by employees or suppliers for invoice-related questions, including payment inquiry, invoice inquiry, expedite payment request, payment terms issues, and invoice entry assistance.

### Integration error

System-generated error task recording integration issues when invoices fail to post to ERP systems due to poor connectivity, missing data, or system timeouts.

### Interaction record

Auto-generated record logging any supplier or employee request for assistance via email, chat, or phone; can be associated with existing cases or used to create new cases.

### Invoice approval

The process of verifying and authorizing an invoice for payment.

### Invoice automation

Case category for automated invoice processing cases created when invoices are ingested through Document Intelligence or API.

### Invoice case

Case record created to manage invoice-related inquiries or processing activities, with categories including Inquiry and Invoice automation.

### Invoice exception

Issues identified during invoice processing that require resolution.

### Invoice ingestion

The process of receiving and entering invoices into the system.

### Invoice ingestion API

Application programming interface that enables bulk AP invoice ingestion from external systems \(supplier billing, buyer networks, OCR solutions\) supporting cXML, JSON, and XML formats.

### Invoice line

Individual line item on an invoice representing specific goods or services purchased; includes quantity, unit price, amount, and cost allocation details.

### Invoice line mapping

Process of matching invoice lines with corresponding purchase order lines using rules-based engine or Now Assist for automated or AI-assisted mapping.

### Invoice processing

The end-to-end handling of invoices from receipt to payment.

### Invoice processing case

Case with category "Invoice automation" and subcategory "Invoice processing" created when invoices are ingested; tracks invoice through complete processing life cycle.

### Invoice table restructuring in APO

Architectural change where invoice table \(sn\_shop\_invoice\) extends base invoice table \(sn\_fin\_base\_invoice\) for improved data structure and extensibility.

### ITAM

Acronym for IT Asset Management.

### ITAM Integration

Integration between IT Asset Management and APO that enhances exception handling for ITAM-driven purchase order invoices by validating received quantities against receiving slips.

## L

### Ledger account

Financial account to which invoice costs are posted; used in cost allocation to distribute expenses across different accounting categories.

### Legal entity

Required field on invoices representing the business entity responsible for payment; used in supplier legal entity mapping and ERP source determination.

## N

### Natural Language Understanding \(NLU\)

AI capability integrated with virtual agent chatbot to help suppliers analyze, understand, and navigate to appropriate topics for invoice and inquiry-related queries.

### NLU

Acronym for Natural Language Understanding.

### Non-PO invoice

Invoice submitted without reference to a purchase order; requires manual coding and validation of supplier, legal entity, and cost allocation details.

## O

### Optical Character Recognition \(OCR\)

A technology that converts scanned contract documents or PDFs into searchable and editable text within ServiceNow.

### Outbound Staging Table in APO

Table where approved invoices are posted before transmission to external ERP systems for payment processing.

## P

### Playbook

Visual workflow representation showing step-by-step invoice processing stages including validation, duplicate checking, matching, exception validation, approval, and payment processing.

### PO invoice

Invoice created against a purchase order; undergoes PO matching to verify quantities, prices, and amounts against the original purchase order.

### PO matching

Process of comparing invoice header and line details with corresponding purchase order information to identify discrepancies before approval.

### PSM

Acronym for Procurement Service Management.

### Purchase order

A document issued by a buyer to a seller, detailing the items or services to be purchased.

## R

### Receipt task

Task created by APO when Insufficient Goods Receipt exception occurs and PSM is installed; assigned to recipient on PO line for goods receipt confirmation.

### Receiving slip

Document generated in ITAM when goods receipt is completed; used to validate received quantities during invoice processing for ITAM-driven purchase orders.

### Rules-based engine

Automated system that maps invoice lines with purchase order lines using fields like unit price, delivered unit price, exact description, exact amount, and amount round off.

## S

### Staging Tables

Temporary database tables storing invoice data during ingestion and transformation process before creation of final invoice records; includes inbound and outbound tables.

### Supplier

Vendor or service provider submitting invoices for payment; must be validated and mapped to legal entity in Supplier Legal Entity Mapping table.

### Supplier collaboration portal

Portal application enabling suppliers to check invoice status, create inquiry cases, submit new invoices, resolve tasks, and interact with AP specialists through chat and virtual agents.

### Supplier Legal Entity Mapping

Table \(sn\_fin\_supplier\_detail\) storing relationships between suppliers and legal entities, including hold payment and hold posting attributes that can trigger invoice exceptions.

### supplier management

The process of managing relationships and transactions with suppliers.

### Supplier tax

Tax amount provided by the supplier on the invoice; compared against system-calculated tax to identify over/under tax variances.

### Source-to-Pay Workspace

Workspace where Accounts Payable specialists and admins create cases, manage invoices, resolve exceptions, and manage integrations with other applications.

### System tax

Tax amount calculated by APO system based on tax type and invoice line amount; compared against supplier tax for validation.

## T

### Tax calculation

Process of computing final tax for invoices based on tax type \(indirect tax or withholding tax\) and comparing supplier-provided tax against system-calculated tax.

### Tax line

Individual tax record added to invoice line specifying tax type, supplier tax amount, system tax amount, and final tax amount after variance resolution.

### Tax type

Classification of tax as either indirect tax \(added to invoice amount\) or withholding tax \(subtracted from invoice amount\) for proper tax calculation.

### Tolerance type

Specific type of tolerance including Line amount tolerance, Line quantity tolerance, Line unit price tolerance, Overbilling amount tolerance, and Over/Under tax amount variance.

### tolerance rules

A limit that is set on invoices to determine acceptable variances before they require further review.

### Transformation process

Document Intelligence process that imports invoice data from staging tables, validates required fields, and creates invoice records in Draft state.

## U

### Universal request

Centralized entry point for invoice owners, suppliers, and customers to submit general case requests, simplifying the process of raising inquiries through Employee Center or Supplier Portal.

### UR

Acronym for Universal Request.

## V

### virtual agent

An AI-driven assistant for handling common requests and inquiries.

### Virtual agent flows

Predefined chatbot conversation topics including Check invoice status, Live agent support, Check inquiry status, Create new inquiry, and Prechat survey.

## W

### workflow

Automated process flow managing invoice progression through various stages from ingestion, validation, matching, exception handling, approval to payment.

### work item

Task or interaction record representing customer requests that need assignment and processing; routed through Advanced Work Assignment queues.

### Work item queue

A storage area for work items waiting to be assigned to agents.

