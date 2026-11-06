---
title: Install and configure Security Incident Response integration with Zscaler
description: Install and configure the Security Incident Response integration with Zscaler internet Access product from the ServiceNow Store to start using the integration on your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/security-incident-response/install-zscaler-integration-for-security-operations.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Security Incident Response integration with Zscaler

Install and configure the Security Incident Response integration with Zscaler internet Access product from the ServiceNow Store to start using the integration on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Download the Security Incident Response integration with Zscaler product from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the Security Incident Response integration with Zscaler tile and select **Configure** &gt; **Create new configuration**.

4.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server Name

</td><td>

Zscaler server name. For example, ZSserver.

</td></tr><tr><td>

Active

</td><td>

Indicator that the profile is active.

</td></tr><tr><td>

Order

</td><td>

Flow priority. The value for this field indicates the order of the workflows when two or more profiles share triggering conditions.

 The flow with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, 300, 400.

 The default is 100.

</td></tr><tr><td>

Zscaler API URL

</td><td>

Base URL that hosts the Zscaler API. For example, `[https://example.zscalerbeta.net](https://example.zscalerbeta.net)`

</td></tr><tr><td>

Authentication Type

</td><td>

Method that ServiceNow uses to authenticate the Zscaler API.-   **Basic Auth**: Authenticates with the Zscaler Internet Access admin user name, password, and API key. This option is the default.
-   **OAuth 2.0**: Authenticates with an OAuth 2.0 Client ID, Client Secret, and Vanity Domain from Zscaler ZIdentity.


</td></tr><tr><td>

Vanity Domain \(Token Domain\)

</td><td>

Organization's ZIdentity sign-in hostname, consisting of your vanity name and the Zscaler login domain. For example, `acme + zslogin.net = acme.zslogin.net`.Required when **Authentication Type** is **OAuth 2.0**.

</td></tr><tr><td>

Client ID

</td><td>

OAuth 2.0 client ID that ServiceNow uses for Zscaler authentication.Required when **Authentication Type** is **OAuth 2.0**.

</td></tr><tr><td>

Client Secret

</td><td>

OAuth 2.0 client secret key for Zscaler authentication.Required when **Authentication Type** is **OAuth 2.0**.

</td></tr><tr><td>

User Name

</td><td>

User name for the Zscaler Internet Access admin account.Required when **Authentication Type** is **Basic Auth**.

</td></tr><tr><td>

Password

</td><td>

Password for the Zscaler Internet Access admin account.Required when **Authentication Type** is **Basic Auth**.

</td></tr><tr><td>

API Key

</td><td>

API key that you obtained from the Zscaler Internet Access administration portal.Required when **Authentication Type** is **Basic Auth**.

**Note:** **The user must have sn\_si.admin role to setup the integration.**

</td></tr></tbody>
</table>    **Note:** Configurations that you created before OAuth 2.0 support was available using Basic Auth. To switch authentication methods, change the **Authentication Type**, fill in the fields for the new method, and select **Validate and Update**.

5.  Select **Validate and Update**.

    The instance checks that the fields for the selected authentication type are filled in and then validates the connection. For OAuth 2.0, the instance requests an access token from `https://{vanity_domain}/oauth2/v1/token`.


## Result

After you validate and save this configuration, return to the Zscaler Configurations page.

