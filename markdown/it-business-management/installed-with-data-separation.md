---
title: Components installed with Data Separation
description: Several types of components are installed with activation of the Data Separation plugin, including user roles and tables.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Data Separation, Strategic Portfolio Management]
---

# Components installed with Data Separation

Several types of components are installed with activation of the Data Separation plugin, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Roles installed

|Role|Description|Contains roles|
|----|-----------|--------------|
|sn\_ds.ds\_admin|Can create/update/delete records in the tables required to configure the Data Separation feature.|sn\_align\_core.ap\_read\_only|
|sn\_ds.ds\_privileged\_user|Can create/update/delete records of any business function in Strategic Portfolio Management, even when Data Separation is enabled.|None|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Display name \[Table name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supported Entity\[sn\_ds\_data\_separation\_config\]

</td><td>

Stores the entity details \(Demand, Project, Resource Plan, Cost Plan, Cost Plan Breakdown, and Project Task\) for enabling Data Separation.

</td></tr><tr><td>

Entity-Group Mapping\[sn\_ds\_entity\_group\_mapping\]

</td><td>

Stores the lens entity and user group details for Data Separation.

</td></tr></tbody>
</table>**Parent Topic:**[Data Separation reference](data-separation-reference.md)

