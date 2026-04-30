---
title: Content pack for Financial Services Operations
description: Using the Process Mining content pack with Financial Services Operations \(FSO\) enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with FSO cases.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Content pack for Financial Services Operations

Using the Process Mining content pack with Financial Services Operations \(FSO\) enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with FSO cases.

**Important:** Starting with the Vancouver release, the Process Optimization application has been renamed to Process Mining.

For information about enabling the FSO Process Mining Content Pack, see [Activate Process Mining content packs](po-content-pack.md).

## Optimization projects

The content pack adds pre-built Process Mining project model definitions for these Financial Services Operations applications.

-   Financial Services Business Deposit Operations
-   Financial Services Business Loan Operations
-   Financial Services Business Lifecycle
-   Financial Services Card Operations
-   Financial Services Client Lifecycle
-   Financial Services Complaint Management
-   Financial Services Payment Operations
-   Financial Services Personal Loan Operations
-   Financial Services Personal Deposit Operations
-   Financial Services Treasury Operations
-   Individual Life Servicing
-   Group Life Servicing
-   Commercial Lines Claims
-   Personal Lines Claims
-   Intelligent Servicing for Fraud

You can also configure a new process project that is based on a pre-built project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

## Roles

Based on the Financial Services Operations application that you're using the Process Mining application for, you need the following roles.

|Financial Services Operations application|Required role|
|-----------------------------------------|-------------|
|Financial Services Card Operations|Dispute management: sn\_bom\_credit\_card.dispute\_manager and sn\_process\_optimization\_analyst|
|Financial Services Payment Operations|sn\_bom\_payment.payments\_manager and sn\_process\_optimization\_analyst|
|Financial Services Business Loan Operations|sn\_bom\_loan\_b2b.manager and sn\_process\_optimization\_analyst|
|Financial Services Personal Loan Operations|sn\_bom\_loan.b2c\_manager and sn\_process\_optimization\_analys|
|Financial Services Business Lifecycle|sn\_bom\_clo\_b2b.manager and sn\_process\_optimization\_analyst|
|Financial Services Client Lifecycle|sn\_bom\_clo\_b2c.manager and sn\_process\_optimization\_analyst|
|Financial Services Complaint Management|sn\_bom\_compl.manager and sn\_process\_optimization\_analyst|
|Financial Services Business Deposit Operations|sn\_bom\_deposit\_b2b.manager and sn\_process\_optimization\_analyst|
|Financial Services Personal Deposit Operations|sn\_bom\_deposit\_b2c.manager and sn\_process\_optimization\_analyst|
|Commercial Lines Claims|sn\_ins\_claim\_cml.manager and sn\_process\_optimization\_analyst|
|Personal Lines Claims|sn\_ins\_claim\_pers.manager and sn\_process\_optimization\_analyst|
|Financial Services Treasury Operations|sn\_bom\_treasury.admin and sn\_process\_optimization\_analyst|
|Individual Life Servicing|sn\_ins\_indiv\_life.manager and sn\_process\_optimization\_analyst|
|Group Life Servicing|sn\_ins\_group\_life.manager and sn\_process\_optimization\_analyst|
|Intelligent Servicing for Fraud|sn\_bom\_fraud.manager and sn\_process\_optimization\_analyst|

-   **[Example of Process Mining for Financial Services Operations](example-po-fso.md)**  
Analyze a process for financial services cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.

**Parent Topic:**[Activate Process Mining content packs](po-content-pack.md)

**Related topics**  


[Example of Process Mining for Financial Services Operations](example-po-fso.md)

