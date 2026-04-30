---
title: Review the Now Assist suggestions for clause deviations
description: Review the Now Assist suggestions for clause deviations and take actions by using the Now Assist in Contract Management application to ensure that the clauses comply with the guidelines of the company.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-10-01"
reading_time_minutes: 5
breadcrumb: [Contract analysis using Now Assist in Contract Management, Using Now Assist in Contract Management, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Review the Now Assist suggestions for clause deviations

Review the Now Assist suggestions for clause deviations and take actions by using the Now Assist in Contract Management application to ensure that the clauses comply with the guidelines of the company.

## Before you begin

Before you start to review a document, make sure that the document has been analyzed by the Now Assist application. For more information, see [Analyze a contract document](cmpro-analyze-contract-doc.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_cm\_core.contract\_fulfiller

## About this task

A clause is a section in a contract document that outlines the guidelines of the company agreement, such as the purpose, term, or confidentiality.

-   As an assigned-to collaborator or group manager with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role, review and act on the suggestions from the contract analysis when the contract request is in the Work in progress state.
-   The Microsoft Word add-in for ServiceNow Contracts isn’t supported when the document is opened from the Google Drive. If you're using Google Drive for external storage, you must download the document from Google Drive and work on it offline.
-   If you're using the Microsoft OneDrive configuration for external storage, you can work on the document online or download it to work on it offline.
-   If you work on the suggestions offline, you must upload the document manually by creating a revision in the contract request. For more information, see [Create a document revision](cncore-create-doc-rev.md).

## Procedure

1.  Open the contract request from the workspace that you’re using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d232380e134">

Method

</th><th align="left" id="d232380e137">

Steps

</th></tr></thead><tbody><tr><td id="d232380e143">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Contract requests** &gt; **All**.
4.  Select a contract request.


</td></tr><tr><td id="d232380e191">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  Select **Contract documents**.

3.  If the contextual side panel isn’t open, select the Now Assist Review for contracts icon \(![Now Assist Review from contracts icon](../image/cmpro-ai-sparkel-icon.png)\).

4.  From the document card, select **Open document**.

    The following table describes the different storage options for internal or external contract downloads.

<table id="table_yy5_yq5_zcc"><thead><tr><th>

Storage

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Internal storage

</td><td>

The document is downloaded into your local system.

</td></tr><tr><td>

External storage:1.  Microsoft OneDrive
2.  Google Drive


</td><td>

The document opens online from the external storage.

</td></tr></tbody>
</table>5.  If you configure Google Drive, download the document and open it offline to review the Now Assist suggestions.

6.  Review the Now Assist suggestions.

    1.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

        For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

    2.  Enter the legal fulfiller credentials to log in.

        The ServiceNow Contracts add-in displays the tabs as listed in the following table.

<table id="table_hh4_5w2_xcc"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Review analysis**

</td><td>

-   **Pending reviews**: Lists all the non-standard clauses and missing clauses.
-   **Completed**: Lists all the completed actions over the clause.


</td></tr><tr><td>

**Clause library**

</td><td>

Lists all the standard clauses that are active for the contract type that the document belongs to.

</td></tr></tbody>
</table>    3.  On the **Review Analysis** tab, select **Pending reviews** to review the Now Assist suggestions.

7.  Work on a clause that is tagged as non-standard.

    1.  On the **Pending reviews** tab, select the clause card that is tagged as **non-standard**.

        -   Microsoft Word navigates to the clause that is associated with the clause card. If it doesn't navigate you to the clause, you must manually navigate to the clause.
        -   The following suggestions are displayed in the card:
            -   Now Assist comment: Now Assist feedback depending on the clause and the expected responses.
            -   Standard clause suggestion: Standard clause content suggestion that is.
            -   Show more/less: Option to expand or collapse the text.
    2.  Accept or ignore the Now Assist suggestion.

<table id="choicetable_zsg_1gb_1dc"><thead><tr><th align="left" id="d232380e510">

Action

</th><th align="left" id="d232380e513">

Steps

</th></tr></thead><tbody><tr><td id="d232380e519">

**Replace the non-standard clause**

</td><td>

-   Select the clause content in the document that needs to be replaced.
-   Select **Use this clause**.


</td></tr><tr><td id="d232380e540">

**Ignore suggestion**

</td><td>

Select **Ignore**.

</td></tr></tbody>
</table>8.  Work on a clause that is tagged as missing.

    1.  On the **Pending reviews** tab, select the clause card that is tagged as non-standard.

    2.  Accept or ignore the Now Assist suggestion.

    |Action|Steps|
    |------|-----|
    |**Add missing clause**|Select **Use this clause**.|
    |**Ignore suggestion**|Select **Ignore**.|

9.  Review the remaining non-standard and missing clauses and act as required.

    As you review the clauses and take action, they’re moved to the **Completed** tab with the details of the action taken.

10. Add a clause from the clause library.

    1.  Select the **Clause library** tab.

    2.  Search the clause by using the clause name.

        The active clauses for the contract type that is associated with the contract document are displayed.

    3.  Select the clause in the library.

    4.  Place the cursor on the document where you want to add the clause.

    5.  Select **Use this clause**.

    The clause is added to the document. When a valid metadata mapping exists within the clause content, the metadata gets auto-populated. Otherwise, a content control tag name is added and the metadata has to be manually updated. For more information, see [Configure metadata for fields, variables, and variables sets in a contract document](cncore-addin-add-metadata.md).

11. Mark the review as complete.

    1.  Select **Mark as complete**.

    2.  Select **Yes** to mark the review complete.

        You can select **Cancel** to continue working on the suggestions.

    -   The review is marked as complete and the file is updated in the configured storage.
    -   After the review is marked complete, you can't take any further actions even if there are pending reviews.
    -   The Contract state is updated to Work in progress and the Contract status is updated to Review completed.
    **Note:** If you downloaded the document to work on it offline, you must upload the document manually by creating a revision. For more information, see [Create a document revision](cncore-create-doc-rev.md).


**Parent Topic:**[Contract analysis using Now Assist in Contract Management](../concept/cncore-NA-review-land.md)

