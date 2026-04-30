---
title: Components installed with Legal Conflict of Interest
description: Several types of components are installed with installation of the Legal Conflict of Interest, including tables and user roles.
locale: en-US
release: zurich
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Conflict of Interest

Several types of components are installed with installation of the Legal Conflict of Interest, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

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

-   sn\_lg\_coi.coi\_fulfiller
-   sn\_lco\_cmn.admin

</td></tr><tr><td>

COI Fulfiller\[sn\_lg\_coi.coi\_fulfiller\]

</td><td>

Provides fulfiller access to all conflict of interest disclosure records.

</td><td>

-   sn\_lg\_coi.coi\_read
-   sn\_lco\_cmn.risk\_reader

</td></tr><tr><td>

COI Read\[sn\_lg\_coi.coi\_read\]

</td><td>

Provides the read-only access to view all conflict of interest records.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal and Contracts Common Utilities configurator\[sn\_lco\_cmn.config\]

</td><td>

Provides write permission on the Legal and Contracts Common Utilities records

</td><td>

-   decision\_table\_admin
-   sn\_doc.writer

</td></tr><tr><td>

Legal and Contracts Common Utilities administrator\[sn\_lco\_cmn.admin\]

</td><td>

Provides administrator permission on the Legal and Contracts Common Utilities records

</td><td>

-   sn\_lco\_cmn.config
-   sn\_lco\_cmn.risk\_reader

</td></tr><tr><td>

Legal and Contracts Common Utilities reader\[sn\_lco\_cmn.risk\_reader\]

</td><td>

Provides read permission on the Legal and Contracts Common Utilities records

</td><td>

None

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

</td></tr><tr><td>

Risk factor conditions\[sn\_lco\_risk\_factor\_conditions\]

</td><td>

Stores the risk factor condition records used to evaluate a risk factor.

</td></tr><tr><td>

Risk factor\[sn\_lco\_risk\_factor\]

</td><td>

Stores the risk factor records associated with risk assessment.

</td></tr><tr><td>

Overall risk assessment scoresn\_lco\_overall\_risk\_assessment\_score

</td><td>

Stores the overall risk assessment score records.

</td></tr><tr><td>

Risk assessment\[sn\_lco\_risk\_assessment\]

</td><td>

Store the risk assessment records.

</td></tr><tr><td>

Risk responsesn\_lco\_risk\_response

</td><td>

Store the risk response records for the evaluated risk factors.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Conflict of Interest reference](legal-coi-reference.md)

