---
title: Cancel AI contract analysis
description: Cancel a AI contract analysis when it’s no longer required due to a change in business requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-cancel-contract-analysis.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract analysis, Use AI skills, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Cancel AI contract analysis

Cancel a AI contract analysis when it’s no longer required due to a change in business requirements.

## Before you begin

You must have initiated the AI contract analysis. For more information, see [Analyze a contract document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-analyze-contract-doc.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_lg\_cnt.contract\_fulfiller

## About this task

You can cancel an analysis for a contract document or for all contract documents by canceling the contract request.

## Procedure

1.  Open the contract request from the workspace that you’re using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d173480e76">

Method

</th><th align="left" id="d173480e79">

Steps

</th></tr></thead><tbody><tr><td id="d173480e85">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Contract requests** &gt; **All**.
4.  Select a contract request.


</td></tr><tr><td id="d173480e133">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  Cancel the contract analysis for a contract document or all documents in a contract request.

<table id="choicetable_hwf_1sy_ddc"><thead><tr><th align="left" id="d173480e163">

Method

</th><th align="left" id="d173480e166">

Steps

</th></tr></thead><tbody><tr><td id="d173480e172">

**Cancel contract analysis for a document**

</td><td>

1.  Select the **Contract documents** tab.
2.  On the document card in the ServiceNow Otto contextual panel, select **Cancel**.
3.  Cancel the contract analysis by selecting **Yes, Cancel**.


</td></tr><tr><td id="d173480e205">

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

**Parent Topic:**[Contract analysis using ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-NA-review-land.md)

