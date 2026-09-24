---
title: Configure Certificate-based authentication properties
description: Use system properties to enable or disable certificate-based authentication features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/certificate-based-authentication/configure-certificate-authentication.html
release: brazil
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Certificate-based authentication, Authentication, Access Management]
---

# Configure Certificate-based authentication properties

Use system properties to enable or disable certificate-based authentication features.

## Before you begin

Role required: sso\_config\_admin

## Procedure

1.  Navigate to **All** &gt; **Certificate Based Authentication** &gt; **Properties**.

2.  On the form, fill in the fields:

<table id="table_fh4_vb1_b4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable certificate based authentication

</td><td>

Option to enable to Certificate-based authentication for both user interface logins and inbound web services.Default: true

**Note:** On the Portal pages, use the Form Layout to add the field to the form and then enable the property.

</td></tr><tr><td>

Show 'Log in with PIV/CAC' option in login screen

</td><td>

Displays the **Log in with PIV/CAC card** option on the login screen. Allows users to log in using Certificate-based authentication using the user interface.Default: false

</td></tr><tr><td>

Enable auto-redirect for certificate based login

</td><td>

Determines whether to require that the user click **Log in with PIV/CAC card** after selecting a registered certificate and entering their PIN. Activate to automatically log in the user after they select a registered client certificate and enter their PIN. Deactivate to require that the user click **Log in with PIV/CAC card** after they select a registered client certificate and enter their PIN.Default: false

</td></tr></tbody>
</table>
