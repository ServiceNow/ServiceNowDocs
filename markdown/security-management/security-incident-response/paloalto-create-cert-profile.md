---
title: Create a certificate profile for the Palo Alto Networks Next-Generation Firewall
description: The integration requires a certificate profile to validate and authenticate the secure connection between the ServiceNow AI Platform server and the Palo Alto Networks Next-Generation Firewall server.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a certificate profile for the Palo Alto Networks Next-Generation Firewall

The integration requires a certificate profile to validate and authenticate the secure connection between the ServiceNow AI Platform® server and the Palo Alto Networks Next-Generation Firewall server.

Role required: Palo Alto Networks Next-Generation Firewall Administrator.

A Palo Alto Networks Next-Generation Firewall authenticates to a ServiceNow AI Platform® instance, retrieves EDL entries from the database table, and incorporates the entries into corresponding firewall policy rules. This retrieval requires the API user account role in the ServiceNow AI Platform® instance, which is used by the PAN firewall admin to access the ServiceNow AI Platform® API.

Follow the steps below on how to download DigiCertificates and configure the certificate profile.

1.  Download DigiCert or Entrust CA Gateway Certificate based on the use case. For more information, see the [KB1702083](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1702083) article in the Now Support Knowledge Base.
2.  Configure the certificate profile. For more information, see [Palo Alto Networks documentation](https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-admin/certificate-management/configure-a-certificate-profile).

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](paloalto_integration.md)

**Previous topic:**[Palo Alto Networks Next-Generation Firewall integration](paloalto_integration.md)

**Next topic:**[Set up and install Palo Alto Networks Next-Generation Firewall](../task/paloalto_install.md)

**Related topics**  


["Configure a Certificate Profile" in the PAN-OS 10.0 Administrator's Guide](https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-admin/certificate-management/configure-a-certificate-profile)

