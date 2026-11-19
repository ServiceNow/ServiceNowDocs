---
title: Import external data using Process Mining
description: Process Mining analyzes process data from your ServiceNow instance by default. However, if your organization runs processes in external systems such as Workday or Salesforce, you can import that data into Process Mining to analyze those processes alongside your ServiceNow data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/import-ext-data.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-07-13"
reading_time_minutes: 2
breadcrumb: [Process Mining, Platform Analytics]
---

# Import external data using Process Mining

Process Mining analyzes process data from your ServiceNow instance by default. However, if your organization runs processes in external systems such as Workday or Salesforce, you can import that data into Process Mining to analyze those processes alongside your ServiceNow data.

## When to import external data

Import external data when the process you want to mine runs primarily in a system outside ServiceNow. For example:

-   Your HR team manages recruitment and onboarding in Workday, and you want to identify bottlenecks in the hiring process.
-   Your sales team runs some workflows in Salesforce, and you want to visualize process variants and deviations.

## Two ways to import external data

Process Mining supports two methods for importing external data.

|Method|Best for|Requires|
|------|--------|--------|
|Manual import via audit table|Any external system; one-time or infrequent imports; systems without a dedicated app|Process Mining plugin|
|App-based import|Supported systems \(Workday, Salesforce\); recurring imports; automated field mapping|Process Mining plugin + the respective app|

Use the manual audit table method when no dedicated app exists for your external system, or when you need full control over which fields to import and how to map them.

Use an app when one is available for your system. Apps automate the connection, field mapping, and scheduling, reducing setup time and the risk of mapping errors.

## Available applications

The following applications are available for app-based import:

-   Process Mining for Workday — Imports HR process data including recruitment, onboarding, and offboarding pipelines from Workday.
-   Process Mining for Salesforce — Imports CRM process data including lead-to-opportunity, quote-to-cash, and case management workflows from Salesforce.

Each application is a separate plugin that requires Process Mining to be active. You install and configure each app independently from the ServiceNow Store.

## Plugin dependency

Applications for external data can't function without Process Mining. Before activating any app, confirm that the Process Mining plugin is active on your instance. Each app listing in the ServiceNow Store lists the required Process Mining plugin version.

**Related topics**  


[Working with external datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/external-dataset.md)

[Process Mining for Workday and Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/pm-workday.md)

[pm-salesforce]

