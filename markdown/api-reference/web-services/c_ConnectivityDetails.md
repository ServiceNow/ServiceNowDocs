---
title: Connectivity details
description: For SOAP requests initiated from your ServiceNow instance to be able to successfully communicate with the web service provider inside a remote network, the ServiceNow instance must have HTTP or HTTPS access to the SOAP endpoint at the provider.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Connectivity details

For SOAP requests initiated from your ServiceNow instance to be able to successfully communicate with the web service provider inside a remote network, the ServiceNow instance must have HTTP or HTTPS access to the SOAP endpoint at the provider.

Like any integration, such as LDAP, web services, or JDBC, the SOAP endpoint may reside behind a firewall that is blocking inbound communication from the instance. If this is the case, you need to make network changes to allow this connectivity into your network. You can either modify the firewall and ACL rules to allow the instance IP address, configure the SOAP message to be sent through a MID Server, or implement a Virtual Private Network \(VPN\) tunnel to allow the instance communication into your network.

**Note:** A common misconception is that because asynchronous SOAP requests are routed through the ECC queue, they are always sent through a MID Server. However, asynchronous SOAP requests use a MID Server only when configured to do so.

**Parent Topic:**[Outbound SOAP web service](c_OutboundSOAPWebService.md)

