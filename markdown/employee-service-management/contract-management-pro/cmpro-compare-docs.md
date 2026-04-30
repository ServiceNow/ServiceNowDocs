---
title: Compare contract revisions in Contract Management Pro
description: Streamline the contract negotiation process by comparing two contract revisions to quickly identify and review all changes between the two versions, thereby reducing manual effort and minimizing the risk of missing critical updates.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
keywords: [Compare contract documents, Compare contract revisions]
breadcrumb: [Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Compare contract revisions in Contract Management Pro

Streamline the contract negotiation process by comparing two contract revisions to quickly identify and review all changes between the two versions, thereby reducing manual effort and minimizing the risk of missing critical updates.

## Before you begin

The contract documents must be stored internally in the ServiceNow instance.

Role required: sn\_cm\_core.contract\_user

## About this task

During contract negotiations, different parties update a contract and share contract revisions. As a contract fulfiller, use the document comparison feature in Contract Management Pro to easily compare two versions of a contract document.

## Procedure

1.  Open a contract request from the workspace you are using.

<table id="table_ujj_bct_fgc"><thead><tr><th>

Method

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Contract Workspace

</td><td>

-   Navigate to **All** &gt; **Contract Workspace**.
-   Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
-   Select **Contract requests** &gt; **All**
-   Select a contract request.


</td></tr><tr><td>

Workspace used by your application

</td><td>

-   Navigate to your workspace.
-   Open the list that displays the contract requests.
-   Select a contract request.


</td></tr></tbody>
</table>2.  In the **Contract documents** tab, select **Compare documents**.

3.  In the Compare documents window, select the contract type and documents you want to compare.

    **Note:** You can only compare files in .doc and .docx format.

    1.  In the **Contract type** field, select the contract type.

        For single contract type contract requests, this field is automatically updated.

    2.  In the **Select document 1** field, select a lower version of the contract document you want to compare.

        Document revisions are listed in ascending order, with older versions appearing above newer ones.

    3.  In the **Select document 2** field, select a higher version of the contract document.

        Document revisions are listed in descending order, with the latest version at the top.

    4.  Select **Compare**.

    The contract document opens on a different tab displaying the comparison summary with total changes, added, deleted, and format changes.

    The deletions are highlighted with red strikeout, additions are highlighted in green, and formatting changes are highlighted in cyan.

4.  Select **Hide redlines** to hide the highlighted changes.

5.  Select **Download redlined document** to download the document, and make further modifications to it.


**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)

