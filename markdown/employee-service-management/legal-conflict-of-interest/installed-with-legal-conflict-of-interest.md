---
title: Components installed with Legal Conflict of Interest
description: Several types of components are installed with installation of the Legal Conflict of Interest, including tables and user roles.
locale: en-US
release: xanadu
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legal Conflict of Interest reference, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Components installed with Legal Conflict of Interest

Several types of components are installed with installation of the Legal Conflict of Interest, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

COI Admin\[sn\_lg\_coi.coi\_admin\]

</td><td>

Provides the administrative permissions for Conflict of Interest app and full access to the underlying data.

</td><td>

sn\_lg\_coi.coi\_fulfiller

</td></tr><tr><td>

COI Fulfiller\[sn\_lg\_coi.coi\_fulfiller\]

</td><td>

Provides fulfiller access to all conflict of interest disclosure records.

</td><td>

sn\_lg\_coi.coi\_read

</td></tr><tr><td>

COI Read\[sn\_lg\_coi.coi\_read\]

</td><td>

Provides the read-only access to view all conflict of interest records.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Scheduled jobs

|Scheduled job|Description|
|-------------|-----------|
|Send Reminder Email to COI Requestor|The job checks for the active conflict of interest disclosure records that have the end date in the next 30 days. For all such records, it sends reminder notifications to requesters to update any changes in their conflicts records.|

## Flows

|Flow|Description|
|----|-----------|
|COI Approval flow|This flow controls the multi-level approvals for conflict of interest disclosure requests.|
|Scheduled Flow to Deactivate COI|This scheduled flow runs daily to check for the active conflict of interest disclosure records for which the end date has passed the current date. For all such records, it updates the state from Active to Inactive.|

## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conflict of Interest Associated Requests\[sn\_lg\_coi\_coi\_request\]

</td><td>

Stores the mapping of legal requests submitted by the user and the conflict of interest disclosure records.

</td></tr><tr><td>

Conflict of Interest Disclosure\[sn\_lg\_coi\_conflict\_of\_interest\]

</td><td>

Stores conflict of interest disclosure records.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Conflict of Interest reference](legal-coi-reference.md)

