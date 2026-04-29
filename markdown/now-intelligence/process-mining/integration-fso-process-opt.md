---
title: Content pack for Financial Services Operations
description: Using the Process Mining content pack with Financial Services Operations \(FSO\) enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with FSO cases.Analyze a process for financial services cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Financial Services Operations

Using the Process Mining content pack with Financial Services Operations \(FSO\) enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with FSO cases.

**Important:** Starting with the Vancouver release, the Process Optimization application has been renamed to Process Mining.

For information about enabling the FSO Process Mining Content Pack, see [Content pack for Financial Services Operations](integration-fso-process-opt.md#).

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

**Parent Topic:**[Activate content packs](../task/activate-po-content-pack.md)

**Related topics**  


[Example of Process Mining for Financial Services Operations](integration-fso-process-opt.md#)

## Example of Process Mining for Financial Services Operations

Analyze a process for financial services cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.

For example: If you’re a process analyst in your financial institution where you must submit analysis on current processes associated with financial services cases, you can use Analyst workbench to access the mined processes for the project definition for financial services payment operations, loan operations, and complaint management.

You can analyze the case process flow and suggest ways to improve the processes by using the following workflow, for example, for **Loan deferment in B2C** project definition:

1.  Select **View in Workspace** from the selected project. Analyst workbench opens in a new tab.

    You can observe the average duration that a Loan deferment case record takes to be closed.

2.  View metrics of the process map by setting the Primary Metric and Secondary Metric lists to **Unique Occurrences** and **Average Duration**, respectively.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You can observe the state transitions and their duration.

4.  In the **Filters** tab, set up the Breakdown filters list for categories and use the activity transitions filters to filter out the records.
5.  In the **Variation Analysis** tab, you can view the routes taken by the records, number of cases in a route, the average duration, and the number of steps involved in the route. Selecting a route highlights the route in the map.
6.  Add notes to the project by selecting the notes icon \(![Notes icon](../image/notes-icon.png)\) and submit an analysis.

![Example: Process Mining Analyst workbench for FSO](../image/example-po-fso.png "Process Mining for Loan deferment in B2C")

**Related topics**  


[Analyzing and getting process insights](analyze-get-process-insights.md)

[Content pack for Financial Services Operations](integration-fso-process-opt.md#)

