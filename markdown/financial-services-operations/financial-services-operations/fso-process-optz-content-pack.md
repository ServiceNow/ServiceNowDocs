---
title: Process Mining for Financial Services Operations
description: The Financial Services Operations Process Mining Content Pack has preconfigured Process Mining models for Financial Services Operations processes that help analysts and process owners analyze how effective their business processes are.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Process Mining for Financial Services Operations

The Financial Services Operations Process Mining Content Pack has preconfigured Process Mining models for Financial Services Operations processes that help analysts and process owners analyze how effective their business processes are.

**Important:** Starting with the Vancouver release, the Process Optimization application has been renamed to Process Mining.

For information about enabling the FSO Process Mining Content Pack, see [Activate Process Mining content packs](https://www.servicenow.com/docs/access?context=po-content-pack&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

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

You can also configure a new process project that is based on a pre-built project. For more information, see .

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

**Parent Topic:**[Integration with other ServiceNow applications](fso-integrated-applications-overview.md)

