---
title: Identity management integrations
description: Manage access and user profile by integrating with Identity providers and LDAP directories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/ia-integrations-il.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Platform module configuration, Configure, Setup Hub, Get started, Administer the ServiceNow AI Platform]
---

# Identity management integrations

Manage access and user profile by integrating with Identity providers and LDAP directories.

## Single sign-on \(SSO\)

\[Omitted image "ia-sso.png"\] Alt text:

SSO simplifies secure multi-system access using one set of credentials.

**Note:** You are required to install Multiple Provider Single Sign-On Enhanced UI plugin before creating a new SSO provider. Select the Go to Application Manager link to install the plugin.

Once the plugin is installed, the existing SSO providers show up. Select the Identity Provider link to create a new SSO provider. You can create an identity provider of one of the following types:

-   Digest
-   SAML
-   OpenID Connect

**Note:** Although the Digest type is an option, it is not supported. OIDC and SAML are the only two providers that are supported.

## Lightweight directory access protocol \(LDAP\)

\[Omitted image "ia-ldap.png"\] Alt text:

LDAP syncs user and group data to centralize authentication and access control.

On selecting LDAP on the left hand side panel, the gallery of the existing LDAP servers shows up. Select **Add an LDAP server** to create a new LDAP server.

**Parent Topic:**[Platform module configuration in Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-config-platform-il.md)

