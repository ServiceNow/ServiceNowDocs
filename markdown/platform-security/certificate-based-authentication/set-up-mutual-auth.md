---
title: Set up Certificate-based authentication
description: Set up mutual authentication for either user interface-based logins or inbound web services.You can activate the Certificate-based authentication plugin \(com.glide.auth.mutual\) for ServiceNow AI Platform if you have the admin role. Register root certificates or intermediate certificates to make them available for authentication.Map PEM certificates to users to enable them to log in using PIV or CAC cards or to authenticate inbound requests. You can map multiple PEM certificates to a user.Use system properties to enable or disable certificate-based authentication features.
locale: en-US
release: xanadu
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Certificate-based authentication, Authentication, Access Management]
---

# Set up Certificate-based authentication

Set up mutual authentication for either user interface-based logins or inbound web services.

## Before you begin

Role required: admin

Check that your instance is using an ADCv2 load balancer. For more information, see the[ADCv2 Migration knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0952875). If your instance is not using the ADCv2 load balancer, contact Now Support.

## Procedure

1.  Set up Certificate-based authentication in order to:

    -   Allow end users to securely log in to the ServiceNow AI Platform or Service Portal using PIV or CAC cards. After certificate-based authentication is enabled, you can self-register the PEM certificate or an administrator can map the certificate for you. See [Log in using Certificate-based authentication](ui-login-mutual-auth.md#).
    -   Enable mutual authentication for inbound web services. Once Certificate-based authentication is set up, the system uses the provided certificates to mutually authenticate requests to access ServiceNow REST and SOAP APIs.

## Activate Certificate-based authentication

You can activate the Certificate-based authentication plugin \(com.glide.auth.mutual\) for ServiceNow AI Platform if you have the admin role.

### Before you begin

Role required: admin.

### About this task

The following Tables are installed with Certificate-based authentication:

-   sys\_user\_certificate
-   sys\_ca\_certificate
-   sys\_ca\_certificate\_api\_track

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Certificate-based authentication plugin \(com.glide.auth.mutual\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## Register CA certificate

Register root certificates or intermediate certificates to make them available for authentication.

### Before you begin

Role required: admin

### Procedure

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


## Map PEM certificate to user

Map PEM certificates to users to enable them to log in using PIV or CAC cards or to authenticate inbound requests. You can map multiple PEM certificates to a user.

### Before you begin

-   Role required: admin
-   Make sure that you have the Privacy Enhanced Mail \(PEM\) certificate of the user.

**Note:** After the Map PEM certificate to User configuration, the "verify certificate" will fail. This is because the PEM certificate is not stored.

### Procedure

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

User who is mapped to the client certificate.The system receives the client certificate from either the inbound request or [certificate registration](ui-login-mutual-auth.md#), and then uses the user designated in this field to initiate a session to execute the request.

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


## Configure Certificate-based authentication properties

Use system properties to enable or disable certificate-based authentication features.

### Before you begin

Role required: admin

### Procedure

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
