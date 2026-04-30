---
title: Configure client type for OAuth and SSO records
description: Configure the Client Type field for OAuth and SSO record related configurations.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Old inbound integrations experience, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Configure client type for OAuth and SSO records

Configure the **Client Type** field for OAuth and SSO record related configurations.

When establishing sessions for various login types such as Web UI \(interactive login\), Iframe Embedded, Embedded or Integration, you can configure the client type for the OIDC \(OAuth Entity\), SAML, and Digest records that are used for various login.

The client type choices are as follows:

-   **Iframe Embedded**: Can be used for interactive ServiceNow instance that resides in an Iframe in the third party websites. For example, if there is a sensitive table \(sys\_user table - phone number of the user\), as admin you can configure the ACL with the sec attribute \(Iframe Embedded\) set to false, to avoid the user accessing the data \(table information\) on the Iframe Embedded session in the third-party.
-   **Integration as a User**: Can be used for Virtual Agent chat bot that are installed in desktop apps such as Slack, Teams etc.
-   **Integration as a Service**: Can be used for machine to machine integration \(communication between services\).

**Note:**

-   For OIDC \(OAuth Entity\): All the choices are available.
-   For SAML and Digest: Only Iframe embedded. You must edit the form and add the **Client Type** field to the record and select the **Iframe Embedded** client type.
-   If the **Client Type** selected is none, then there is no classification of the session.

It is recommended to use client type field to every records created for OIDC \(OAuth Entity\), SAML, and Digest. This enables you to have a better control over each login methods that has the same configurations but distinguished with the client type.

After configuring the field, whenever a user logs in from the corresponding configuration \(OAuth or SSO\), once the authentication is successful, the session is considered based on the configured client type and accordingly the session timeout is leveraged.

For the current session, the corresponding security attribute are included or can be leveraged to prevent users from accessing table specific information within the selected client type. For more information, see [OOB \(Out-of-Box\) Security Attributes](../../../administer/contextual-security/reference/oob-security-attributes.md).

## Session time out for the Client Types

Following are the system properties related to session time out for the various client types:

-   `glide.session_timeout.iframe_embedded`
-   `glide.session_timeout.integration_as_a_user`
-   `glide.session_timeout.integration_as_a_service`

