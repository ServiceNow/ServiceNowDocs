---
title: Search in contracts document
description: Ask question in the Now Assist panel to search for information in the content of the contract document.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational contract search and insights Workflow, Use agentic workflows, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Search in contracts document

Ask question in the Now Assist panel to search for information in the content of the contract document.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

Conversational search enables you to find information by searching within the contract documents. The system performs semantic searches through the document text and returns relevant matches. By default the search results display the following columns:

-   Document: Document name in which content is found
-   Number: Contract number
-   Summary: AI-generated summary explaining what was found
-   Section details: Section of the document where the information was found

You can customize the columns to be displayed by using the **Personalize fields** option under **More Actions** icon.

![Conversational search results for query related to content in the document](../image/cmpro-na-converse-rag-result.png)

Contract fulfillers and assignment group managers with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and now\_assist\_panel\_user role can view the agentic workflow conversation in the Now Assist panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

For feature limitations, see [Explore Now Assist in Contract Management](cncore-exp-now-assist-land.md).

## Procedure

1.  Navigate to Now Assist panel.

2.  Enter a query in the Now Assist panel.

    ![Conversational search for contracts](../image/cmpro-na-converse-result.png "Conversational search for contracts")

3.  Select **Show** to view the search results.

4.  View contract details.

    1.  Select CNTR number to view the contract details.

    2.  Select **Open request** to open the contract record.

5.  View contract document and search within it.

    The Document, Summary and Section details columns are available only when the search is performed within the contract document.

    1.  Select the link in the **Document** column to open the contract document.

        ![Open contract document](../image/cmpro-na-converse-docselect.png)

    2.  View the document and enter text in the Search Document field to search within the document.

        ![View and search in the document](../image/cmpro-na-converse-docview.png)

6.  Navigate to the Summary and Section columns to view the AI generated summary for the search and to view the specific section where the search result was found.


