---
title: Ask Now Assist to generate summary of contract documents in a contract request
description: Generate summaries, frequently asked questions \(FAQs\), or ask questions to retrieve specific information from contract documents in Contract Management Pro.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Contract summarization, Summarize contract, Ask Now Assist]
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Ask Now Assist to generate summary of contract documents in a contract request

Generate summaries, frequently asked questions \(FAQs\), or ask questions to retrieve specific information from contract documents in Contract Management Pro.

## Before you begin

-   The smart documents skill must be activated. For more information, see [Configure the Smart Documents Skill for Now Assist in Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-skill-smart-documents.md).
-   Your role and relevant tables must be configured to use this feature. For more information, see [Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md).
-   The Now Assist panel must be enabled. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   Role required: sn\_cm\_core.contract\_fulfiller

## About this task

Use the Smart Documents capability in Now Assist for ServiceNow AI Platform to generate a summary and FAQs from contract documents, and ask questions in the Now Assist panel to retrieve specific information from contract documents.

## Procedure

1.  Open a contract request from the workspace that you are using.

<table id="table_ujj_bct_fgc"><thead><tr><th>

Method

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Contract Workspace

</td><td>

-   Navigate to **All** &gt; **Contract Workspace**.
-   Select the list icon ![](../../legal-request-management/image/lsd-lcc-list-icon.png).
-   Select **Contract requests** &gt; **All**.
-   Select a contract request.


</td></tr><tr><td>

Workspace used by your application

</td><td>

-   Navigate to your workspace.
-   Open the list that displays the contract requests.
-   Select a contract request.


</td></tr></tbody>
</table>2.  In the **Contract documents** tab, select **Preview document**.

    ![Preview document in a contract request.](../image/cmpro-preview-doc.png "Preview contract document")

3.  In the Preview document window, select the contract type, and then select **Preview**.

    The contract document opens in a document viewer.

4.  Select **Ask Now Assist**.

    ![Summarize button in the document viewer used to generate summary of a contract.](../image/cmpro-summarize-doc.png "Ask Now Assist")

    The Now Assist panel opens where you can select the option to summarize the contract, generate FAQs from the document, or ask questions to gain specific insights on the document.

    ![Now Assist panel displaying options to summarize the document, generate FAQs, and ask questions.](../image/cmpro-summary-nap.png "Contract summary options in the Now Assist panel")

    For more information on using Now Assist for generating summaries, see [Generate a document summary by using Now Assist in Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/generate-document-summary-now-assist.md) and [Generate summary and ask questions using Now Assist in Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ask-questions-faqs-now-assist.md).

    You can also summarize supporting documents and signed contracts using Ask Now Assist in the document viewer.


**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)

