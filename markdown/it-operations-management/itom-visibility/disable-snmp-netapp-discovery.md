---
title: Disable SNMP-based NetApp storage cluster discovery
description: Disable the default SNMP-based NetApp storage cluster discovery and use REST-based discovery instead for enhanced security.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [NetApp Server and Cluster, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Disable SNMP-based NetApp storage cluster discovery

Disable the default SNMP-based NetApp storage cluster discovery and use REST-based discovery instead for enhanced security.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **SNMP**.

2.  In the **Name** field, search for `NetApp Storage Server Cluster-Mode`.

3.  Select the NetApp Storage Server Cluster-Mode record.

4.  Clear the **Active** check box.

5.  Select **Update**.


## What to do next

Configure basic authentication credentials for a user with a read-only role. For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Related topics**  


[NetApp Server and Cluster discovery](../../discovery/concept/netapp-discovery.md)

