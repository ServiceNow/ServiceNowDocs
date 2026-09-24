---
title: Map PEM certificate to user
description: Map PEM certificates to users to enable them to log in using PIV or CAC cards or to authenticate inbound requests. You can map multiple PEM certificates to a user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/certificate-based-authentication/map-user-pem-certificate.html
release: brazil
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Certificate-based authentication, Authentication, Access Management]
---

# Map PEM certificate to user

Map PEM certificates to users to enable them to log in using PIV or CAC cards or to authenticate inbound requests. You can map multiple PEM certificates to a user.

## Before you begin

-   Role required: sso\_config\_admin
-   Make sure that you have the Privacy Enhanced Mail \(PEM\) certificate of the user.

**Note:** After the Map PEM certificate to User configuration, the "verify certificate" will fail. This is because the PEM certificate is not stored.

## Procedure

1.  Navigate to **All** &gt; **Certificate Based Authentication** &gt; **User to Certificate Mapping** and click **New**.

2.  On the form, fill in these fields:

<table id="table_r1h_21z_14b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user client certificate.

</td></tr><tr><td>

Expiration notification

</td><td>

Option to warn users when a certificate is about to expire.

</td></tr><tr><td>

Warn in days to expire

</td><td>

Number of days when a notification is sent to users before a certificate expires.

</td></tr><tr><td>

Notify on expiration

</td><td>

List of users to be notified when the certificate expires.

</td></tr><tr><td>

Active

</td><td>

Option to make the client certificate active.

</td></tr><tr><td>

User

</td><td>

User who is mapped to the client certificate.The system receives the client certificate from either the inbound request or [certificate registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/certificate-based-authentication/ui-login-mutual-auth.md), and then uses the user designated in this field to initiate a session to execute the request.

</td></tr><tr><td>

Short description

</td><td>

Short description of the user client certificate.

</td></tr><tr><td>

Format

</td><td>

Privacy Enhanced Mail \(PEM\) format is a base-64 encoded Distinguished Encoding Rules \(DER\) certificate.

</td></tr><tr><td>

Type

</td><td>

Client cert. This field is read only.

</td></tr></tbody>
</table>    **Note:** During the certificate upload, the read-only fields, **Valid from**, **Expires**, **Expires in days**, **Issuer**, and **Subject** are extracted and auto-populated.

3.  Click the attachments icon and upload the certificate.

4.  Click **Submit**.

    The certificate is validated and mapped to the specified user if the certificate is from a trusted Certificate Authority \(CA\).


