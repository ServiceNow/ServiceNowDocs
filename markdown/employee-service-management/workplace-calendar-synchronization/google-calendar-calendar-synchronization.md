---
title: Google Calendar - Calendar synchronization
description: Create a connection with Google Calendar and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the Google Calendar and vice versa.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Google Calendar - Calendar synchronization

Create a connection with Google Calendar and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the Google Calendar and vice versa.

The reservation synchronization from a Google Calendar to the Workplace Reservation Management is performed using various approaches like events, and occurrences.

**Important:** The application does not support a strict mode configuration for Google Calendar.

## Synchronization from Workplace Reservation Management to Google Calendar

The synchronization process from Workplace Reservation Management to Google is performed using the Google Calendar spoke. You can configure a connection with Google using the Flow designer.

The synchronization process includes the following steps:

1.  Install [Google Calendar Spoke](https://www.servicenow.com/docs/access?context=gcal-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
2.  [Set up Google Calendar spoke](https://www.servicenow.com/docs/access?context=setup-gcal&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
3.  Authenticate ServiceNow with Google. Refer to [Authenticate Google for calendar synchronization](../task/authenticate-google-for-calendar-sync.md).
4.  Configuring the Google Calendar Spoke connection using the Flow designer. Refer to [Create a Connection and credential record for Google](../task/create-connection-configuration-with-google.md).
5.  Creating the Google Calendar provider. Refer to [Configure Google as calendar provider](../task/configure-google-as-calendar-provider.md).

The application also enables you to create your own connection and credential alias instead of using the default alias created by using the flow designer. Refer to [Configure your own Google connection and credential alias](../concept/configure-your-own-google-connection-and-credential-alias.md).

## Synchronization from Google Calendar to Workplace Reservation Management

The reservation synchronization from the Google Calendar to Reservation portal is done by pulling the latest calendar updates in Google Calendar by using a scheduled job, **WSDRS Sync Calendar items**. All the events related to the sync-enabled rooms are read and updated in the Workplace Reservation Management application. The application creates Create, Update, Delete, and Read events in the **Events** table.

The scheduled job, **WSDRS Sync Calendar items**, is provided with the application to get the latest changes for all the active reservable sync configurations. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. By default, the scheduled job is set to run for every five minutes. However, you can set the scheduled job time as you want. At any time, you can also manually execute it.

An approach called, Delta synchronization is used by the Workplace Calendar Synchronization application. With Delta synchronization, you retrieve only the incremental changes made on a resource email id of the calendar using a reference point called as synchronization token. That is, for each room \(each reservable sync record\), linked to the on-premises calendar provider you get the synchronization tokens, which are the reference points to get the update from the calendar in increments.

-   Based on the **Page size**, **Sync batch size** and the **Sync batch interval**, the information is retrieved by the synchronization tokens. For example, if you specified the values as **5**, **500**, and **60** respectively \(in the previous fields\). It means that you can raise 500 requests in an interval of 60 seconds. The synchronization results five changes in a page.
-   When you create a reservable sync configuration record under the Google calendar, you must ensure that it is activated.
-   When the sync record is activated, a flow is triggered and a synchronization token for that reservable synchronization record is created in the **Sync Deltas** module.
-   The scheduled job, **WSDRS Sync Calendar items**, is provided with the application to get the latest changes for all the active reservable sync configurations. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. By default, the scheduled job is set to run for every five minutes. However, you can set the scheduled job time as you want. At any time, you can also manually execute it.
-   The changes made on the reservable sync configurations are created as events in the **Events** module. The application creates Create, Update, Delete, and Read, events for the Google Calendar.
-   For each sync record, an event is created. Depending on the page size specified on the calendar provider, the changes are displayed. If there are any pending changes, it is displayed during the next scheduled job run.
-   The API that is used to get the synchronization tokens, saves the response in the **Response** field of the event. The API provides changes made on a single reservation, multi-reservation, and the parent recurring reservation.
-   Using the response created by the API, a reservation is created in the Workplace Reservation Management application.
-   With every scheduled job run, the synchronization token is also updated which is used as the reference point for the next synchronization.

## Synchronizing past reservations

he Workplace Calendar Synchronization enables you to also synchronize reservations made in the past. You can specify the date and time range in the **Sync start date time** and **Sync end date time** fields. For the on-premises calendar, the following conditions must be met to sync past reservations:

-   The calendar provider that is the Google Calendar calendar provider that you configured must be active.
-   The **Synchronize past reservations** field must be selected.
-   The reservable sync configuration for which you want to sync past reservations must be active.

    **Note:** After you enable the **Synchronize past reservations**, you must navigate to the locations of each reservable sync configuration record and select **Sync Location**.


## 'No request' handling

No request is a mechanism to validate the generated syntax of the payload of an event created for the calendar. But, instead of sending the event to the calendar provider, it is only created. The admin can validate the payload content of the event \(JSON\) to ensure that is generated as expected. 'No request' ensures that the application does not make any API calls to the calendar provider when you create, update, or cancel a reservation in the Workplace Reservation Management application.

