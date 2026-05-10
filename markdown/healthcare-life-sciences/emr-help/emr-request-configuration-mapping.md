---
title: Request configuration mapping table
description: The Request configuration mapping \[sn\_ind\_rmt\_help\_defn\_param\_data\_map\] table stores the association between the request parameter and the request definition.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Request configuration mapping table

The Request configuration mapping \[sn\_ind\_rmt\_help\_defn\_param\_data\_map\] table stores the association between the request parameter and the request definition.

The Request configuration mapping \[sn\_ind\_rmt\_help\_defn\_param\_data\_map\] table has the following features:

-   Extends the Application File \[sys\_metadata\] table that uses the update\_synch dictionary attribute to enable customizations. For more information, see [Customizations tracked by update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/customizations-tracked-update-sets.md).
-   For a request definition, maps each active request parameter to a specific column in the corresponding request data table.

Role required to configure the table: sn\_ind\_rmt\_help.admin.

<table id="table_k4j_nvy_11c"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain

</td><td>

Domain ID

</td><td>

The domain associated with this record.

</td></tr><tr><td>

Internal ID

</td><td>

String

</td><td>

The internal ID associated with this record.

</td></tr><tr><td>

Order

</td><td>

Integer

</td><td>

The order that your parameters display in the contextual sidebar.

</td></tr><tr><td>

Request data column

</td><td>

Field Name

</td><td>

The field on the task type table that is defined in the request definition.

</td></tr><tr><td>

Request definition

</td><td>

Reference

</td><td>

References the remote request definition.

</td></tr><tr><td>

Request parameter

</td><td>

Reference

</td><td>

References the remote request parameter.

</td></tr></tbody>
</table>**Parent Topic:**[EMR Help data model tables](tables-installed-with-emr-help.md)

