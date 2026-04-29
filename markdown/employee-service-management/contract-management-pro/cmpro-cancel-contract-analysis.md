---
title: Cancel a Now Assist contract analysis
description: Cancel a Now Assist contract analysis when it’s no longer required due to a change in business requirements.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract analysis, Use generative AI skills, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Cancel a Now Assist contract analysis

Cancel a Now Assist contract analysis when it’s no longer required due to a change in business requirements.

## Before you begin

You must have started the contract analysis with Now Assist. For more information, see [Analyze a contract document](cmpro-analyze-contract-doc.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_lg\_cnt.contract\_fulfiller

## About this task

You can cancel an analysis for a contract document or for all contract documents by canceling the contract request.

## Procedure

1.  Open the contract request from the workspace that you’re using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d165702e88">

Method

</th><th align="left" id="d165702e91">

Steps

</th></tr></thead><tbody><tr><td id="d165702e97">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Contract requests** &gt; **All**.
4.  Select a contract request.


</td></tr><tr><td id="d165702e145">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  Cancel the contract analysis for a contract document or all documents in a contract request.

<table id="choicetable_hwf_1sy_ddc"><thead><tr><th align="left" id="d165702e175">

Method

</th><th align="left" id="d165702e178">

Steps

</th></tr></thead><tbody><tr><td id="d165702e184">

**Cancel contract analysis for a document**

</td><td>

1.  Select the **Contract documents** tab.
2.  On the document card in the Now Assist contextual panel, select **Cancel**.
3.  Cancel the contract analysis by selecting **Yes, Cancel**.


</td></tr><tr><td id="d165702e214">

**Cancel contract analysis for all the documents in a contract request**

</td><td>

1.  Select the More Actions ![More actions icon](../../workplace-central/images/more-actions-move-schedule.png) icon.
2.  Select **Cancel request**
3.  Confirm the cancellation by selecting **Cancel Request**.


</td></tr></tbody>
</table>
## Result

The contract analysis is canceled.

-   If a contract analysis for a specific contract document was canceled, the Now Assist analysis status for the document version is updated to Canceled.
-   If a contract analysis for all the contract documents under analysis is canceled, the Now Assist analysis status is updated to Canceled for any pending analysis. For contract documents that are already analyzed, the status remains as Completed.
-   The contract request state is Work in progress.
-   A cancellation email notification is sent to the contract fulfiller, group manager, and collaborator.

**Parent Topic:**[Contract analysis using Now Assist in Contract Management](../concept/cncore-NA-review-land.md)

