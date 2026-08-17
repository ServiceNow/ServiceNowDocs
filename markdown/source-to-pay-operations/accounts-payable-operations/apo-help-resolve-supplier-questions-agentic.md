---
title: Inquiry resolution provider AI agent
description: Use the Inquiry resolution provider AI agent to process high volume repetitive invoice inquiries across multiple channels to significantly reduce the workload of human agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/apo-help-resolve-supplier-questions-agentic.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Supplier inquiries, APO, Accounts Payable Operations, Invoice inquiry resolution, AI agent, Autonomous resolution, virtual agent]
breadcrumb: [Use AI agents in ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Inquiry resolution provider AI agent

Use the Inquiry resolution provider AI agent to process high volume repetitive invoice inquiries across multiple channels to significantly reduce the workload of human agents.

## AI agents

The following table lists the agents that are used in the APO.

|AI agent|AI agent role|
|--------|-------------|
|Inquiry resolution provider|Analyzes the inquiry case record that is based on the invoice details and related data. It suggests the resolution details to agents autonomously and updates the invoice case record with the suggested resolution.|

## Tools mapped to the Inquiry resolution provider AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Invoice Inquiry resolution generator and case update|Collects data from invoice, invoice lines, invoice tax lines, exceptions, purchase order, and purchase order line tables. Generates a resolution for an inquiry case and updates the case record. If no invoice is provided as input, collects information from the knowledge base article configured in system properties.|
|Scripts|Autonomous|Close the case|Closes the case if the user responds positively.|

**Related topics**  


[Invoice inquiry cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-inquiry-cases.md)

