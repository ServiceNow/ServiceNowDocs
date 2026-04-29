---
title: Create the credential for the ACME Certificate Authority
description: Create an ACME credential on the ACME Certificate Authority's website or API. The credential is used by your ACME client software to interact with the ACME Certificate Authority \(CA\) to request, renew, or revoke certificates.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ACME, Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Create the credential for the ACME Certificate Authority

Create an ACME credential on the ACME Certificate Authority's website or API. The credential is used by your ACME client software to interact with the ACME Certificate Authority \(CA\) to request, renew, or revoke certificates.

## Before you begin

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  On the **What type of Credentials would you like to create?** page, select **Certificate Management Credentials**.

4.  On the form, fill in the fields.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the credential.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias that is linked to the CA credential.

</td></tr><tr><td>

CA Type

</td><td>

Type of the Certificate Authority \(for example, Let's Encrypt or Entrust\).

</td></tr><tr><td>

ACME

</td><td>

Option to enable ACME flow for the Entrust CA type.**Note:** For the CA type **Let's Encrypt**, this option is selected by default.

</td></tr><tr><td>

Private Key

</td><td>

Create any private key or generate an account using Let's Encrypt or Entrust. Provide a private key with the key type RSA or ECDSA.

</td></tr><tr><td>

Key Type

</td><td>

Encryption algorithm for the private key \(for example, RSA or ECDSA\).

</td></tr><tr><td>

Key ID

</td><td>

Used for account binding and is provided by the CA.**Note:** Applicable for CA Type **Entrust**.

</td></tr><tr><td>

MAC Key

</td><td>

Used for account binding and is provided by the CA.**Note:** Applicable for CA Type **Entrust**.

</td></tr></tbody>
</table>5.  Select **Update**.


