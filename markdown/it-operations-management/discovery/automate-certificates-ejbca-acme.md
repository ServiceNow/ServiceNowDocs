---
title: ACME integration with KeyFactor EJBCA for automated flows
description: Automate the flow of requesting, renewing, and revoking your certificates by integrating Keyfactor EJBCA with the Automated Certificate Management Environment \(ACME\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# ACME integration with KeyFactor EJBCA for automated flows

Automate the flow of requesting, renewing, and revoking your certificates by integrating Keyfactor EJBCA with the Automated Certificate Management Environment \(ACME\).

Keyfactor EJBCA is a certificate authority that issues your certificates. ACME are a set of protocols and rules that give you a secure environment to use an automated flow of managing certificates.

By configuring your routing policy fields, you can ensure that the content in your Certificate Signing Request \(CSR\) aligns with the correct routing policy. This streamlines the process of requesting, renewing, and revoking your certificates.

EJBCA has two types of Credentials. One includes External Account Binding \(EAB\), and the other doesn’t.

In EJBCA, automated certificate workflows start when you create routing policies for EJBCA ACME Certificates. For every routing policy, there are required fields where you have to give information.

Your platform has routing policies where you fill in all the fields of the routing policy. Your platform aligns that information to each CSR you create to request, renew, and revoke certificates.

For more information, see [Create a routing policy for EJBCA ACME certificates](../../discovery/task/routing-policies-ejbca-acme-certificates.md).

Perform the following task to use EJBCA ACME to automate your certificate life cycle:

1.  [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md)
2.  [Configure your base API URL for EJBCA ACME](../../discovery/task/configure-base-api-url-for-ejbca-acme.md)
3.  [Validate your EJBCA ACME base API URL](../../discovery/task/validate-ejbca-acme-base-api-url.md)

