---
title: Exploring SCIM Provider
description: The Service Provider provisions users and groups using the SCIM API.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Exploring SCIM Provider

The Service Provider provisions users and groups using the SCIM API.

As a SCIM provider, the ServiceNow schemas support SCIM APIs to provision users and groups.

The SCIM provider synchronizes the changes made to identities in the IdP, including creating, updating, or deleting records. These changes are automatically synchronized to the provider according to the SCIM protocol. Also, the IdP can read identities from the provider to add to the IdP directory. The IdP can then detect incorrect values in the provider that could create security vulnerabilities. The synchronization enables end users to have seamless access to applications for which they’re assigned, with up-to-date profiles and permissions.

## Configurations for SCIM Provider

To configure the SCIM Provider, perform the following tasks:

-   Activate the **SCIM v2 - ServiceNow Cross-domain Identity Management** plugin. To learn more, see [Activating the SCIM plugin](../task/activate-scim-plugin.md).​
-   Activate the other plugins that other plugins that are required for SCIM:
    -   [OAuth 2.0](../../../administer/security/task/t_SettingUpOAuth.md)
    -   REST API Provider
    -   [REST API Access Policy​](../task/activate-rest-api-access-policy.md)
-   Add the scim\_admin role as part of the SCIM service.​

**Warning:** Grant this role carefully. The scim\_admin role is equivalent to giving the user the admin role, where the scmin\_admin can add or update Personally Identifiable Information \(PII\).

## Tables

Two tables, sys\_user and sys\_group, contain the SCIM attributes that do not map to existing ServiceNow tables. To know more about the tables, see the [SCIM-specific tables](https://www.servicenow.com/docs/access?context=scim-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

