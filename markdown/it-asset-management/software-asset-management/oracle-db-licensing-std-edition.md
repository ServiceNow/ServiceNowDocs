---
title: Oracle Database licensing for Standard Editions
description: Oracle Database Standard Editions are licensed on servers having a value less than the maximum capacity of sockets to help ensure risk-free license compliance.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Database licensing for Standard Editions

Oracle Database Standard Editions are licensed on servers having a value less than the maximum capacity of sockets to help ensure risk-free license compliance.

Sockets are slots on which processors or CPUs are placed. You must manually enter socket information under the non-discoverable field **Socket count** in the **cmdb\_hardware\_product\_model** hardware model table. ITOM Discovery discovers only the occupied slots and Software Asset Management reconciles and provides compliance.

<table id="table_spb_45j_1rb"><thead><tr><th>

Edition

</th><th>

Max rule for NUP and processor

</th></tr></thead><tbody><tr><td>

Oracle DB Standard Edition

</td><td>

4 sockets per server

</td></tr><tr><td>

Oracle DB Standard Edition 1

</td><td>

2 sockets per server

</td></tr><tr><td>

Oracle DB Standard Edition 2

</td><td>

2 sockets per server

</td></tr></tbody>
</table>## Oracle Standard Edition 2 deployed on a server with more than 2 sockets

The following example shows the message that would appear for a reclamation or removal candidate that doesn't follow the licensing rules.

`Oracle DB Server Standard Edition 2 installed on <Server Name> has been flagged as an unlicensed install. As per Oracle Licensing Policy, Oracle Database Standard Edition 2 may only be licensed on servers that have a maximum capacity of 2 sockets. This Server is found to have <no. of socket> number of sockets available. You are advised to uninstall the Oracle DB Server Standard Edition 2 from this server or upgrade to Oracle DB Enterprise Edition. We suggest working with your Oracle Database Administrator to assess the impact before proceeding with this action. Please note that the maximum number of sockets or slots available on a server are part of the hardware specification. Hence it is advised to update this information on the hardware product model <hw model name>. If this information is not present on the hardware model, it is assumed that all sockets are occupied and discovered.`

**Parent Topic:**[Software Asset Management publisher pack for Oracle](oracle-publisher-pack.md)

