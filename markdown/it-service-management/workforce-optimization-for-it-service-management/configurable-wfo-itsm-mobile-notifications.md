---
title: Notifications in ITSM Mobile Agent for Workforce Optimization for ITSM
description: Receive notifications when you manage shift-swap and time-off requests. Enable notifications for the actions that are most relevant to you. For example, get notified when you receive a request for approval from an agent who wants to swap shifts with a peer.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Requesting time-off using the ITSM Mobile Agent, Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Notifications in ITSM Mobile Agent for Workforce Optimization for ITSM

Receive notifications when you manage shift-swap and time-off requests. Enable notifications for the actions that are most relevant to you. For example, get notified when you receive a request for approval from an agent who wants to swap shifts with a peer.

As a Workforce Optimization for ITSM agent \(sn\_shift\_planning.agent\) and a Workforce Optimization for ITSM manager \(sn\_wfo\_cfg\_ws.manager\), you can enable or disable notifications for shift-swap and time-off requests and approvals. Agents can request a shift-swap with their peers and get approval from their manager. They can also request approval for time-off from their managers.

You must set your notification preferences in your desktop application to receive the notifications in your ITSM Mobile Agent application.

To enable the notifications:

1.  On your desktop application instance, click the gear icon ![Gear icon](../image/gear-icon.png) in the top-right corner. The **System Settings** screen appears.
2.  Click **Notifications**.
3.  Enable **Allow Notifications**.
4.  In the **Notifications Category** section, click **Mobile - Shift Planning**.
5.  Enable the desired notification.

<table id="table_omz_rqm_h4b"><thead><tr><th>

When you enable this notification

</th><th>

You receive a notification when your

</th></tr></thead><tbody><tr><td>

Shift-swap approval request

</td><td>

-   Agents send shift-swap requests to approve.
-   Your peer sends a shift-swap request to approve.

</td></tr><tr><td>

Shift-swap approved by manager

</td><td>

Manager approves your request to swap shifts with your peer.

</td></tr><tr><td>

Shift-swap approved by peer

</td><td>

Peer approves your request to swap shifts with them.

</td></tr><tr><td>

Shift-swap rejected by manager

</td><td>

Manager rejects your request to swap shifts with your peer.

</td></tr><tr><td>

Shift-swap rejected by peer

</td><td>

Peer rejects your request to swap shifts with them.

</td></tr><tr><td>

Time-off approval request

</td><td>

Agents send requests to approve time off.

</td></tr><tr><td>

Time off approved

</td><td>

Manager approves your time-off request.

</td></tr><tr><td>

Time off rejected

</td><td>

Manager rejects your time-off request.

</td></tr></tbody>
</table>**Parent Topic:**[Requesting time-off using the ITSM Mobile Agent for Workforce Optimization for ITSM](../concept/configurable-agent-schedule-mobile-wfo-itsm.md)

**Related topics**  


[Setting notification preferences in Core UI](https://www.servicenow.com/docs/access?context=user-notification-preferences&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

