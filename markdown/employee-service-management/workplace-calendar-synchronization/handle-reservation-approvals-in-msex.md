---
title: Reservation approvals in Microsoft Exchange Online
description: Track the approval status from Microsoft Outlook when a reservation request is either approved or rejected by the delegate.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2025-04-03"
reading_time_minutes: 1
breadcrumb: [Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Reservation approvals in Microsoft Exchange Online

Track the approval status from Microsoft Outlook when a reservation request is either approved or rejected by the delegate.

If you create a reservation in Workplace Service Delivery for a room with approvals enabled in Microsoft Outlook, the reservation status is initially set to Awaiting confirmation. When a callback is received from Microsoft Outlook, the reservation status updates to Awaiting approval. The reservation remains in this state until a delegate manually accepts or rejects the request.

-   If the approver accepts the request in Microsoft Outlook, the reservation status in **Workplace Reservations** \[sn\_wsd\_rsv\_reservation\] table changes to Confirmed.
-   If the approver declines the request, the reservation status in **Workplace Reservations** \[sn\_wsd\_rsv\_reservation\] table changes to Cancelled.

A new column **External Approval State** has been added to the **Workplace Reservations** \[sn\_wsd\_rsv\_reservation\] table to track the approval statues. This column retrieves data from Outlook callbacks and reflects the status of the approval request.

-   **Awaiting Approval** – Indicates that the request is pending action from the delegate
-   **Accepted** – Indicates that the request has been approved by the delegate
-   **Declined** – Indicates that the request has been rejected by the delegate
-   **Not Required** – Indicates that approvals aren’t required for this room in Outlook

**Note:** If a room has approvals enabled in both Workplace Service Delivery and Microsoft Outlook, the reservation status remains in Awaiting approval until it’s approved in both systems.

