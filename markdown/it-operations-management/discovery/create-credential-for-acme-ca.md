---
title: Create credentials for ACME certificate authority
description: Create credentials so Certificate Inventory and Management can communicate with your ACME certificate authority \(CA\) for automated certificate life-cycle management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/create-credential-for-acme-ca.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Create credentials for ACME certificate authority

Create credentials so Certificate Inventory and Management can communicate with your ACME certificate authority \(CA\) for automated certificate life-cycle management.

## Before you begin

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    1.  From the credentials list, select **Certificate Management Credentials**.

    2.  On the form, fill in the fields.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the credential.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias linked to the credential.

</td></tr><tr><td>

CA Type

</td><td>

Type of the CA. The available options are:-   DigiCert
-   Entrust
-   Let's Encrypt
-   EJBCA
-   Sectigo Universal
-   Sectigo Public

**Note:** If you added an ACME-compatible CA, it is listed here as a CA type. For more information, see [Add ACME-compatible certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-acme-compatible-certificate-authorities.md).

</td></tr><tr><td>

ACME

</td><td>

Option to enable ACME flow the CA. For Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public CAs, this check box is selected by default.

</td></tr><tr><td>

Private Key

</td><td>

Create any private key or generate an account using the ACME CA. Provide a private key with the key type RSA or ECDSA.

</td></tr><tr><td>

Key Type

</td><td>

Encryption algorithm for the private key \(for example, RSA or ECDSA\).

</td></tr><tr><td>

Key ID

</td><td>

Used for account binding and is provided by the CA.

</td></tr><tr><td>

MAC Key

</td><td>

Used for account binding and is provided by the CA.

</td></tr><tr><td>

Active

</td><td>

Option to make the credential active. This check box is selected by default.

</td></tr></tbody>
</table>3.  Select **Submit**.


