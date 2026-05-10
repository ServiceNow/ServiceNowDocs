---
title: Analyze a contract document from Source-to-Pay Workspace
description: As a contract fulfiller, analyze a contract document with generative AI to identify non-standard and missing clauses.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Now Assist Contract Management, Source-to-Pay Operations integration Contract Management, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Analyze a contract document from Source-to-Pay Workspace

As a contract fulfiller, analyze a contract document with generative AI to identify non-standard and missing clauses.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller or sn\_cm\_core.contract\_fulfiller

## About this task

You can analyze an entire document and identify any non-standard or missing clauses by using generative AI with the Now Assist in Contract Management application. With generative AI, your organization can save time and effort by reducing the need for manual review.

For more information, see [Contract analysis using Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-NA-review-land.md).

## Procedure

1.  Open the **Source-to-Pay Workspace**.

2.  Navigate to **Lists** &gt; **My work** &gt; **Open contract requests**

3.  Select a contract request that is in Work in progress state.

    **Note:** You can analyze only the contracts that are in Work in progress state.

4.  If the contextual side panel isn’t open, select the Now Assist Contract Review by Now Assist icon \(![Contract Review by Now Assist icon](../image/cmpro-ai-sparkel-icon.png)\).

    You can analyze contracts in the Now Assist contextual side panel as shown in the following example.

    ![Analyze contracts with Now Assist contextual side panel](../image/cmpro-na-side-panel.png)

5.  On the contract request page, select **Contract documents**.

6.  Submit contract documents for Now Assist analysis.

    The latest versions of the documents are automatically selected for analysis.

<table id="choicetable_p3s_2gn_zcc"><thead><tr><th align="left" id="d85369e159">

Method

</th><th align="left" id="d85369e162">

Steps

</th></tr></thead><tbody><tr><td id="d85369e168">

**Run Now Assist analysis on a single contract document**

</td><td>

1.  On the **Contract documents** tab, select a contract document.
2.  From the contextual side panel, select **Analyze with Now Assist**.


</td></tr><tr><td id="d85369e195">

**Run Now Assist analysis on multiple contract documents**

</td><td>

1.  After opening a contract request, from the contextual side panel select **Analyze with Now Assist**.

**Note:** A list of contract documents that were submitted for the Now Assist analysis is displayed. Information about the documents and any errors that were found are also included.

2.  Select **Analyze contract**.


</td></tr></tbody>
</table>    After you select **Analyze with Now Assist**, you might encounter Restricted Caller Access \(RCA\) approval messages as shown in the image.

    ![RCA approvals for Now Assist in Contract Management.](../image/spo-cmro-rca-message.png)

    For more information about approving restricted caller access \(RCA\) privileges to allow cross-scope access to Now Assist in Contract Management, see [RCA approvals for Now Assist in Contract Management](approve-rca-contracts-spo.md).

7.  Select **Analyze contract**.

    1.  The Now Assist application creates a copy of the documents and starts analysis on the new documents. The status is now Analysis in progress.
    2.  A card is created for each document in Analyzed contracts with the Now Assist contextual panel. The contract status updates to the Awaiting review status.
    3.  When the analysis of the documents is complete, the status changes to Ready for review with the following details:

        |Section|Description|
        |-------|-----------|
        |Pending reviews|Displays the number of deviations reported and pending for review.|
        |Completed|Displays the number of reviewed deviations that have been reviewed and any actions taken.|

8.  Select the document card to view the details of the analysis.

    The details of the contract analysis are displayed with the Now Assist comments. The comments explain the reasons for marking a clause non-standard.

9.  View the analysis and select **Back** to go to the analyzed contracts in the Now Assist contextual side panel.

    You can only view the suggestions in the contextual side panel. To act on a suggestion, open a .docx Microsoft Word document and use the Microsoft Word add-in for ServiceNow Contracts. For more information, see [Contract analysis states in Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-states.md)


-   **[RCA approvals for Now Assist in Contract Management](approve-rca-contracts-spo.md)**  
Approve restricted caller access \(RCA\) privileges to allow cross-scope access to Now Assist in Contract Management.

**Parent Topic:**[Using Now Assist for Contract Management in Sourcing and Procurement Operations](../concept/use-now-assist-cmpro-spo.md)

**Related topics**  


[Enable Now Assist in Contract Management](activate-na-cmpro-spo.md)

[Start a metadata extraction for a contract from Source-to-Pay Workspace](extract-metadata-spo.md)

