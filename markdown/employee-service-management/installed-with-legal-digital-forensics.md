---
title: Components installed with Legal Digital Forensics
description: Several types of components are installed with activation of the Legal Digital Forensics application, including tables and user roles.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Digital Forensics, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Digital Forensics

Several types of components are installed with activation of the Legal Digital Forensics application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Forensics Administrator\[sn\_lg\_forensics.forensics\_admin\]

</td><td>

Application-specific administrator role for the Legal Digital Forensics app having the administrative access for the app and full access to the underlying data.

</td><td>

-   sn\_lg\_forensics.forensics\_config
-   sn\_lg\_forensics.forensics\_fulfiller

</td></tr><tr><td>

Forensics Configurator\[sn\_lg\_forensics.forensics\_config\]

</td><td>

Provides access to configure data for the Legal Digital Forensics app such as search sources.

</td><td>

sn\_lg\_forensics.forensics\_fulfiller

</td></tr><tr><td>

Forensics Fulfiller\[sn\_lg\_forensics.forensics\_fulfiller\]

</td><td>

Provides the fulfiller access for working on assigned digital forensic requests and matters.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custodial Core\[sn\_lg\_forensics\_custodian\]

</td><td>

Users from the Legal Profile table that are added in a digital forensics request.

</td></tr><tr><td>

Custodial Data\[sn\_lg\_forensics\_custodial\_data\]

</td><td>

Extends the Custodial Core table and has additional fields to store information of users added in a digital forensics request.

</td></tr><tr><td>

Data Source\[sn\_lg\_forensics\_search\_source\]

</td><td>

Search sources, checklist items, and instructions for the task owners for the resolution of legal requests. You can configure search sources such as Slack, Box, OneDrive, or Microsoft Outlook.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Data Source Details\[sn\_lg\_forensics\_search\_source\_detail\]

</td><td>

Details recorded for a search source for custodians by the task owner while working on a digital forensics matter task.

</td></tr><tr><td>

Fulfillment Steps\[sn\_lg\_forensics\_fulfillment\_steps\]

</td><td>

Steps required for a task owner to fulfill an assigned digital forensics request.Extends the Application File \[sys\_metadata\] table.

</td></tr><tr><td>

Non Custodial Core\[sn\_lg\_forensics\_non\_custodial\_data\]

</td><td>

Extends the Custodial Core table and has additional fields to store information of non-custodial records added in a digital forensics request.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Digital Forensics reference](legal-dft-reference.md)

