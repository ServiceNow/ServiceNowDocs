---
title: Configure Discovery for UNIX or Linux hosts with attached storage
description: Discovery can find information about a UNIX or Linux host and attached storage.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure discovery of hosts with attached storage, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Configure Discovery for UNIX or Linux hosts with attached storage

Discovery can find information about a UNIX or Linux host and attached storage.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  On the host, assign elevated privileges to the account that Discovery will use.

2.  On the ServiceNow instance, add credentials to the Discovery Credentials table.

3.  Create a Discovery Schedule for each host IP address.

4.  Create a behavior that uses a functionality definition with a wbem port probe to make the initial port-scanning phase \(Shazzam\) more efficient.

5.  Run network discovery.

    **Note:** If the host also connects to a NAS or SAN storage array, set up the [SMI-S Provider](t_ConfigDiscoForStandaloneStorage.md) and CIM credentials.


**Parent Topic:**[Configure discovery of hosts with attached storage](../concept/configure-discovery-of-hosts-with-attached-storage.md)

