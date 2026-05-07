---
title: Analyze a contract document
description: Analyze a contract document with generative AI to identify non-standard and missing clauses. You can do this task by using the Now Assist in Contract Management application.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Contract analysis, Use generative AI skills, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Analyze a contract document

Analyze a contract document with generative AI to identify non-standard and missing clauses. You can do this task by using the Now Assist in Contract Management application.

## Before you begin

Ensure that Now Assist has data access for your role. For more information, see [Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

-   As an assigned-to collaborator or group manager with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role, you can initiate a Now Assist analysis for a contract document when the contract request is in the Work in progress state.
-   The Now Assist analysis is run on the latest revision of the contract document.
-   Only documents in Microsoft Word \(.docx\) and PDF formats can be analyzed with the Now Assist application. For more information on the document limitations, see [Limitations in Document Intelligence](https://www.servicenow.com/docs/access?context=hard-limits-in-doc-intel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   For contract documents that are in a PDF format, you can run the Now Assist analysis but you can't act on a suggestion.

**Note:** Be sure to review the AI-generated analysis for accuracy.

## Procedure

1.  Open the contract request from the workspace that you’re using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d521045e135">

Method

</th><th align="left" id="d521045e138">

Steps

</th></tr></thead><tbody><tr><td id="d521045e144">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon ![](../../legal-request-management/image/lsd-lcc-list-icon.png).
3.  Select **Contract requests** &gt; **All**.
4.  Select a contract request.


</td></tr><tr><td id="d521045e191">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  If the contextual side panel isn’t open, select the Now Assist Review for contracts icon ![](../image/cmpro-ai-sparkel-icon.png).

    You can analyze contracts in the Now Assist contextual side panel as shown in the following example.

    ![Analyze contracts with the Now Assist contextual side panel.](../image/cmpro-na-side-panel.png)

3.  On the contract request page, select **Contract documents**.

4.  Submit contract documents for Now Assist analysis.

    The latest versions of the documents are automatically selected for analysis.

<table id="choicetable_p3s_2gn_zcc"><thead><tr><th align="left" id="d521045e266">

Method

</th><th align="left" id="d521045e269">

Steps

</th></tr></thead><tbody><tr><td id="d521045e275">

**Run Now Assist analysis on a single contract document**

</td><td>

1.  On the **Contract documents** tab, select a contract document.
2.  From the contextual side panel, select **Analyze with Now Assist**.


</td></tr><tr><td id="d521045e302">

**Run Now Assist analysis on multiple contract documents**

</td><td>

1.  After opening a contract request, from the contextual side panel, select **Analyze with Now Assist**.

**Note:** A list of contract documents that were submitted for the Now Assist analysis is displayed. Information about the documents and any errors that were found are also included.

2.  Select **Analyze contract**.


</td></tr></tbody>
</table>    1.  The Now Assist application creates a copy of the documents and starts analysis on the new documents. The contract analysis state is now Analysis in progress.
    2.  A card is created for each document in Analyzed contracts with the Now Assist contextual panel. The contract status updates to the Awaiting review.
    3.  When the analysis of the documents is complete, the state changes to Ready for review with the following details:

        |Section|Description|
        |-------|-----------|
        |Pending reviews|Displays the number of deviations reported and pending for review.|
        |Completed|Displays the number of reviewed deviations that have been reviewed and any actions taken.|

5.  Select the document card to view the details of the analysis.

    The details of the contract analysis are displayed with the Now Assist comments. The comments explain the reasons for marking a clause non-standard.

6.  Review the Now Assist suggestions and provide feedback to help improve the accuracy of Now Assist contract analysis over time.

    1.  For each suggestion, select the thumbs up icon ![](../../../reuse/icons/product-icons/thumbs-up-outline-24.svg) if the suggestion is helpful or the thumbs down icon ![](../../../reuse/icons/product-icons/thumbs-down-outline-24.svg) if the suggestion is not helpful.

    2.  In the pop-up, select the options that best describe your experience.

        You can select multiple options and add optional comments.

    3.  Select **Submit**.

    The feedback is captured in the Contracts Gen AI Feedback \[sn\_cm\_gen\_ai\_feedback\] table.

7.  Go to the analyzed contracts in the Now Assist contextual side panel by selecting **Back**.

    You can only view the suggestions in the contextual side panel. To act on a suggestion, open a .docx Microsoft Word document and use the Microsoft Word add-in for ServiceNow Contracts. For more information, see [Review the Now Assist suggestions for clause deviations](cmpro-review-contract-document.md).


**Parent Topic:**[Contract analysis using Now Assist in Contract Management](../concept/cncore-NA-review-land.md)

