---
title: Certificate request form
description: The Request New Certificate \(Automated\) and Renew Certificate \(Automated\) forms enable you to submit or update a Certificate Signing Request \(CSR\) to be submitted to a certificate authority.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/req-new-cert-form-table-fields.html
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate request form

The Request New Certificate \(Automated\) and Renew Certificate \(Automated\) forms enable you to submit or update a Certificate Signing Request \(CSR\) to be submitted to a certificate authority.

<table id="table_lhb_ppz_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Purpose

</td><td>

Determines whether the Certificate is internal or external.-   Internal: Requires a completed form
-   External: Requires importing the CSR and private key from an external source

</td></tr><tr><td>

Environment

</td><td>

Environment where the certificate must be deployed or installed. The available options are Development, Disaster recovery, Production, or Sub-Production.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

The number of days the certificate is valid. This field appears only when External is selected from the Certificate Purpose field.

</td></tr><tr><td>

Choose how to generate CSR

</td><td>

Determines which CSR is used to generate the certificate. The available values are:-   Use external CSR
-   Generate CSR in CyberArk: Available only when CyberArk Certificate Manager SaaS is selected as the **Select how to manage your certificate** value when requesting or revoking a certificate.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

CSR sent to the external Certificate Authority \(CA\) to request the certificate.

</td></tr><tr><td>

Subject Common Name

</td><td>

Entity or domain name the certificate is issued to.

</td></tr><tr><td>

Subject Alternative Name

</td><td>

Domain or subdomain included in the Subject Common Name.

</td></tr><tr><td>

Organization

</td><td>

Organization submitting the CSR.

</td></tr><tr><td>

Organizational Unit

</td><td>

Organizational unit submitting the CSR.

</td></tr><tr><td>

Locality/City

</td><td>

Locality \(city\) of the organization submitting the CSR.

</td></tr><tr><td>

Province

</td><td>

State or province of the organization submitting the CSR.

</td></tr><tr><td>

Country

</td><td>

Country of the organization submitting the CSR.

</td></tr><tr><td>

Email Address

</td><td>

Email address of the administrator in the organization submitting the CSR.

</td></tr><tr><td>

Key Algorithm

</td><td>

Cryptographic algorithm for generating the certificate key pair, based on algorithms supported by CyberArk. The available options are RSA 1024, RSA 2048, RSA 3072, RSA 4096, EC P256, EC P384, EC P521, and EC ED25519.

</td></tr><tr><td>

Application Services

</td><td>

Application services for the certificate.

</td></tr><tr><td>

Servers

</td><td>

Servers the certificate can be hosted on.

</td></tr><tr><td>

Application Names

</td><td>

Specific application the certificate is issued for.

</td></tr><tr><td>

Application Servers

</td><td>

Application servers the certificate is hosted on.

</td></tr><tr><td>

Certificate Owner Group

</td><td>

Certificate owner group for the certificate.

</td></tr><tr><td>

Certificate Owner

</td><td>

Specific entity that the certificate is issued to.

</td></tr><tr><td>

Renewal Tracking

</td><td>

Determines whether to track certificate renewal automatically. The available options are Create priority 1 tasks, Create prioirty 3 tasks, and Do not create renewal tasks.

</td></tr><tr><td>

Renew Automatically

</td><td>

Option to automatically renew the certificate.

</td></tr><tr><td>

How many days before expiry does the certificate need to be renewed?

</td><td>

Number of days before certificate expiration to trigger renewal.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cert-invt-mgmt-references.md)

