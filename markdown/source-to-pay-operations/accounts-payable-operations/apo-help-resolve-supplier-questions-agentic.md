---
title: Inquiry resolution provider AI agent
description: Use the Inquiry resolution provider AI agent to process high volume repetitive invoice inquiries through various channels \(web, email, virtual agent, mobile and manual entry\) to significantly reduce the workload of human agents.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Supplier questions]
breadcrumb: [Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Inquiry resolution provider AI agent

Use the Inquiry resolution provider AI agent to process high volume repetitive invoice inquiries through various channels \(web, email, virtual agent, mobile and manual entry\) to significantly reduce the workload of human agents.

## AI agents

The following table lists the agents that are used in the APO.

|AI agent|AI agent role|
|--------|-------------|
|Inquiry resolution provider|Analyzes the inquiry case record that is based on the invoice details and related data. It suggests the resolution details to agents autonomously and updates the invoice case record with the suggested resolution.|

## Tools mapped to the Inquiry resolution provider AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Invoice Inquiry resolution generator and case update|Collects the data related to invoice, invoice lines, invoice tax lines, exceptions, purchase order, purchase order line tables, knowledge base tables and generates resolution for an inquiry case and auto-updates the inquiry case record with the generated resolution. If invoice is not passed as input, the information is collected from the knowledge base article \(with the knowledge base configured in system properties\).|
|Scripts|Autonomous|Close the case|Closes the case if the user responds positively.|

**Related topics**  


[Invoice inquiry cases](work-with-inquiry-cases.md)

