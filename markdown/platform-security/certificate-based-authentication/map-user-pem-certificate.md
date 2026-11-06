---
title: Map PEM certificate to user
description: Map Privacy Enhanced Mail \(PEM\) certificates to users to enable them to log in using personal identity verification \(PIV\) or Common Access Card \(CAC\) or to authenticate inbound requests. You can map multiple PEM certificates to a user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/certificate-based-authentication/map-user-pem-certificate.html
release: australia
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Certificate-based authentication, Authentication, Access Management]
---

# Map PEM certificate to user

Map Privacy Enhanced Mail \(PEM\) certificates to users to enable them to log in using personal identity verification \(PIV\) or Common Access Card \(CAC\) or to authenticate inbound requests. You can map multiple PEM certificates to a user.

## Before you begin

-   Role required: sso\_config\_admin
-   The Privacy Enhanced Mail \(PEM\) certificate of the user must be available.

**Note:** After the Map PEM certificate to User configuration, the "verify certificate" fails. This is because the PEM certificate is not stored.

## Procedure

1.  Navigate to **All** &gt; **Certificate Based Authentication** &gt; **User to Certificate Mapping** and select **New**.

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

User who is mapped to the client certificate.The system receives the client certificate from either the inbound request or [certificate registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/certificate-based-authentication/ui-login-mutual-auth.md), and then uses the user designated in this field to initiate a session to execute the request.

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

Client cert.

</td></tr></tbody>
</table>    **Note:** During the certificate upload, the read-only fields, **Valid from**, **Expires**, **Expires in days**, **Issuer**, and **Subject** are extracted and auto-populated.

3.  Select the attachments icon and upload the certificate.

4.  Select **Submit**.

    The certificate is validated and mapped to the specified user if the certificate is from a trusted Certificate Authority \(CA\).


