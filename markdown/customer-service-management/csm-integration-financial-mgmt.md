---
title: Integrating with Financial Management
description: Customer Service Management and Field Service Management provide an integration with the ServiceNow Financial Management application as well as dashboards and reports.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integrate, Customer Service Management]
---

# Integrating with Financial Management

Customer Service Management and Field Service Management provide an integration with the ServiceNow® Financial Management application as well as dashboards and reports.

The Financial Management application enables you to allocate, track, and report on expenses in your organization. When the Financial Management application allocates an expense, it breaks down the expense into detailed amounts of money called allocations. These allocations can be associated with specific segments and accounts for a specific cost model. The integration with Financial Management provides cost allocations for Customer Service Management and Field Service Management.

Use these cost allocations on the Financial Management workbench, which provides financial administrators with a graphical interface to allocate expenses. Access the workbench through the **Cost Transparency** &gt; **Workbench** module.

## Plugins

Two different plugins, one for Customer Service Management and one for Field Service Management, enable the integration with Financial Management. These plugins also add dashboards based on cost allocations.

-   Performance Analytics - Content Pack - Financial Management for Customer Service plugin \(com.snc.pa.fm.csm\).
-   Performance Analytics - Content Pack - Financial Management for Field Service Management plugin \(com.snc.pa.fm.fsm\)

The Performance Analytics - Content Pack - Financial Management for Customer Service plugin includes demo data for FY16: Q1 through FY17: Q2. The demo data includes records with the CSFM prefix, which indicates that the records are for the Customer Service Management integration with Financial Management. Activating the plugin adds these records to the Case \(sn\_customerservice\_case\) table.

**Note:** The Performance Analytics - Content Pack - Financial Management for Field Service Management plugin doesn’t include demo data.

## Cost models

A cost model is a set of rules, methods, and metrics that determines the allocation of expenses. Select cost models on the Data Definitions tab of the Financial Management workbench.

For Customer Service Management, the integration with Financial Management provides these cost models:

-   **CSM Allocation Model for Cost Account**: Allocates expenses for individual B2B customer accounts.
-   **CSM Allocation Model for Channels**: Allocates expenses for communication channels.

For Field Service Management, the integration with Financial Management provides this cost model:

**FSM Allocation Model for Company**: Allocates expenses for companies.

## Segment hierarchy

All accounts in the chart of accounts belong to segments which are structured in a hierarchy. This hierarchy enables the roll-up of expenses from lower-level accounts and segments to higher-level accounts and segments.

-   **CSM Allocation Model for Cust Account** uses this segment hierarchy: Assignment Group &gt; Product &gt; Customer Account.
-   **CSM Allocation Model for Channels** uses this segment hierarchy: Assignment Group &gt; Product &gt; Channels.
-   **FSM Allocation Model for Company** uses this segment hierarchy: Assignment Group &gt; Product &gt; Company.

## Account buckets

Use account buckets to categorize cleansed expenses before assigning them to accounts and segments. Account buckets can be organized in parent-child relationships so that several child buckets can refer to a single parent bucket.

The Customer Support and Field Service Support account buckets include:

-   Facilities
-   IT Chargeback
-   Payroll and Labor Expenses
-   Professional Fees &amp; Services
-   Supplies
-   Training
-   Other expenses

## Allocation metrics

Allocation metrics are rules that you can create and use to split an allocation based on dimensions such as:

-   Number of Customer Service cases: Allocate expenses to a product based on the number of cases closed in a fiscal period.
-   Total Customer Service case resolution time: Allocate expenses to a product based on the total hours worked on cases closed in a fiscal period.
-   Number of Field Service work order tasks: Allocates expenses to a product based on the number of work order tasks completed in a fiscal period.
-   Total work order completion time: Allocates expenses to a product based on the total hours worked on tasks completed in a fiscal period.

For Customer Service Management, the integration with Financial Management provides these allocation metrics:

-   CSM Allocate to Assignment Groups by Headcount
-   CSM Allocate to Product by \# Cases
-   CSM Allocate to Product by Case Time Worked Duration
-   CSM Rollup from AssgGrp to Product by \# Cases
-   CSM Rollup from AssgGrp to Product by Case Time Worked Duration
-   CSM Rollup from Product to Account by \# Cases
-   CSM Rollup from Product to Account by Case Time Worked Duration

For Field Service Management, the integration with Financial Management provides these allocation metrics:

-   FSM Allocate to Assignment Groups by Headcount
-   FSM Allocate to Product by \# Work Orders
-   FSM Rollup from Product to Company by \# Work Orders

## User roles

These roles can access the Financial Management workbench \(**Cost Transparency** &gt; **Workbench**\):

-   cost\_transparency\_analyst
-   cost\_transparency\_admin
-   financial\_mgmt\_user
-   financial\_mgmt\_admin

## Dashboards and reports

The Performance Analytics - Content Pack - Financial Management for Customer Service and Performance Analytics - Content Pack - Financial Management for Field Service Management plugins provide the following dashboards:

-   CSM Financials Dashboard
-   FSM Financials Dashboard

Navigate to **Performance Analytics** &gt; **Dashboards** and select the desired dashboard from the Dashboard menu.

**Related topics**  


[bundle-itbm.c_ITFinance]

[bundle-itbm.c_TheITFinanceWorkbench]

