---
title: Certificate Routing Policy form for ACME
description: Fill in the Certificate Routing Policy form to set up the routing policy for ACME.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/certificate-routing-policy-field-values.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Routing Policy form for ACME

Fill in the Certificate Routing Policy form to set up the routing policy for ACME.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the routing policy.

</td></tr><tr><td>

Certificate Authority

</td><td>

Certificate Authority \(CA\) used to create, renew, or revoke certificates. The available options are:-   DigiCert
-   Entrust
-   Let's Encrypt
-   EJBCA
-   Sectigo Public ACME
-   Sectigo Universal ACME

**Note:** If you added an ACME-compatible CA, it is listed here as a CA type. For more information, see [Add ACME-compatible certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-acme-compatible-certificate-authorities.md).

</td></tr><tr><td>

Certificate Authority API URL

</td><td>

For DigiCert CA, the API URL to handle automated processes and revocation flows.

</td></tr><tr><td>

Assignment Group

</td><td>

Group to which a manual certificate task is assigned.

</td></tr><tr><td>

DNS Challenge Action

</td><td>

Flow designer option to resolve DNS challenges automatically \(for example, base script - **ACME DNS Challenge - GoDaddy**\).**Note:** You can also create a new action similar to the base script to support any other DNS provider. The flow\_designer role or action\_designer role is required for this action.

If **None** is selected, then the new or renew certificates are done using ACME manual flow of DNS challenge.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias linked to the CA credential.

</td></tr><tr><td>

Vault Type

</td><td>

External vault provider to use for private key storage with this routing policy. When set to HashiCorp Vault, the system stores private keys in the HashiCorp vault during automated certificate operations.

</td></tr><tr><td>

Certificate Purpose

</td><td>

Indicates whether the certificate request is for an internal or external purpose.

</td></tr><tr><td>

Certificate Format

</td><td>

Format in which the certificate is generated. The available options are: PEM, DER, and PKCS12. The default value is PEM.

</td></tr><tr><td>

PKCS12 Password Vault Reference

</td><td>

Reference to the PKCS\#12 key store password stored in your external vault. For HashiCorp Vault, enter the full path to the secret. This field is required when the Certificate Format field is set to PKCS12.

</td></tr><tr><td>

PKCS12 Password Vault Key

</td><td>

Name of the key within the vault secret that holds the PKCS\#12 key store password. This field is required when the Certificate Format field is set to PKCS12 and the Vault Type field is set to HashiCorp Vault.

</td></tr><tr><td>

Allow validity override

</td><td>

For DigiCert ACME, Sectigo Public ACME, and Sectigo Universal ACME CAs, option to include a custom certificate validity period in the ACME order sent to the CA. When selected, the system sends the requested validity period \(notAfter\) to the CA. When cleared, the system omits the validity period and the CA applies its default validity. This check box is selected by default.**Note:** Clear this check box if the CA profile rejects client-requested validity.

</td></tr><tr><td>

Task Approval Group

</td><td>

Group to which the task approval is assigned.

</td></tr><tr><td>

DNS Task Assignment Group

</td><td>

Group to which the DNS challenge for this task is assigned.

</td></tr><tr><td>

Mid Server

</td><td>

MID Server for certificate actions.

</td></tr><tr><td colspan="2">

**Note:**

The **Organization**, **Organizational Unit**, **Locality**, **State**, **Country**, and **Email Address** fields accept comma-separated values. The **Subject Common Name** and **Subject Alternative Name** fields take regex expressions. The regex format has the following restrictions:

-   Shouldn’t contain commas.
-   Shouldn’t start or end with a forward slash \(/\).

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-invt-mgmt-references.md)

