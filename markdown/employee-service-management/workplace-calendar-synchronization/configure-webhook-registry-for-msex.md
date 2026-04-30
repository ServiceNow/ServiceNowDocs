---
title: Configure the webhook registry of Microsoft Exchange Online spoke
description: Configure callback URL for communication between the Workplace Calendar Synchronization application and Microsoft Exchange Online calendar.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure the webhook registry of Microsoft Exchange Online spoke

Configure callback URL for communication between the Workplace Calendar Synchronization application and Microsoft Exchange Online calendar.

## Before you begin

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Microsoft Exchange Online Spoke** &gt; **Webhook Registry**.

2.  Select the **WSDRS Event Subscription** registry.

    The webhook registry is provided by default with the application.

3.  On the form, select **Callback URL**.

    The **Client State** and **Callback URL** is automatically generated.

4.  Select **Update**.


**Parent Topic:**[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

**Related topics**  


[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

[Create single or multiple calendar providers with Microsoft Exchange Online](create-multiple-connection-same-provider.md)

[Approve a reservation](approve-or-reject-reservation.md)

[Reservation approvals in Microsoft Exchange Online](../concept/handle-reservation-approvals-in-msex.md)

