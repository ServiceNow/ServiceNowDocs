---
title: Components installed with Gifts and Entertainment Compliance
description: Several types of components are installed with installation of the Gifts and Entertainment Compliance, including tables and user roles.
locale: en-US
release: australia
product: Legal Gifts and Entertainment
classification: legal-gifts-and-entertainment
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Gifts and Entertainment Compliance, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Gifts and Entertainment Compliance

Several types of components are installed with installation of the Gifts and Entertainment Compliance, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Gifts and Entertainment administrator\[sn\_lg\_gifts.gifts\_admin\]

</td><td>

Provides the administrative permissions for Gifts &amp; Entertainment app and full access to the underlying data.

</td><td>

-   sn\_lg\_gifts.gifts\_fulfiller
-   sn\_lg\_gifts.gifts\_config

</td></tr><tr><td>

Gifts and Entertainment Configurator\[sn\_lg\_gifts.gifts\_config\]

</td><td>

Provides access to configure data for the Gifts &amp; Entertainment application.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Gifts and Entertainment Fulfiller\[sn\_lg\_gifts.gifts\_fulfiller\]

</td><td>

Provides fulfiller access to all Gifts &amp; Entertainment disclosure records.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Flows

|Flow|Description|
|----|-----------|
|Gifts Approval|This flow controls the multi-level approvals for gift and entertainment disclosure requests.|

## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Gift Policy\[sn\_lg\_gifts\_policy\_configuration\]

</td><td>

Stores gifts and entertainment policy records.

</td></tr></tbody>
</table>**Parent Topic:**[Gifts and Entertainment Compliance reference](lsd-ge-reference.md)

