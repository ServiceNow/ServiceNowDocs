---
title: Cancel AI contract analysis
description: Cancel a AI contract analysis when it’s no longer required due to a change in business requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cmpro-cancel-contract-analysis.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract analysis, Use AI skills, Now Assist in Contract Management, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Cancel AI contract analysis

Cancel a AI contract analysis when it’s no longer required due to a change in business requirements.

## Before you begin

You must have initiated the AI contract analysis. For more information, see [Analyze a contract document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-analyze-contract-doc.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_lg\_cnt.contract\_fulfiller

## About this task

You can cancel an analysis for a contract document or for all contract documents by canceling the contract request.

## Procedure

1.  Open the contract request from the workspace that you’re using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d172543e79">

Method

</th><th align="left" id="d172543e82">

Steps

</th></tr></thead><tbody><tr><td id="d172543e88">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Contract requests** &gt; **All**.
4.  Select a contract request.


</td></tr><tr><td id="d172543e136">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  Cancel the contract analysis for a contract document or all documents in a contract request.

<table id="choicetable_hwf_1sy_ddc"><thead><tr><th align="left" id="d172543e166">

Method

</th><th align="left" id="d172543e169">

Steps

</th></tr></thead><tbody><tr><td id="d172543e175">

**Cancel contract analysis for a document**

</td><td>

1.  Select the **Contract documents** tab.
2.  On the document card in the ServiceNow Otto contextual panel, select **Cancel**.
3.  Cancel the contract analysis by selecting **Yes, Cancel**.


</td></tr><tr><td id="d172543e208">

**Cancel contract analysis for all the documents in a contract request**

</td><td>

1.  Select the More Actions \[Omitted image "more-actions-move-schedule.png"\] Alt text: More actions icon icon.
2.  Select **Cancel request**
3.  Confirm the cancellation by selecting **Cancel Request**.


</td></tr></tbody>
</table>
## Result

The contract analysis is canceled.

-   If a contract analysis for a specific contract document was canceled, the AI analysis status for the document version is updated to Canceled.
-   If a contract analysis for all the contract documents under analysis is canceled, the AI analysis status is updated to Canceled for any pending analysis. For contract documents that are already analyzed, the status remains as Completed.
-   The contract request state is Work in progress.
-   A cancellation email notification is sent to the contract fulfiller, group manager, and collaborator.

**Parent Topic:**[Contract analysis using Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-NA-review-land.md)

