---
title: Register CA certificate
description: Register root certificates or intermediate certificates to make them available for authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/certificate-based-authentication/map-ca-cert-chain.html
release: brazil
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Certificate-based authentication, Authentication, Access Management]
---

# Register CA certificate

Register root certificates or intermediate certificates to make them available for authentication.

## Before you begin

Role required: sso\_config\_admin

## Procedure

1.  Navigate to **All** &gt; **Certificate Based Authentication** &gt; **CA Certificate Chain**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_att_rwx_c4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the certificate.

</td></tr><tr><td>

Expiration notification

</td><td>

Option to warn users when a certificate is about to expire.

</td></tr><tr><td>

Notify on expiration

</td><td>

List of users to be notified when the certificate expires.

</td></tr><tr><td>

Warn in days to expire

</td><td>

Number of days when a notification is sent to users before a certificate expires.

</td></tr><tr><td>

Active

</td><td>

Option to make the client certificate active.

</td></tr><tr><td>

Format

</td><td>

PEM

</td></tr><tr><td>

Type

</td><td>

Type of certificate. Options include:-   **CA Cert**: The root CA certificate. Can also include intermediate certificates in the chain. CA certificates are automatically synced with the load balancer. Use this option when possible to avoid missing a required certificate in the chain.
-   **Intermediate Cert**: An intermediate certificate in the certificate chain. This certificate remains on the instance only and is not synced with the load balancer. Only use this option if you need to add an intermediate certificate to an existing chain.


</td></tr><tr><td>

Short description

</td><td>

Short description of the user client certificate.

</td></tr></tbody>
</table>    **Note:** During the certificate upload, the read-only fields, **Valid from**, **Expires**, **Expires in days**, **Issuer**, and **Subject**, **Certificate Chain**, and **PEM Certificate** are extracted and auto-populated.

4.  Click **Submit**.

5.  Click **Validate Stores/Certificates** to validate the certificate.


