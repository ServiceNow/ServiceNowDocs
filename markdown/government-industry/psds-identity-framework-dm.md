---
title: Identity Provider Integration Data Model
description: The Identity Provider Integration \(sn\_idp\_integ\) plugin provides ServiceNow developers the data model foundation to develop OpenID Connect \(OIDC\) integrations to authenticate and verify constituent identities through approved government OIDC providers — ID.me \(US\), myID \(Australia\), GOV.UK One Login \(UK\) — replacing email-only identification. The Identity Provider Integration standardizes and enhances the identity verification process, delivering a provider-neutral OIDC framework for capturing and storing identity provider data, including identity provider issuer, identity provider ID, and assurance level from OIDC providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-identity-framework-dm.html
release: brazil
topic_type: reference
last_updated: "2026-10-02"
reading_time_minutes: 3
breadcrumb: [Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Identity Provider Integration Data Model

The Identity Provider Integration \(sn\_idp\_integ\) plugin provides ServiceNow developers the data model foundation to develop OpenID Connect \(OIDC\) integrations to authenticate and verify constituent identities through approved government OIDC providers — ID.me \(US\), myID \(Australia\), GOV.UK One Login \(UK\) — replacing email-only identification. The Identity Provider Integration standardizes and enhances the identity verification process, delivering a provider-neutral OIDC framework for capturing and storing identity provider data, including identity provider issuer, identity provider ID, and assurance level from OIDC providers.

## Tables installed with Identity Provider Integration

The Identity Provider Integration data model contains the `sn_idp_integration` table, which references the `sys_user` core table. The model supports multiple providers per user, enforces provenance-based downstream field locking, and aligns with global OIDC terminology. These fields use standard, provider-neutral OIDC terminology for consistency across identity providers.

<table id="table_nzg_qfs_tkc"><tbody><tr><td>

**Name**

</td><td>

**Type**

</td><td>

**Definition**

</td><td>

**Example**

</td></tr><tr><td>

user

</td><td>

Reference \(sys\_user\)

</td><td>

Matches and identifies the platform user associated with identity-provider account

</td><td>

John.doe@gmail.com

</td></tr><tr><td>

identity\_provider\_issuer

</td><td>

String \(255\)

</td><td>

OIDC iss claim. Identifies the external IdP namespace

</td><td>

https://identity.example.gov

</td></tr><tr><td>

identity\_provider\_id

</td><td>

String \(255\)

</td><td>

OIDC sub claim. Unique identifier within the issuer namespace

</td><td>

9f3c7d13...c297

</td></tr><tr><td>

identity\_assurance\_level

</td><td>

Choice

</td><td>

Globalized assurance tier mapped from provider-specific values

</td><td>

IAL1, IAL2, IAL3

</td></tr><tr><td>

active

</td><td>

True/False

</td><td>

Marks the constituent’s current identity-provider association when more than one exists

</td><td>

true

</td></tr></tbody>
</table>## Roles

Identity administrators hold the `identity_admin` role, and caseworkers or other agents who need audit access hold the `agent` role. The `integration` role can be granted only to the MPSSO transform service account.

<table id="table_psds_idp_roles"><thead><tr><th>

Role

</th><th>

Grants

</th></tr></thead><tbody><tr><td>

identity\_admin\[sn\_idp\_integration.identity\_admin\]

</td><td>

Standard read access to identity-provider records, for admins who manage identity-provider configuration.

</td></tr><tr><td>

agent, record owner\[sn\_idp\_integration.agent\]

</td><td>

Standard read access to identity-provider records, for caseworkers or agents who need it to audit or investigate a constituent's identity.

</td></tr><tr><td>

integration \[sn\_idp\_integration.integration\]

</td><td>

Write access to the identity table. Granted only to the OIDC provider MPSSO transform service account. This is the only role granted write access to these fields \(and their downstream claim-mapped copies on `csm_consumer_user`, `csm_consumer`, `sn_gsm_constituent_profile`, that are also populated by the configured identity provider\).

</td></tr></tbody>
</table>## Access Control Lists \(ACLs\)

The `sn_idp_integration` table uses provenance-based access controls to avoid unauthorized read access to sensitive identity provider data, and to restrict write access to identity data to the MPSSO transform’s service account only.

| |Access|Roles|
|---|------|-----|
|sn\_idp\_integration: all fields|Read|sn\_idp\_integration.identity\_admin, sn\_idp\_integration.agent, record owner|
|sn\_idp\_integration: all fields|Write|sn\_idp\_integration.integration|
|Downstream claim-mapped fields `csm_consumer_user`, `csm_consumer`, `sn_gsm_constituent_profile`|Write|sn\_idp\_integration.integration|

The `sn_idp_integration` table is owned by the integration: every record is created and updated by the MPSSO transform’s service account, and write access is not granted to any human user. The configured OIDC identity provider has the sole write access for the downstream fields it populates \(existing fields on the linked `csm_consumer_user`, `csm_consumer`, and `sn_gsm_constituent_profile` records that may receive identity-provider claims\). Once they have been populated at the constituent’s achieved assurance level by the identity-provider integration, those fields become read-only to human users.

Fields that are not populated by the configured identity provider maintain their normal read/write behavior. In addition, fields maintain their normal read/write behavior when identity-provider verification isn't configured so constituent identities can still be verified through existing mechanisms.

## Identity Assurance Levels

The `sn_idp_integration` table is shipped with a globalized IAL1–IAL3 identity assurance model, mapped from provider-specific values. After a user logs in and consents to identity verification by the configured identity provider, the strength of identity, or assurance level, rises from IAL1 to IAL2, and higher-assurance, verified field values override lower-assurance ones. Once populated and verified by the identity-provider, these fields are moved to read-only.

**Parent Topic:**[Public Sector Digital Services Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/public-sector-digital-services-data-model.md)

