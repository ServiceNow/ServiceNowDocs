---
title: Client type configuration for OAuth and SSO records
description: Configure the Client Type field for OAuth and SSO record related configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/client-type.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Old inbound integrations experience, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Client type configuration for OAuth and SSO records

Configure the **Client Type** field for OAuth and SSO record related configurations.

When establishing sessions for various login types such as Web UI \(interactive login\), Iframe Embedded, Embedded or Integration, you can configure the client type for the OIDC \(OAuth Entity\), SAML, and Digest records that are used for various login.

The client type choices are as follows:

-   **Iframe Embedded**: Can be used for interactive ServiceNow instance that resides in an Iframe in the third-party websites. For example, if there is a sensitive table \(sys\_user table - phone number of the user\), as admin you can configure the ACL with the security attribute \(Iframe Embedded\) set to false, to avoid the user accessing the data \(table information\) on the Iframe Embedded session in the third party.
-   **Integration as a User**: Can be used for Virtual Agent chatbot that are installed in desktop apps such as Slack, Teams, and so on.
-   **Integration as a Service**: Can be used for machine to machine integration \(communication between services\).

**Note:**

-   For OIDC \(OAuth Entity\): All the choices are available.
-   For SAML and Digest: Only Iframe embedded. You must edit the form and add the **Client Type** field to the record and select the **Iframe Embedded** client type.
-   If the **Client Type** selected is none, then there is no classification of the session.

Use the client type field in every record created for OIDC \(OAuth Entity\), SAML, and Digest. This enables you to have a better control over each login method that has the same configurations but is distinguished by the client type.

After configuring the field, whenever a user logs in from the corresponding configuration \(OAuth or SSO\), after the authentication is successful, the session is considered based on the configured client type and accordingly the session timeout is used.

For the current session, the corresponding security attributes are included or can be used to help prevent users from accessing table specific information within the selected client type. For more information, see [OOB \(Out-of-Box\) Security Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/oob-security-attributes.md).

## Session timeout for the client types

The following system properties are related to session timeout for the various client types:

-   `glide.session_timeout.iframe_embedded`
-   `glide.session_timeout.integration_as_a_user`
-   `glide.session_timeout.integration_as_a_service`

