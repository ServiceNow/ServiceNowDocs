---
title: Automated certificate management for TLS certificates
description: From Certificate Inventory and Management Version 1.3.8, you can automate the request flow for new certificates, renewals, and revoking certificates.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Automated certificate management for TLS certificates

From Certificate Inventory and Management Version 1.3.8, you can automate the request flow for new certificates, renewals, and revoking certificates.

Certificate Inventory and Management automatically fetches certificates from Certificate Authorities \(CAs\) without requiring manual intervention from the PKI team. Starting in Version 2.1.0, this feature supports DigiCert and Entrust CA Gateway for seamless automatic fulfillment flows, with the limitation that only OV DigiCert certificates can be requested. Version 2.3.2 introduces support for the Microsoft CA. For more information, refer to the respective provider documentation. For automated flows with DigiCert or Entrust CA Gateway in Certificate Inventory and Management, you must have permissions to request, renew, and revoke certificates.

The Microsoft CA user requires the following permissions:

<table id="table_xdl_5jz_31c"><thead><tr><th>

Permission

</th><th>

Action

</th></tr></thead><tbody><tr><td>

CredSSP on CA, intermediate server, and MID Server

</td><td>

Set up CredSSP on CA, intermediate server, and MID Server.For CredSSP configuration steps, see the Now Support Knowledge Base documented in the KB article [KB1632624](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1632624).

</td></tr><tr><td>

Membership in Enterprise Admins

</td><td>

Ensure the user holds membership in the Enterprise Admins group.

</td></tr><tr><td>

Security Group Inclusion for Template

</td><td>

Ensure the user is included in the Security Group of the template.

</td></tr><tr><td>

Specific Permissions in CA

</td><td>

Grant the user permissions: Read, Issue and Manage Certificates, Manage CA, and Request Certificates in the CA.

</td></tr></tbody>
</table>