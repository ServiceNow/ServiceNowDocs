---
title: Search in contracts document
description: Ask question in the ServiceNow Otto panel to search for information in the content of the contract document.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cmpro-na-converse-ask-ques-new.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational contract search and insights Workflow, Use agentic workflows, Now Assist in Contract Management, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Search in contracts document

Ask question in the ServiceNow Otto panel to search for information in the content of the contract document.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

Conversational search enables you to find information by searching within the contract documents. By default the search results display the following columns:

-   Document: Document name in which content is found
-   Number: Contract number
-   Summary: AI-generated summary explaining what was found
-   Section details: Section of the document where the information was found

You can customize the columns to be displayed by using the **Personalize fields** option under the **More Actions** icon \(\[Omitted image "agent-workspace-more-ui-actions-icon.jpg"\] Alt text: More actions icon\). The columns you configure are also included when you export the search results.

Contract fulfillers and assignment group managers with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and nowi think\_assist\_panel\_user role can view the agentic workflow conversation in the ServiceNow Otto panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

For feature limitations, see [Explore Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md).

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

5.  View contract details.

    1.  Select CNTR number to view the contract details.

    2.  Select **Open request** to open the contract record.

6.  View contract document and search within it.

    The Document, Summary and Section details columns are available only when the search is performed within the contract document.

    1.  Select the link in the **Document** column to open the contract document.

    2.  View the document and enter text in the Search Document field to search within the document.

7.  Navigate to the Summary and Section columns to view the AI generated summary for the search and to view the specific section where the search result was found.


