---
title: Identity management integrations
description: Manage access and user profile by integrating with Identity providers and LDAP directories.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Platform module configuration, Configure, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Identity management integrations

Manage access and user profile by integrating with Identity providers and LDAP directories.

## Single sign-on \(SSO\)

![](../image/ia-sso.png)

SSO simplifies secure multi-system access using one set of credentials.

**Note:** You are required to install Multiple Provider Single Sign-On Enhanced UI plugin before creating a new SSO provider. Select the Go to Application Manager link to install the plugin.

Once the plugin is installed, the existing SSO providers show up. Select the Identity Provider link to create a new SSO provider. You can create an identity provider of one of the following types:

-   Digest
-   SAML
-   OpenID Connect

**Note:** Although the Digest type is an option, it is not supported. OIDC and SAML are the only two providers that are supported.

## Lightweight directory access protocol \(LDAP\)

![](../image/ia-ldap.png)

LDAP syncs user and group data to centralize authentication and access control.

On selecting LDAP on the left hand side panel, the gallery of the existing LDAP servers shows up. Select **Add an LDAP server** to create a new LDAP server.

**Parent Topic:**[Platform module configuration in Now Assist for Setup](ia-config-platform-il.md)

