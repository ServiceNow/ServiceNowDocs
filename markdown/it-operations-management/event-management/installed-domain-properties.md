---
title: Domain properties installed with Event Management
description: Use the domain properties installed with Event Management to provide the metadata that points to the appropriate table to identify the domain so that you know which domain to create the event in.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Domain properties installed with Event Management

Use the domain properties installed with Event Management to provide the metadata that points to the appropriate table to identify the domain so that you know which domain to create the event in.

<table id="table_e5g_lsy_nxb"><thead><tr><th align="left">

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evt\_mgmt. connector\_domain\_info\_table\_name

</td><td>

Table that stores domain information.

-   **Type**: string
-   **Default value**: core\_company

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_info\_column\_name

</td><td>

Table field to identify the provided domain.-   **Type**: string
-   **Default value**: name

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_id\_column\_name

</td><td>

Field that provides the domain ID.-   **Type**: string
-   **Default value**: sys\_domain

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_path\_column\_name

</td><td>

Field that provides the domain path.-   **Type**: string
-   **Default value**: sys\_domain\_path

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

