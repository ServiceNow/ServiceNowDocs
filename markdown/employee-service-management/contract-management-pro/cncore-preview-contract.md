---
title: Preview and download a signed contract document
description: View and download a signed contract document.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Preview and download a signed contract document

View and download a signed contract document.

## Before you begin

**Important:** Cancelling a contract request after it has been sent for signature stops the process in its current state.

Role required: sn\_cm\_core.contract\_user

## About this task

When all signatories have signed a contract document, it’s considered as the final contract document and is stored in the Contract Request Repositories \[sn\_cm\_core\_contract\_request\_m2m\_contract\_repository\] table.

Access to a contract document is based on the following user roles and conditions:

-   Group manager, Assigned to user and collaborator have edit access to the contract repository.
-   Contract fulfiller belonging to the same assignment group has view access to the contract repository.
-   Contract fulfiller not in assignment group do not have any access to the to the contract repository.
-   Only a contracts administrator can delete contract documents.
-   Requesters can view only the contract documents for which they submitted the contract request.
-   Users can view only contract documents for which they have been added to the watch list of the corresponding contract requests.

When multiple contract documents are attached, a separate contract repository record is created for each contract type.

## Procedure

1.  Navigate to your workspace.

2.  Select a contract request.

3.  Navigate to **Contract repository**.

4.  Select the contract number.

5.  Navigate to **Contract documents** tab.

6.  View the contract document.

<table id="choicetable_vxh_nwf_t1c"><thead><tr><th align="left" id="d760233e125">

Choice

</th><th align="left" id="d760233e128">

Steps

</th></tr></thead><tbody><tr><td id="d760233e134">

**When internal storage is configured**

</td><td>

1.  Select the revision number.
2.  From the Attachments pane select the document to view it.
3.  Select download icon to download the document.


</td></tr><tr><td id="d760233e155">

**When external storage is configured**

</td><td>

1.  Select the URL. The document will open from the external storage.
2.  Select download icon to download the document.


</td></tr></tbody>
</table>
**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)

