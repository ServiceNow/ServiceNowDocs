---
title: Components installed with Workplace Move Management
description: Several types of components are installed with the Workplace Move Management application, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workplace Move Management references, Workplace Move Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Move Management

Several types of components are installed with the Workplace Move Management application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed with Workplace Move Management

<table id="table_rpj_13j_qpb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace move admin \[sn\_wsd\_move.admin\]

</td><td>

As a Workplace Move Management admin, you can access the application completely.

</td><td>

sn\_wsd\_move.manager

</td></tr><tr><td>

Workplace move manager\[sn\_wsd\_move.manager\]

</td><td>

As a Workplace Move Manager, you can access the application completely.

</td><td>

-   sn\_wsd\_move.agent
-   template\_editor\_global

</td></tr><tr><td>

Workplace move agent\[sn\_wsd\_move.agent\]

</td><td>

-   Create, read, update, and delete Move tasks.
-   Create, read, update, and delete Move cases.
-   Create knowledge base articles.

</td><td>

-   sn\_wsd\_move.writer
-   flow\_operator
-   sn\_wsd\_core.kb\_writer

</td></tr><tr><td>

Workplace move writer\[sn\_wsd\_move.writer\]

</td><td>

-   Create, read, update, and delete Move tasks.
-   Create, read, update, and delete Move cases.

</td><td>

-   sn\_wsd\_move.reader
-   sn\_wsd\_case.case\_writer

</td></tr><tr><td>

Workplace move reader\[sn\_wsd\_move.reader\]

</td><td>

Has read permissions to access the following:-   Move tasks
-   Move cases

</td><td>

sn\_wsd\_case.case\_reader

</td></tr></tbody>
</table>## Tables installed with Workplace Move Management

<table id="table_t5k_1kj_qpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Move Case\[sn\_wsd\_move\_case\]

</td><td>

Stores information about all the move cases and child move cases created in the application.**Note:** This table is a child table of Workplace tasks \[sn\_wsd\_core\_workplace\_task\] in Workplace Core. If **WSD: Archive old workplace tasks** archival rule is applied then Workplace Move Case \[sn\_wsd\_move\_case\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Move Request Conflict\[sn\_wsd\_move\_request\_conflict\]

</td><td>

Stores information about all the move conflicts that occurred while agents were fulfilling a move request in the application.

</td></tr><tr><td>

Workplace Move Task\[sn\_wsd\_move\_task\]

</td><td>

Stores information about all the move tasks and child move tasks created in the application.**Note:** If **WSD: Archive old workplace tasks** archival rule is applied then Workplace Move Task \[sn\_wsd\_move\_task\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Move Management references](../concept/workplace-move-mgmt-references.md)

