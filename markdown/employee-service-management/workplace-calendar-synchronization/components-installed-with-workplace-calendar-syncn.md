---
title: Components installed with Workplace Calendar Synchronization
description: Several types of components are installed with the Workplace Calendar Synchronization application, including tables and user roles.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workplace Calendar Synchronization references, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Calendar Synchronization

Several types of components are installed with the Workplace Calendar Synchronization application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed with Workplace Calendar Synchronization

<table id="table_otr_ffn_5nb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace Calendar Synchronization admin \[sn\_wsd\_rsvsync.admin\]

</td><td>

As a system admin, you can do the following:-   Access the application completely.
-   Create, manage, and edit a Connection configuration.
-   Establish OAuth credentials.
-   Create, manage, and edit Calendar providers.
-   Retrieve reservations.

 As a Workplace Calendar Synchronization admin, you can create, manage, and edit a Reservable Sync Configuration.

</td><td>

None

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Tables installed with Workplace Calendar Synchronization

<table id="table_nfv_dgn_5nb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calendar Item\[sn\_wsd\_rsvsync\_calendar\_item\]

</td><td>

Stores information about all the calendar items that are created in the application.

</td></tr><tr><td>

Synchronization Delta\[sn\_wsd\_rsvsync\_delta\]

</td><td>

Stores information about the last successful synchronization of a workplace item. Each sync delta contains a token that indicates how much information was synced last time so that a delta with the new changes can be returned in the next request instead of the complete calendar history.**Note:** Starting from Workplace Calendar Synchronization version 2.0.1, for Microsoft Exchange Online, only Webhook is used for an improvised approach.

</td></tr><tr><td>

Event\[sn\_wsd\_rsvsync\_event\]

</td><td>

Store information about all the events that are created in the application. Events are created for actions such as create, read, update or delete.**Note:** If **WSD: Archive old workplace tasks** archival rule is applied then Event \[sn\_wsd\_rsvsync\_event\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Provider\[sn\_wsd\_rsvsync\_provider\]

</td><td>

Stores information about the configuration settings that are used for synchronizing the reservations with the calendar provider.

</td></tr><tr><td>

Reservable Sync Configuration\[sn\_wsd\_rsvsync\_reservable\_sync\_configuration\]

</td><td>

Stores information about all the workplace items that are configured to synchronize with a calendar service whenever a reservation is made.

</td></tr></tbody>
</table>## Tables installed with Retrieve reservations

<table id="table_ryk_4ph_ybc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retrieve reservations\[sn\_wsd\_rsvsync.admin\]

</td><td>

Retrieves all the events for the active **Reservable Sync Configurations** fromMicrosoft Outlook to Workplace Service Delivery

</td></tr><tr><td>

On demand sync executions\[sn\_wsd\_rsvsync.admin\]

</td><td>

It stores the parent record of the active Reservable Sync configurations.

</td></tr><tr><td>

Execution start time

</td><td>

Stores the start time when retrieve reservations was executed

</td></tr><tr><td>

Execution end time

</td><td>

Stores the end time when retrieve reservations got ended

</td></tr><tr><td>

Type

</td><td>

Displays the type of records.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Calendar Synchronization references](../concept/workplace-calendar-sync-references.md)

**Related topics**  


[Properties installed with Workplace Calendar Synchronization](properties-installed-with-workplace-calendar-syncn.md)

[Scheduled jobs installed with Workplace Calendar Synchronization](scheduled-jobs-installed-with-workplace-calendar-synchronization.md)

[Flows installed with Workplace Calendar Synchronization](flows-installed-with-workplace-calendar-synchronization.md)

[Instance scan findings](sacn-finding-messages.md)

