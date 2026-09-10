---
title: Automated certificate management with ACME
description: The Automated Certificate Management Environment \(ACME\) is a communication protocol that automates the interaction between a certificate authority \(CA\) and a server. It streamlines the processes of requesting, renewing, and revoking SSL/TLS certificates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/exploring-acme.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Automated certificate management with ACME

The Automated Certificate Management Environment \(ACME\) is a communication protocol that automates the interaction between a certificate authority \(CA\) and a server. It streamlines the processes of requesting, renewing, and revoking SSL/TLS certificates.

## ACME overview

ACME uses JSON-formatted messages transmitted over a secure HTTPS connection. This communication enables for automated certificate life-cycle management, reducing manual intervention and the risk of errors.

ACME is a widely adopted standard used by public key infrastructure admins, line of business owners, certificate management users, admins, account owners, and team managers.

Certificate Inventory and Management supports the following ACME CAs: DigiCert, Entrust, Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public. The ACME framework is extensible to any ACME-compatible certificate authority. Admins can add a CA by creating a record in the Certificate Authority \[sn\_disco\_certmgmt\_ca\] table. For more information, see [Add ACME-compatible certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-acme-compatible-certificate-authorities.md).

## ACME benefits

During requesting, renewing, or revoking SSL/TLS certificates, ACME offers significant benefits:

-   It automates tasks associated with certificate management, reducing the administrative burden for IT teams.
-   It helps verify that the certificates are valid and up-to-date.
-   It eliminates the need for manual certificate management tasks, reducing overall costs.

