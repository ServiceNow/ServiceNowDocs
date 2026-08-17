---
title: Search in contract metadata
description: Ask question in the ServiceNow Otto panel to search for information related to contract fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-na-search-metadata.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational contract search and insights Workflow, Use agentic workflows, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Search in contract metadata

Ask question in the ServiceNow Otto panel to search for information related to contract fields.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

Conversational search enables you to find information by searching across contract fields using natural language queries. When you ask questions about structured information—such as vendor names, contract dates, payment terms, or contract status —the system searches the contract metadata and returns matching contract records. By default the search results display the following columns:

-   Number
-   Contract model
-   Vendor
-   Start date
-   End date
-   State

You can customize the columns to be displayed by using the **Personalize fields** option under the **More Actions** icon \(\[Omitted image "agent-workspace-more-ui-actions-icon.jpg"\] Alt text: More actions icon\)\). The columns you configure are also included when you export the search results.

Contract fulfillers and assignment group managers with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and now\_assist\_panel\_user role can view the agentic workflow conversation in the ServiceNow Otto panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

For feature limitations, see [Explore ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md).

## Procedure

1.  Navigate to ServiceNow Otto panel.

2.  Enter a query in the ServiceNow Otto panel.

3.  Select **Show** to view the search results.

4.  Export the search results.

    The export includes all search results, not just the results currently displayed on screen.

    1.  Select **Export**.

    2.  From the File Type list, select the export format.

    3.  Select the **Download** option.

    4.  Select **Export**.

5.  Select CNTR number to view the contract details.

    \[Omitted image "cmpro-na-search-meta-viewresult.png"\] Alt text: Conversational search for contracts

6.  Select **Open request** to open the contract record.

    \[Omitted image "cmpro-na-converse-openreq.png"\] Alt text: Open contract request


