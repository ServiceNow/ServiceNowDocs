---
title: External Related Files spoke
description: The External Related Files spoke stores information about files in third-party systems and helps you manage the information.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Spokes, Flow integrations, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# External Related Files spoke

The External Related Files spoke stores information about files in third-party systems and helps you manage the information.

<table id="table_zkq_pfp_mhb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External Provider \[sn\_ext\_files\_spoke\_provider\]

</td><td>

Stores information about the external provider. For example, Box or DocuSign services.

</td></tr><tr><td>

External Related Files \[sn\_external\_related\_files\]

</td><td>

Stores metadata information about the files in third-party systems. This table is extensible.**Note:** If you extend the table, ensure that you perform the data separation for the scoped applications

 -   To store metadata information of files in a specific third-party system, create a table with a column that contains a reference field to the External Related Files table. For more information about reference fields, see [Reference field type](https://www.servicenow.com/docs/access?context=c_ReferenceField&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   To establish a relationship between a specific ServiceNow table and External Related Files table, [Create defined related lists](https://www.servicenow.com/docs/access?context=t_CreateDefinedRelatedLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>|Action|Description|
|------|-----------|
|Create External File Record|Creates a record in the External Related Files table.|
|Update External File Record|Updates a record in the External Related Files table.|
|Delete External File Record|Deletes a record in the External Related Files table.|

<table id="table_ydk_dkp_mhb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ext\_files\_spoke.doc\_reader

</td><td>

Read records in the External Related Files and External Provider tables.

</td></tr><tr><td>

sn\_ext\_files\_spoke.file\_admin

</td><td>

-   Read, update, and delete records in the External Related Files table.
-   Read records in the External Provider table.

</td></tr><tr><td>

sn\_ext\_files\_spoke.provider\_admin

</td><td>

Read, update, and delete records in the External Provider table.

</td></tr></tbody>
</table>**Parent Topic:**[Spokes](../concept/spokes.md)

