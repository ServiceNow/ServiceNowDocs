---
title: Purchase state indicators
description: Your purchases, which include purchase requisitions, purchase requisition lines, purchase orders, purchase order lines, and sourcing requests, are highlighted with color coding to help you quickly understand their state and due date. The progress bar on these purchases follows a similar color coding.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [purchase states, purchase state indicators, purchase state tracking, track purchase states]
breadcrumb: [Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase state indicators

Your purchases, which include purchase requisitions, purchase requisition lines, purchase orders, purchase order lines, and sourcing requests, are highlighted with color coding to help you quickly understand their state and due date. The progress bar on these purchases follows a similar color coding.

A red state badge is displayed if a purchase is closed canceled or closed rejected.![Red state badge for rejected purchase.](../image/my-purchases-rejected.png)

A yellow state badge indicates that a purchase requires decision or needs information.

For all other states, a grey badge is displayed.

A red due date badge is displayed for a purchase if:

-   Any of the purchasing tasks associated with the purchase requisition line or purchase order line are overdue.
-   Any of the milestones associated with the purchase order line are overdue.
-   Any of the receipt tasks associated to the parent purchase order are overdue.

Similarly, a yellow due date badge is displayed for a purchase if any of the above conditions have a due date approaching in three days. A green due date badge indicates that everything is on schedule.

A procurement administrator can use the sn\_shop.spend.sla.due.days purchasing property to configure the number of days for displaying the yellow highlight. By default, this is set to three days of the task due date.

**Note:** The total line amount that you see for each purchase includes the updated shipping and tax estimates.

Your purchases are also highlighted with colored information banners when approvers request for clarification, or reject your purchase requisitions, purchase orders, or sourcing requests, in whole or in part. The reason for rejection is also displayed.

**Parent Topic:**[My purchases on Shopping Hub](my-purchases.md)

