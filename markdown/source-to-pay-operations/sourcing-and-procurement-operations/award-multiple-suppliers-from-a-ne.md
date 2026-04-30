---
title: Award multiple suppliers from a negotiation event
description: When negotiations are complete for a negotiation event, you can award one or multiple suppliers from the negotiation event, or reject all bids, as required. Awarding suppliers create purchase requisitions for the selected suppliers and items.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Source-to-Pay Workspace, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Award multiple suppliers from a negotiation event

When negotiations are complete for a negotiation event, you can award one or multiple suppliers from the negotiation event, or reject all bids, as required. Awarding suppliers create purchase requisitions for the selected suppliers and items.

## Before you begin

Ensure that you’ve qualified all the relevant suppliers, and have received all the bids and responses from them, before you begin the awarding process. At this point, the negotiation event that you plan to work on, and all its associated negotiations, sourcing requests, and purchase lines must be in the Requires Decision state.

Role required: sn\_shop.procurement\_specialist

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  On the list page, navigate to **All work** &gt; **Negotiation Events**.

3.  Select and open the negotiation event that you plan to work on.

    The **Details** page is displayed with a list of all the negotiations, suppliers, state, and negotiation outcome.

4.  From the **Award single supplier** list, select **Award multiple suppliers**.

    The **Award suppliers** tab is displayed with all the supplier bids and responses grouped by products, with details of the requester’s intake.

5.  Do one of the following.

    -   Select **Review selection** without making any selection for any product. A dialog box is displayed with a message alerting you that you haven't made any selection. Selecting **Continue** rejects all the bids.
    -   Select **Review selection** without making at least one selection for all the products. A dialog box is displayed with a message alerting you that you haven't made a selection for all the products. Selecting **Continue** awards the selected suppliers and rejects all the unselected bids.
    -   Select **None, reject bids** for all the products, and then select **Review selection**. The **Reject all bids?** dialog box is displayed where you must enter your reason for rejection. Selecting **Reject all bids** rejects all the bids.
    -   Select at least one supplier for all the products, except one whose bids you reject, and then select **Review selection**. The **Here's what you selected** dialog box is displayed with a summary of your selection. Selecting **Submit** awards the selected suppliers and rejects all the unselected bids.
    **Note:** The negotiation event is moved to Closed Complete, with the individual negotiations under it moved to Closed Decided or Closed Rejected based on your selection. The awarded sourcing requests are moved to Closed Complete, with purchase requisitions automatically created for the purchase lines. All the other sourcing requests are moved to the Closed Rejected state.


**Parent Topic:**[Source-to-Pay Workspace](../concept/procurement-specialist-workspace.md)

