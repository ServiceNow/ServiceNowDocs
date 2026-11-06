---
title: Certificate Inventory and Management tables
description: This framework supports security, compliance, and streamlined operations. Certificate Inventory and Management tables provide a centralized system to track and manage digital certificates. They capture key details, including discovered certificates, installation locations, historical data, and associated tasks such as renewals and requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/cert-invt-mgmt-tables.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Inventory and Management tables

This framework supports security, compliance, and streamlined operations. Certificate Inventory and Management tables provide a centralized system to track and manage digital certificates. They capture key details, including discovered certificates, installation locations, historical data, and associated tasks such as renewals and requests.

<table id="table_vph_p4w_31c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unique Certificate \[cmdb\_ci\_certificate\]

</td><td>

The Fingerprint column is unique for every server certificate. **Note:** You can also view the entire certificate chain using the related list in the Unique Certificate table. The State field records the life cycle state of the certificate and doesn't include an Expired value. Expired certificates are denoted as Issued. Use the Valid to field to identify certificates that have expired.

</td></tr><tr><td>

Installed Certificate \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\]

</td><td>

Discovery populates this table with all discovered certificates and shows all locations where certificates are installed. It does not have a reference to the server CI and does not go through IRE. Relationships with the managed certificate are stored in the CI Relationship \[cmdb\_rel\_ci\] table. The relationships can be for servers, applications, or business services.

</td></tr><tr><td>

Discovered Certificate \[sn\_disco\_certmgmt\_certificate\_history\]

</td><td>

Discovered certificates are stored in this table first as part of the Shazzam and URL discovery sensor and shows the XML payload of all certificates with that address.

</td></tr><tr><td>

Certificate Domain \[certificate\_domain\]

</td><td>

Contains one or more domains for the subject alternative name.

</td></tr><tr><td>

Certificate Task \[sn\_disco\_certmgmt\_certificate\_task\]

</td><td>

Contains all certificate renewal tasks and new certificate request tasks.

</td></tr><tr><td>

Certificate URL \[sn\_disco\_certmgmt\_cert\_url\]

</td><td>

Contains URLs targeted for certificate discovery.

</td></tr><tr><td>

Certificate Management Credential\[sn\_disco\_certmgmt\_certificate\_management\_credential\]

\(Version 1.1.7 Certificate Inventory and Management\)

</td><td>

Stores the CA types including GoDaddy and DigiCert. Others are populated based on the **certificate\_authority** script. Only discovery\_admin can create other CA credentials.

</td></tr><tr><td>

Scheduled Certificate URL\[sn\_discovery\_cert\_url\_sched\_m2m\]

</td><td>

Links the URLs to discover \[discovery\_cert\_url\] to a particular Discovery schedule \[discovery\_schedule\].

</td></tr><tr><td>

Certificate Authority\[sn\_disco\_certmgmt\_ca\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains the Certificate Authority name and base URL of the REST API.

</td></tr><tr><td>

Certificate Authority API URL \[sn\_disco\_certmgmt\_ca\_api\_url\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains the reference of certificate authority, end point URL of REST API, and certificate validation type.

</td></tr><tr><td>

Routing Policy\[sn\_disco\_certmgmt\_routing\_policy\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Determines which CA to contact for certificate operations. This table contains the CA, CA URL, Credential, Approval Group, Assignment Group, and CSR attributes.

</td></tr><tr><td>

Automated Certificate Task \[sn\_disco\_certmgmt\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains all automated certificate request tasks \(new, renew, and revoke\).

</td></tr><tr><td>

New Certificate Tasks \[sn\_disco\_certmgmt\_new\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from \[sn\_disco\_certmgmt\_task\] and contains new certificate request tasks.

</td></tr><tr><td>

Renew Certificate Tasks\[sn\_disco\_certmgmt\_renew\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from \[sn\_disco\_certmgmt\_task\] and contains renew certificate request tasks.

</td></tr><tr><td>

Revoke Certificate Tasks \[sn\_disco\_certmgmt\_revoke\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from \[sn\_disco\_certmgmt\_task\] and contains revoke certificate request tasks.

</td></tr><tr><td>

Certificate Extensions \[sn\_disco\_certmgmt\_certificate\_extension\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Stores information for all server certificates.

</td></tr><tr><td>

Microsoft Teams Channel \[sn\_disco\_certmgmt\_microsoft\_teams\_channel\]

\(Version 4.2.0 Certificate Inventory and Management\)

</td><td>

Stores the Microsoft Teams channel configuration.

</td></tr><tr><td>

Certificate Notification Policy\[sn\_disco\_certmgmt\_notification\_policy\]

\(Version 4.2.0 Certificate Inventory and Management\)

</td><td>

Stores the Microsoft Teams channel notification settings for certificate events.

</td></tr><tr><td>

Certificate Metadata \[sn\_disco\_certmgmt\_certificate\_metadata\]

\(Version \[OXY-PLACEHOLDER\] Certificate Inventory and Management\)

</td><td>

Stores one record for each certificate in the Unique Certificate \[cmdb\_ci\_certificate\] table. Each record contains the private key vault reference \(HashiCorp Vault or Azure Key Vault\), the certificate format used at issuance \(PEM, DER, or PKCS12\), and the auto-renewal settings. Auto-renewal settings include whether auto renewal is enabled, the number of days before expiry to trigger renewal \(default 30\), the renewal date, and the renewal state \(ready, processing, processed, or error\). The settings also store the retry count and the Renew Certificate Task \[sn\_disco\_certmgmt\_renew\_task\] used to renew the certificate.

</td></tr><tr><td>

DNS Task \[sn\_disco\_certmgmt\_dns\_task\]

\(Version \[OXY-PLACEHOLDER\] Certificate Inventory and Management\)

</td><td>

Extends from Task \[task\] and tracks the DNS validation for a certificate request in the Automated Certificate Task \[sn\_disco\_certmgmt\_task\] table. Contains the reference to the certificate task, the order URL, the finalize URL that is called after all domains are validated, and the state of the DNS task \(Work in Progress, Completed, or Failed\).

</td></tr><tr><td>

DNS Challenge \[sn\_disco\_certmgmt\_dns\_challenge\]

\(Version \[OXY-PLACEHOLDER\] Certificate Inventory and Management\)

</td><td>

Contains the DNS challenges for a DNS task \[sn\_disco\_certmgmt\_dns\_task\]. Each record stores the domain that the challenge belongs to, the DNS key and DNS value to add to the DNS record, and the challenge URL that is called to validate the challenge.

</td></tr><tr><td>

Certificate Request UID to Task Map \[sn\_disco\_certmgmt\_uid\_to\_task\_map\]

\(Version \[OXY-PLACEHOLDER\] Certificate Inventory and Management\)

</td><td>

Maps a certificate request UID to the Automated Certificate Task \[sn\_disco\_certmgmt\_task\] created for it. Each record contains the certificate request UID, the certificate task, and whether the mapping is active.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cert-invt-mgmt-references.md)

