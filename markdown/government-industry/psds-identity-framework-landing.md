---
title: Identity Provider Integration plugin
description: The Identity Provider Integration plugin \(sn\_idp\_integ\) allows provides ServiceNow developers with the data model foundation to develop OpenID Connect \(OIDC\) integrations that authenticate and verify constituent identities through approved government OpenID Connect \(OIDC\) providers — ID.me \(US\), myID \(Australia\), GOV.UK One Login \(UK\) — replacing email-only identification. It standardizes and enhances the identity verification process, delivering a provider-neutral OIDC framework for capturing and storing key identity provider data, including identity provider issuer, identity provider ID, and assurance level from OIDC providers on top of the existing Multi-Provider SSO \(MPSSO\) plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-identity-framework-landing.html
release: brazil
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [Integrate, Public Sector Digital Services \(PSDS\)]
---

# Identity Provider Integration plugin

The Identity Provider Integration plugin \(sn\_idp\_integ\) allows provides ServiceNow developers with the data model foundation to develop OpenID Connect \(OIDC\) integrations that authenticate and verify constituent identities through approved government OpenID Connect \(OIDC\) providers — ID.me \(US\), myID \(Australia\), GOV.UK One Login \(UK\) — replacing email-only identification. It standardizes and enhances the identity verification process, delivering a provider-neutral OIDC framework for capturing and storing key identity provider data, including identity provider issuer, identity provider ID, and assurance level from OIDC providers on top of the existing Multi-Provider SSO \(MPSSO\) plugin.

Identity Provider Integration adds a new standalone table that stores OIDC identity-provider metadata for externally authenticated users. The table supports more than one identity-provider association per user over time. This enables agencies to reliably identify constituents, prevent duplicate accounts, and protect sensitive data via role-based ACLs. The model supports multiple providers per user, and enforces provenance-based write access to downstream user fields.

Two MPSSO configurations support the workflow:

-   Login Authentication Configuration — the standard "Sign in with ID.me" login flow, configured with scopes that only require self-reported user attributes,
-   Verification configuration— the "Verify with ID.me" step-up flow, configured with scopes that require remotely verified user attributes

Both Provider configurations return OIDC claims through the same MPSSO transform script, validated against the OIDC provider sandbox. The script, which runs a find-or-create logic before a new user is created from an OIDC provider login, checks if this identity already exists by searching the `sn_idp_integration` table for a Identity Provider Issuer + Identity Provider ID match, reusing the existing, verified user instead of creating a duplicate if it finds a match, or creating a new user record table entry if there's no match.

For more information about the Identity Provider Integration plugin, see [Identity Provider Integration Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-identity-framework-dm.md).

**Related topics**  


[Install Identity Provider Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-identity-framework-install.md)

