---
title: Domain separation properties for Event Management connectors
description: Properties provide the metadata to identify the domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/system-default-properties-personalizing-domain-separation-event-management-connectors.html
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-11-19"
reading_time_minutes: 1
breadcrumb: [Reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Domain separation properties for Event Management connectors

Properties provide the metadata to identify the domain.

You can change the values if you want to use any other table or fields for domain identification but make sure that the table is domain separated.

**Note:** When personalizing domain separation for event management connectors, all the properties can be overridden at the connector level as well.

There are three caches maintained for personalizing domain separation \(main, user\_access, missing\_domain\). You can create a few system properties to control them.

<table id="table_e5g_lsy_nxb"><thead><tr><th align="left">

Property

</th><th>

Description

</th></tr></thead><thead><tr><th align="left">

Property

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

evt\_mgmt. connector\_domain\_info\_table\_name

</td><td>

The table where you store domain information for personalizing domain separation.

-   **Type**: string
-   **Default value**: core\_company

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_info\_column\_name

</td><td>

The field name in the table to identify the provided domain for personalizing domain separation.-   **Type**: string
-   **Default value**: name

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_id\_column\_name

</td><td>

The field to get domain ID from for personalizing domain separation.-   **Type**: string
-   **Default value**: sys\_domain

</td></tr><tr><td>

evt\_mgmt. connector\_domain\_path\_column\_name

</td><td>

The field to get the domain path from for personalizing domain separation.-   **Type**: string
-   **Default value**: sys\_domain\_path

</td></tr></tbody><tbody><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_cache\_expire\_in\_seconds

</td><td>

For personalizing domain separation, if you don’t want your main cache to expire every week.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_user\_access\_on\_domain\_cache\_size

</td><td>

For personalizing domain separation, if you want to increase the size of the user access cache.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_missing\_domain\_cache\_expire\_in\_seconds

</td><td>

For personalizing domain separation, if you want to increase the expire time for cache storing information regarding the missing domain.

</td></tr><tr><td>

evt\_mgmt.connector\_custom\_domain\_sep\_cache\_size

</td><td>

For personalizing domain separation, if you need more main cache size for storing domain information.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-management-reference.md)

