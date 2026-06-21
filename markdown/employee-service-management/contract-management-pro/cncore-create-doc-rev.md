---
title: Create a document revision
description: As a contract fulfiller, create a document revision to upload an updated version of the contract that contains the latest changes in the contract request, corrections, or suggestions from a third party.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-create-doc-rev.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a document revision

As a contract fulfiller, create a document revision to upload an updated version of the contract that contains the latest changes in the contract request, corrections, or suggestions from a third party.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

You can create document revisions only when the State is Work in progress.

**Note:** If the contract type is inactive, the **Create revision** button isn’t available for self-served contract requests.

## Procedure

1.  Open a contract request from the workspace you are using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d233286e62">

Method

</th><th align="left" id="d233286e65">

Steps

</th></tr></thead><tbody><tr><td id="d233286e71">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Contract requests** &gt; **All**
4.  Select a contract request.


</td></tr><tr><td id="d233286e118">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  In the **Contract Documents** tab, select **Create Revision**.

    \[Omitted image "cmpro-create-rev.png"\] Alt text: Create a contract revision in contract request

3.  In the **Create revision** window, upload the updated contract.

    \[Omitted image "cmpro-creare-rev-pop-up.png"\] Alt text: Attach document for contract revision

    1.  For non-self-served requests, select the contract type in the **Select contract type** field.

        Only active contract types are displayed in the list.

        **Note:** The field is available only for multiple contracts type contract requests.

    2.  In the **Create revision from** drop-down list, select the source of the updated contract and add the file.

        -   **Computer**

            Select this option to upload a file from your system. The field appear upon selecting this option. Select and upload the updated contract from your system.

        -   **Activity stream**

            Select this option to select a document from the activity stream. The **Document** field appears upon selecting this option. Select the document in the activity stream.

            The activity stream includes documents attached while requesting changes for a contract or documents received through email.

        -   **External storage**

            Select this option if external storage is enabled. The **Document** field appears upon selecting this option. Select the updated contract from external storage.

4.  Select **Create**.

    The document is added to the contract request. The revision number of the latest document is one higher than the previous document's revision number. The document revision is listed in the **Contract Documents** tab.

5.  Select **Save**.


**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-use-cmpro.md)

