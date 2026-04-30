---
title: Microsoft Exchange Online - Calendar synchronization
description: Synchronize reservations between Microsoft Exchange Online and Workplace Reservation Management.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Microsoft Exchange Online - Calendar synchronization

Synchronize reservations between Microsoft Exchange Online and Workplace Reservation Management.

The Workplace Calendar Synchronization application provides a medium to establish a connection between your Microsoft Exchange Online Outlook calendar and the Workplace Reservation Management application. You can synchronize reservations made in the Reservation portal to the Microsoft Outlook calendar and block the date and time. Similarly, you can also synchronize the events made in the Microsoft Outlook calendar with the Workplace Reservation Management application and track the reservations and its details.

## Microsoft Graph API

The Microsoft Graph API provides access to data stored across Microsoft 365 services. So, to synchronize reservations, the Microsoft Graph connection plays a crucial role. When you install Microsoft Exchange Online Spoke, the following credentials are installed:

-   **MS Graph 1**
-   **MS Graph 2**

To install the Microsoft Exchange Online Spoke, refer to [Create a connection with Microsoft Exchange Online spoke](../task/create-connection-with-msspoke.md).

## Subscriptions

When you activate a reservable sync configuration to synchronize reservations with Microsoft Exchange Online, a subscription is created automatically. The application notifies if a subscription renewal fails. The notification is sent to the users with the Workplace Calendar Synchronization admin \[sn\_wsd\_rsvsync.admin\] role. Subscriptions are created only for active reservable sync configurations. A subscription notifies you about the changes to events on the room mailbox. For more information about subscriptions, refer to [https://learn.microsoft.com/en-us/graph/api/subscription-post-subscriptions?view=graph-rest-1.0&amp;tabs=http](https://learn.microsoft.com/en-us/graph/api/subscription-post-subscriptions?view=graph-rest-1.0&tabs=http).

A webhook registry contains the subscription-related details to perform a call-back. To configure a webhook registry, refer to [Configure the webhook registry of Microsoft Exchange Online spoke](../task/configure-webhook-registry-for-msex.md).

## Synchronization from Workplace Service Delivery to Microsoft Exchange Online

To synchronize reservations made using the Workplace Reservation Management application to the Microsoft Exchange Online Microsoft Outlook calendar, you must first create a connection with Microsoft Exchange Online. Depending on how you want to establish the connections, refer to the respective topics:

**Note:** By default, Microsoft Exchange Online Spoke provides you with the MS Graph 1 and MS Graph two credentials. If you do not want to use the default connection and credential alias provided by the application, you can create your own alias.

-   To configure a normal mode connection with Microsoft Exchange Online, refer to [Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md).
-   To configure a strict mode connection with Microsoft Exchange Online, refer to [Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md).

## Synchronization from Microsoft Exchange Online to Workplace Reservation Management

The process of synchronizing reservations made in an Microsoft Outlook calendar to the Workplace Reservation Management is performed with the help of subscriptions. A subscription is created in the calendar provider for the room \(reservable sync record\). The application is notified by the subscription whenever an action is performed on the room. For more information about subscriptions, refer to [https://learn.microsoft.com/en-us/graph/api/subscription-post-subscriptions?view=graph-rest-1.0&amp;tabs=http](https://learn.microsoft.com/en-us/graph/api/subscription-post-subscriptions?view=graph-rest-1.0&tabs=http).

## Strict mode

The Workplace Calendar Synchronization application enables you to configure your connections and configurations with Microsoft Exchange Online in strict mode as well. In strict mode, events are not directly created in an employee's calendar, instead, they are sent to a general email address. Employees are invited to the event. You can specify a strict mode email id through which you want to sync reservations. Employees can only make changes using the Workplace Reservation Management application.

To configure strict mode, enable the **Strict mode** option while configuring the Microsoft Exchange Online as calendar provider. The requesters are considered as invitees.

## Personal authentication mode

The Workplace Calendar Synchronization application enables you to configure your connections and configurations with Microsoft Exchange Online in personal authentication mode to synchronize reservations and to restrict unauthorized access to resource calendars. In personal authentication mode, a user level authentication token is generated that enables the user to create, update, or cancel reservation to synchronize events on user outlook calendar. You need to specify a strict mode email id through which you want to sync reservations. Employees can only make changes in the Workplace Reservation Management application using the generated token.

To configure personal authentication mode, enable the Personal mode option while configuring the Microsoft Exchange Online as calendar provider.

## Sync past reservations

The Workplace Calendar Synchronization application enables you to sync reservations that were made in the past. You can specify the duration in date and time to get those past reservations to sync with Microsoft Exchange Online or Workplace Reservation Management. You can configure the setting using the **Synchronize past reservations**. Specify the **Sync start date time** manually from the subscription record of the reservable sync record for which you are synchronizing the past reservations. In the **Sync end date time**, you can specify the end time as you want.

## Multi-provider setup

The Workplace Calendar Synchronization enables you to configure a multi-provider setup with Microsoft Exchange Online. That is, configure multiple connections and credentials with Microsoft Exchange Online. For more information on how to set up a multiprovider, refer to [Create single or multiple calendar providers with Microsoft Exchange Online](../task/create-multiple-connection-same-provider.md).

**Important:** Multi-provider is not supported or is not the same as Exchange hybrid configurations.

## 'No request' handling

No request is a mechanism to validate the generated syntax of a payload of an event created for the calendar. But, instead of sending the event to the calendar provider, it is only created. The admin can validate the payload content of the event \(JSON\) to ensure that is generated as expected. 'No request' ensures that the application does not make any API calls to the calendar provider when you create, update, or cancel a reservation in the Workplace Reservation Management application.

## Run instance scan

Execute an Instance scan on your Workplace Calendar Synchronization configurations with Microsoft Exchange Online. The Instance Scan application diagnoses the configurations with the calendar provider by running a series of checks using suites.

Refer to [Run Instance scan to check Microsoft Exchange Online synchronization configuration](../task/run-instance-scan-on-your-workplace-cal-sync-configs.md).

