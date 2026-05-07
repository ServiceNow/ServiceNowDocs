---
title: Work on a sourcing event
description: You can work on a sourcing event and complete an entire workflow, right from starting negotiations with multiple suppliers, to awarding one or multiple suppliers, or rejecting bids. Awarding suppliers create purchase requisitions for the selected suppliers and items.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Procurement Case Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Work on a sourcing event

You can work on a sourcing event and complete an entire workflow, right from starting negotiations with multiple suppliers, to awarding one or multiple suppliers, or rejecting bids. Awarding suppliers create purchase requisitions for the selected suppliers and items.

## Before you begin

Ensure that you’ve qualified all the suppliers involved in the sourcing event before you start negotiating with them. You can add additional relevant sourcing requests and qualified suppliers to the ongoing sourcing event, as and when required, when working on the event. This allows you to manage complex negotiation activities. Adding a sourcing request or supplier auto-creates purchase lines and creates a new negotiation record to manage negotiation activities for that specific supplier.

Role required: sn\_shop.procurement\_specialist

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  On the list page, navigate to **Review needed** &gt; **Sourcing event: ready to negotiate**.

3.  Select and open the sourcing event that you plan to work on.

4.  Select **Start negotiating**.

    The sourcing event moves to the Work in Progress state.

5.  Select **Add sourcing requests** if you want to add more similar sourcing requests to this sourcing event.

6.  Select **Add suppliers** if you want to add more suppliers to this sourcing event.

7.  On the **Purchase Lines** tab, update the **Negotiated unit cost** field for each purchase line.

    This moves the purchase request lines to the Pricing Obtained state.

8.  On the **Negotiations** tab, select **Finish negotiating** for each negotiation.

    This moves the sourcing event and all its associated negotiations, sourcing requests, and purchase lines to the Requires Decision state.

9.  Do one of these actions.

<table id="choicetable_bhm_f5c_htb"><thead><tr><th align="left" id="d111942e162">

Action

</th><th align="left" id="d111942e165">

Description

</th></tr></thead><tbody><tr><td id="d111942e171">

**Save**

</td><td>

Saves the details of the sourcing event for further action.

</td></tr><tr><td id="d111942e180">

**Cancel**

</td><td>

Cancels the sourcing event and moves all its negotiations and associated sourcing requests and purchase lines to the Closed Cancelled state. This sourcing event is no longer considered for the awarding process.

</td></tr><tr><td id="d111942e189">

**Award single supplier**

</td><td>

Opens the **Select a supplier to award** dialog box, where you can select one of the suppliers from the list and select **OK** to award the supplier. The awarded negotiation moves to the Closed Decided state while all the others move to Closed Rejected. The purchase lines for the awarded negotiation are automatically converted to purchase requisitions.

</td></tr><tr><td id="d111942e204">

**Award multiple suppliers**

</td><td>

Opens the **Award suppliers** tab, where you can select one or more suppliers from the list and select **Review selection** to award the suppliers. The awarded negotiations move to the Closed Decided state while the others move to Closed Rejected. The purchase lines for the awarded negotiation are automatically converted to purchase requisitions.

 For information on more options that are available to you on this tab, see [Award multiple suppliers from a sourcing event](award-multiple-suppliers-from-a-ne.md).

</td></tr><tr><td id="d111942e233">

**Reject bids**

</td><td>

Opens the **Reject all bids?** dialog box, where you must enter your reason for rejection to reject all the bids. The sourcing event and all its negotiations and associated sourcing requests and purchase lines move to the Closed Rejected state.

</td></tr></tbody>
</table>10. Select **View purchase requisitions** from the sourcing event or the awarded negotiation to view the details of the newly created purchase requisitions.


**Parent Topic:**[Using Procurement Case Management](../concept/using-pcm.md)

