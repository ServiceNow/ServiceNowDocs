---
title: Microsoft Exchange On-Premises - Calendar synchronization
description: Create a connection with Microsoft Exchange On-Premises and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the On-Premises calendar and vice versa. The reservation synchronization from an On-Premises calendar to the Workplace Reservation Management is performed using various approaches like subscriptions, synchronization tokens, events, and occurrences.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Microsoft Exchange On-Premises - Calendar synchronization

Create a connection with Microsoft Exchange On-Premises and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the On-Premises calendar and vice versa. The reservation synchronization from an On-Premises calendar to the Workplace Reservation Management is performed using various approaches like subscriptions, synchronization tokens, events, and occurrences.

The Microsoft Exchange On-Premises, unlike other calendar providers, isn’t accessible online. The provider is remote and is accessible only by the organization locally. To synchronize calendar reservations with this on-premise setup, the Workplace Calendar Synchronization application enables you to communicate using the MID server. A MID server is installed in the same local setup where the Microsoft Exchange On-Premises is installed. This way, a communication can be established with the MID server and communicate frequently. To support the on-premises calendar provider, a new calendar processor, Microsoft EWS is supported in the Workplace Calendar Synchronization application.

1.  Connect MID server with ServiceNow®.
2.  Create a connection and credential alias.

**Important:** The Workplace Reservations for Microsoft Outlook Add-in application does not support Microsoft Exchange On-Premises.

## Synchronization from Workplace Reservation Management to Microsoft Exchange On-Premises

Synchronize reservations to the on-premises calendar from Workplace Reservation Management by communicating using the MID server.

-   Install [Microsoft Exchange Server Spoke](https://www.servicenow.com/docs/access?context=msexchangeserver-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
-   [Set up the Microsoft Exchange Server spoke](https://www.servicenow.com/docs/access?context=setup-msexchange&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   [Connect Microsoft Exchange On-Premises MID server with ServiceNow](../task/connect-on-premise-mid-server-with-servicenow.md)
-   After configuring the MID server, create a connection and credential alias to connect it with the calendar provider. For more information, refer to [Create a Connection and credential alias for Microsoft Exchange On-Premises](../task/create-a-connection-and-credential-alias-for-ms-exch-onprem.md).
-   After setting up the connection and credential aliases, configure Microsoft Exchange On-Premises as a calendar provider. For more information, refer to [Configure Microsoft Exchange On-Premises as calendar provider](../task/configure-ms-exchange-on-prem-as-calendar-provider.md). To support the on-premises calendar provider, a new calendar processor, Microsoft EWS is added.

## Synchronization from Microsoft Exchange On-Premises calendar to Workplace Reservation Management

The reservation synchronization from the Microsoft Exchange On-Premises calendar to the Reservation portal is done by running a timely scheduled job, **WSDRS Sync Calendar items**.

An approach called, Delta synchronization is used by the Workplace Calendar Synchronization application. With Delta synchronization, you retrieve only the incremental changes made on a resource email id of the calendar using a reference point called as synchronization token. That is, for each room \(each reservable sync record\), linked to the on-premises calendar provider you get the synchronization tokens, which are the reference points to get the update from the calendar in increments.

-   Based on the **Page size**, **Sync batch size** and the **Sync batch interval**, the information is retrieved by the synchronization tokens. For example, if you specified the values as **5**, **500**, and **60** respectively \(in the previous fields\). It means that you can raise 500 requests in an interval of 60 seconds. The synchronization results five changes in a page.
-   When you create a reservable sync configuration record under the on-premises calendar, you must ensure that is activated.
-   When the sync record is activated, a flow is triggered and a synchronization token for that reservable synchronization record is created in the **Sync Deltas** module.
-   The scheduled job, **WSDRS Sync Calendar items**, is provided with the application to get the latest changes for all the active reservable sync configurations. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. By default, the scheduled job is set to run for every five minutes. However, you can set the scheduled job time as you want. At any time, you can also manually execute it.
-   The changes made on the reservable sync configurations are created as events in the **Events** module. The application creates Create, Update, Delete, Read, and Retrieve attendees events for Microsoft Exchange On-Premises calendar.
-   For each sync record, an event is created. Depending on the page size specified on the calendar provider, the changes are displayed. If there are any pending changes, it is displayed during the next scheduled job run.
-   The API that is used to get the synchronization tokens, saves the response in the **Response** field of the event. The API provides changes made on a single reservation, multi-reservation, and the parent recurring reservation.
-   Using the response created by the API, a reservation is created in the Workplace Reservation Management application.
-   With every scheduled job run, the synchronization token is also updated which is used as the reference point for the next synchronization.

## Strict mode

The Workplace Calendar Synchronization application enables you to configure your connections and configurations with Microsoft Exchange On-Premises in strict mode as well. In strict mode, events are not directly created in an employee's calendar, instead, they are sent to a general email address. Employees are invited to the event. You can specify a strict mode email id through which you want to sync reservations. Employees can only make changes using the Workplace Reservation Management application.

To enable strict mode, you can enable the **Strict mode** option in the while configuring the on-premises calendar provide. The requesters are considered as invitees.

## Synchronizing past reservations

The Workplace Calendar Synchronization enables you to also synchronize reservations made in the past. You can specify the date and time range in the **Sync start date time** and **Sync end date time** fields. For the on-premises calendar, the following conditions must be met to sync past reservations:

-   The calendar provider that is the Microsoft Exchange On-Premises calendar provider that you configured must be active.
-   The **Synchronize past reservations** field must be selected.
-   The reservable sync configuration for which you want to sync past reservations must be active.

**Note:** Ensure that the reservations that you want to sync from the past are not above 1000. If in cases the expected number of past events are more than 1000, it is recommended to modify the system property **sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths**. Specify the value in months keeping in mind the expected past reservations. A single sync syncs reservations from those many months. Ensure that the specified number of months do not have more than 1000 reservations per room/resource.

## 'No request' handling

No request is a mechanism to validate the generated syntax of the payload of an event created for the calendar. But, instead of sending the event to the calendar provider, it is only created. The admin can validate the payload content of the event \(JSON\) to ensure that is generated as expected. 'No request' ensures that the application does not make any API calls to the calendar provider when you create, update, or cancel a reservation in the Workplace Reservation Management application.

