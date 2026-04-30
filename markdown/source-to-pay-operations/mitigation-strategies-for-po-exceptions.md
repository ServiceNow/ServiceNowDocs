---
title: Identify and execute mitigation strategies for purchase order exceptions
description: Leverage the define PO exception mitigation strategy workflow to resolve purchase order exceptions and avoid the risk of critical part shortages. This agentic workflow helps buyers identify and execute the best mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-02-11"
reading_time_minutes: 1
breadcrumb: [Using agentic workflows in Now Assist for Purchase Order Management \(POM\), Now Assist for POM, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Identify and execute mitigation strategies for purchase order exceptions

Leverage the define PO exception mitigation strategy workflow to resolve purchase order exceptions and avoid the risk of critical part shortages. This agentic workflow helps buyers identify and execute the best mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.

## Define PO exception mitigation strategy agentic workflow overview

The Define PO exception mitigation strategy agentic workflow analyzes purchase order exceptions and generates actionable mitigation strategies by calculating delivery gap schedules.

## Accessing the define PO exception mitigation strategy agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Define PO exception mitigation strategy**.

## AvailabIe agents

The following table lists the agents that are used in the Define PO exception mitigation strategy workflow.

|AI agent|AI agent role|
|--------|-------------|
|Purchase order plan creation AI agent|Analyzes purchase order exceptions and generates actionable mitigation strategies by calculating delivery gap schedules. It identifies alternative purchase order lines from different suppliers, and creates optimized change requests that combine supplier-suggested modifications with buyer-approved mitigation plans.|

## Tools mapped to the Purchase order plan creation AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Create Change Requests|Creates Purchase Request \(PR\) records of type 'revision' to implement approved mitigation changes.|
|Scripts|Autonomous|Fetch Exception and Gap Schedule Details|Retrieves the purchase order exception details and delivery gap schedule.|
|Scripts|Autonomous|Get Editable Purchase Orders|Searches for alternative purchase order lines that can be modified to resolve delivery gaps.|

