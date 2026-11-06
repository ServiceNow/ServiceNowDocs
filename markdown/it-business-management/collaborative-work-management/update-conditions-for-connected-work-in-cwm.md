---
title: Update filter conditions for connected work in CWM
description: Update the filter conditions for connected work item types in Collaborative Work Management Boards so that the work items displayed in the Board reflect your team's current workload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/collaborative-work-management/update-conditions-for-connected-work-in-cwm.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Connect work, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Update filter conditions for connected work in CWM

Update the filter conditions for connected work item types in Collaborative Work Management Boards so that the work items displayed in the Board reflect your team's current workload.

## Before you begin

Role required: sn\_cwm.cwm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select the Board that you want to manage the connected work item types for.

3.  From the Board header, select **Connected work**.

    \[Omitted image "cwm-connected-work-header.png"\] Alt text: Connect work option in the CWM Board header.

4.  From the More actions menu \(\[Omitted image "cwm-icon-page-actions.png"\] Alt text: More actions icon.\) of a connected work item type, select **Edit**.

    \[Omitted image "cwm-connected-work-more-options.png"\] Alt text: Choose to edit a connected work item type configuration for a CWM Board.

5.  Use the condition builder to edit the defined conditions.

6.  Select the Update count icon \(\[Omitted image "cwm-icon-update-count.png"\] Alt text: Update count icon.\) to check the number of records that exist which match the filter criteria that you updated.

    **Note:**

    The matching record count includes every item that meets your import conditions, but the board might display fewer items. Items can be hidden by ACLs or by board preferences. By default, a board shows only items that were updated in the last 90 days, and it can also hide completed items. To see items that match your conditions but aren't displayed, update the board preferences.

    \[Omitted image "cwm-connected-work-define.png"\] Alt text: Define conditions to connect records from other ServiceNow applications.

7.  Select **Save**.

8.  Repeat steps 4 through 7 to update conditions of any other connected work item type.

9.  After all required changes are made, select **Save** in the Manage connected work modal.


## Result

The Board is refreshed to load the work items based on your changes.

Items that no longer meet the conditions aren't removed from the Board automatically. You can remove them manually or remove the item type from connected work and re-add it with the updated condition.

**Parent Topic:**[Connected work in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/collaborative-work-management/unified-boards-for-connected-work-in-cwm.md)

