---
title: LDAP integration setup
description: Administrators can enable LDAP integration to allow sign-on of users from their company LDAP directory.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# LDAP integration setup

Administrators can enable LDAP integration to allow sign-on of users from their company LDAP directory.

LDAP typically uses one of these types of communication channels.

|Connection|Description|LDAP import support?|LDAP authentication support?|
|----------|-----------|--------------------|----------------------------|
|MID Server connection|Communicates over HTTP on port 80 by default. This communication channel does not require a certificate. The connection between the MID Server and the instance is over HTTPS \(port 443\). You can use the MID Server to import data over LDAP, but you cannot use the MID Server for LDAP authentication. Proceed to [Define the LDAP Server](../task/t_DefineAnLDAPServer.md).|Yes|No|
|Standard LDAP integration|Communicates over TCP on port 389 by default. This communication channel does not require a certificate. Proceed to [Define the LDAP Server](../task/t_DefineAnLDAPServer.md).|Yes|Yes|
|SSL-encrypted LDAP integration \(LDAPS\)|Communicates over TCP on port 636 by default, This communication channel requires a certificate. Proceed to [Install the LDAP X.509 SSL certificate](../task/t_UploadTheX509SSLCertificate.md) to obtain and upload the certificate.|Yes|Yes|
|VPN connection|Communicates over an IPSEC tunnel. Purchase or create an IPSEC tunnel on your local network. Proceed to [Define the LDAP Server](../task/t_DefineAnLDAPServer.md).|Yes|Yes|

If using a MID Server, the MID Server connects to the instance and the MID Server also connects to the LDAP server. In both cases, the MID Server initiates the connection:

1.  First, the MID Server connects to the LDAP server via LDAP on Port 389.
2.  Then, the MID Server initiates an HTTPS encrypted connection to the instance on Port 443 to push the data to the instance.

For more information about VPNs, Mid Servers, and LDAP, see [You Don't Need A VPN Part II](https://community.servicenow.com/community?id=community_blog&sys_id=10dd26e9dbd0dbc01dcaf3231f9619c8&view_source=searchResult) on the community.

