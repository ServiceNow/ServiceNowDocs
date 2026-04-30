---
title: Certificate Inventory and Management tables
description: Certificate Inventory and Management tables provide a centralized system to track and manage digital certificates. They capture key details, including discovered certificates, installation locations, historical data, and associated tasks such as renewals and requests. This framework ensures efficient certificate management, supporting security, compliance, and streamlined operations.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Certificate Inventory and Management tables

Certificate Inventory and Management tables provide a centralized system to track and manage digital certificates. They capture key details, including discovered certificates, installation locations, historical data, and associated tasks such as renewals and requests. This framework ensures efficient certificate management, supporting security, compliance, and streamlined operations.

<table id="table_vph_p4w_31c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unique Certificate \[cmdb\_ci\_certificate\]

</td><td>

Discovery populates this table with one record for each unique certificate discovered for certificate management. Fingerprint column is unique for every server certificate.**Note:** You can also view the entire certificate chain using the related list in the Unique Certificate table.

</td></tr><tr><td>

Installed Certificate \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\]

</td><td>

Discovery populates this table with all discovered certificates and shows all locations where certificates are installed. It does not have a reference to the server CI and does not go through IRE. All the relationships with the managed certificate are stored in the CI Relationship \[cmdb\_rel\_ci\] table. The relationships can be for servers, applications, or business services.

</td></tr><tr><td>

Discovered Certificate \[sn\_disco\_certmgmt\_certificate\_history\]

</td><td>

Discovered certificates are stored in this table first as part of the Shazzam and URL discovery sensor and shows the XML payload of all certificates with that address.

</td></tr><tr><td>

Certificate Domain \[certificate\_domain\]

</td><td>

Stores one or more domains for the subject alternative name.

</td></tr><tr><td>

Certificate Task \[sn\_disco\_certmgmt\_certificate\_task\]

</td><td>

Stores all certificate renewal tasks and new certificate request tasks.

</td></tr><tr><td>

Certificate URL \[sn\_disco\_certmgmt\_cert\_url\]

</td><td>

Holds a list of URLs by row to target for certificate discovery.

</td></tr><tr><td>

Certificate Management Credential\[sn\_disco\_certmgmt\_certificate\_management\_credential\]

\(Version 1.1.7 Certificate Inventory and Management\)

</td><td>

Stores the CA types including GoDaddy and DigiCert. Others are populated based on the certificate\_authority script. Only discovery\_admin will be able to create other CA credentials. External Credential support will be available in a future release.

</td></tr><tr><td>

Scheduled Certificate URL\[sn\_discovery\_cert\_url\_sched\_m2m\]

</td><td>

Links the URLs to discover \[discovery\_cert\_url\] to a particular Discovery schedule \[discovery\_schedule\].

</td></tr><tr><td>

Certificate Authority\[sn\_disco\_certmgmt\_ca\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains the Certificate Authority Name and Base URL of REST API.

</td></tr><tr><td>

Certificate Authority API URL \[sn\_disco\_certmgmt\_ca\_api\_url\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains the reference of certificate authority, end point URL of REST API, and certificate validation type.

</td></tr><tr><td>

Routing Policy\[sn\_disco\_certmgmt\_routing\_policy\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Decides which CA needs to be contacted for certificate operations. This table contains the CA, CA URL, Credential, Approval Group, Assignment Group, and CSR attributes.

</td></tr><tr><td>

Automated Certificate Task \[sn\_disco\_certmgmt\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Contains all automated certificate request tasks \(new, renew, and revoke\).

</td></tr><tr><td>

New Certificate Tasks \[sn\_disco\_certmgmt\_new\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from sn\_disco\_certmgmt\_task and contains new certificate request tasks.

</td></tr><tr><td>

Renew Certificate Tasks\[sn\_disco\_certmgmt\_renew\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from sn\_disco\_certmgmt\_task and contains renew certificate request tasks.

</td></tr><tr><td>

Revoke Certificate Tasks \[sn\_disco\_certmgmt\_revoke\_task\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Extends from sn\_disco\_certmgmt\_task ans contains revoke certificate request tasks.

</td></tr><tr><td>

Certificate Extensions \[sn\_disco\_certmgmt\_certificate\_extension\]

\(Version 1.3.8 Certificate Inventory and Management\)

</td><td>

Stores information for all server certificates.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](cert-invt-mgmt-references.md)

