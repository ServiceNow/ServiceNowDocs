---
title: LDAP integration via MID Server
description: Administrators can integrate using an LDAP data source over a Management, Instrumentation, and Discovery \(MID\) Server.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# LDAP integration via MID Server

Administrators can integrate using an LDAP data source over a Management, Instrumentation, and Discovery \(MID\) Server.

The MID Server enables communication and movement of data between the ServiceNow AI Platform and external applications, data sources, and services. For details on installing a MID Server, see [MID Server installation](https://www.servicenow.com/docs/access?context=mid-server-installation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Using a MID Server to establish an LDAP connection prevents you from having to expose the LDAP server to external network traffic. It eliminates the need to establish a VPN tunnel between your LDAP server and datacenters. The MID Server user must have the user\_admin role to be able to read LDAP server configuration records.

**Note:** The MID Server does not allow using the UI action `<instance>/sys_ui_action.do?sys_id=1b4f7ef30a0001060058e223c9a5744c` to refresh user and group records from LDAP.

A MID Server connection communicates over HTTP on port 80 by default. This communication channel does not require a certificate. The connection between the MID Server and the instance is over HTTPS \(port 443\). The instance connects to the LDAP server directly, using LDAP or LDAPS. This connection can either be over the internet or through a VPN tunnel.

**Note:** LDAP cannot communicate via the MID Server with password authentication.

For a secure communication over SSL, you must [add an SSL certificate for the MID Server](https://www.servicenow.com/docs/access?context=add-ssl-certificates&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Change the LDAP server URL from LDAP to LDAPS and change to port 636.

![LDAPS connection URL and SSL flag](../image/ldaps-midserver-setting.png)

**Note:** If you create a new LDAP server, the MID Server SSL flag sets to false by default. You can ignore this behavior.

To set connection properties for a specific LDAP server, see [Define an LDAP server](../task/t_DefineAnLDAPServer.md).

