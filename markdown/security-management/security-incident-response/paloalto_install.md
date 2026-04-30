---
title: Set up and install Palo Alto Networks Next-Generation Firewall
description: Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up and install Palo Alto Networks Next-Generation Firewall

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation.

## Before you begin

Role required: \(admin\)

<table id="table_xxz_jyj_4cb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have the required ServiceNow AI Platform and Security Incident Response roles assigned.

</td><td>

The following roles are required:-   The System Administrator \(admin\) installs the app and assigns the Security Incident Administrator \(sn\_si.admin\) role.
-   The Security Incident Administrator \(sn\_si.admin\) oversees the configuration, and creates, activates, and removes EDLs. This role also assigns the sn\_si.analyst role.
-   The \(admin\) assigns the ServiceNow AI Platform® API account role \(sn\_sec\_panfw.api\_account\_access\), which is used exclusively for entering credentials required for authentication on Palo Alto Networks so the firewalls can retrieve EDLs from the ServiceNow AI Platform®.
-   \(sn\_si.analyst\), or Security Operations Center \(SOC\) Analyst, creates EDL entries and works with security incidents.

</td></tr><tr><td>

Verify that you are using Palo Alto Networks Next-Generation Firewall version-OS 9.x, and 10.x.

</td><td>

This integration only supports Palo Alto Networks Next-Generation Firewall OS 9.0 and later.

</td></tr><tr><td>

Set up any EDL profiles, security policy rules, and certificate profiles in Palo Alto Networks as recommended in Palo Alto Networks documentation.

</td><td>

Refer to Palo Alto Networks general documentation and requirements at the: [Paloalto Networks Documentation website](https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-admin).

</td></tr><tr><td>

Verify that you have downloaded and configured the DigiCert Root Authority Certificate.

</td><td>

The integration requires this certificate to validate and authenticate the secure connection between the ServiceNow AI Platform server and the Palo Alto Networks Next-Generation Firewall server. For more information on setting up the certificate, see ["Configure a Certificate Profile" in the PAN-OS 10.0 Administrator's Guide](https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-admin/certificate-management/configure-a-certificate-profile). For the download, see [Create a certificate profile for the Palo Alto Networks Next-Generation Firewall](../concept/paloalto-create-cert-profile.md) and [DigiCert Trusted Root Authority Certificates](https://www.digicert.com/kb/digicert-root-certificates.htm).

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Madrid and later release requirements

 For the Madrid release and later family releases, the Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr><tr><td>

If your organization has ServiceNow AI Platform® change management and approval processes for email deletion, verify that email send/receive capability is enabled.

</td><td>

To verify that email send/receive capability is enabled in your ServiceNow AI Platform® instance, navigate to **Email properties** &gt; **Administration** &gt; **Email Properties**. In Outbound Email Configuration, verify **Email sending** and **Email receiving** are selected.

</td></tr></tbody>
</table>## Procedure

1.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.


**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Create a certificate profile for the Palo Alto Networks Next-Generation Firewall](../concept/paloalto-create-cert-profile.md)

**Next topic:**[Create the API account role for Palo Alto Networks Next-Generation Firewall](paloalto-create-snrole.md)

