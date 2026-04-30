---
title: Multi-Provider SSO properties, tables, and scripts
description: The Integration - Multiple Provider Single Sign-On Installer plugin includes the following system properties, tables, and scripts.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Multi-Provider SSO properties, tables, and scripts

The Integration - Multiple Provider Single Sign-On Installer plugin includes the following system properties, tables, and scripts.

## Properties

Multi-Provider SSO adds the following system properties.

<table id="table_mpj_qpb_gp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.authenticate.multisso.debug**

</td><td>

Enables \(true\) or disables \(false\) debug logging for the multi-provider SSO integration.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**glide.authenticate.multisso.enabled**

</td><td>

Enables \(true\) or disables \(false\) multi-provider SSO.-   Type: true \| false
-   Default value: false

 **Note:** Setting this property to false will not disable multi-provider SSO if Account Recovery \(ACR\) is also enabled on the instance. To log in with a username and password ACR must also be disabled using the **glide.sso.acr.enabled** property. For details on this property see [Account recovery properties](acr-properties.md).

</td></tr><tr><td>

**glide.authenticate.multissov2\_feature.enabled**

</td><td>

This property determines if the MultiSSOv2 version is enabled in the instance.

</td></tr><tr><td>

**glide.authenticate.show.max.sso.login.option**

</td><td>

This property determines the maximum number of SSO options displayed on the login screen.**Note:** The default value is 5. The maximum value of the property is 10.

</td></tr><tr><td>

**glide.authenticate.show.max.sso.login.option**

</td><td>

This property determines the maximum number of IdPs displayed on the login screen. "glide.authenticate.show.max.sso.login.option" **Note:** The default value is 10.

</td></tr></tbody>
</table>## Tables

Multi-Provider SSO adds the following tables.

|Name|Description|
|----|-----------|
|SSO Properties `[sso_properties]`|Stores data for each IdP, schema, common SSO data, and so on.|
|SAML 2 Update 1 Properties`[saml2_update1_properties]`|Stores data for SAML 2.0 Update 1 configurations such as SAML certificates.|
|Digest Properties `[digest_properties]`|Stores data for digest token authentication configurations.|
|SSO Federation `[sso_federation]`|Stores data for each SSO federation.|
|OIDC Identity Provider `[oidc_identity_provider]`|Stores data for Open ID connect based identity providers.|

## Scripts

Multi-Provider SSO adds the following scripts.

|Name|Description|
|----|-----------|
|MultiSSO|Allows a customer to have an SSO type defined on a company basis.|
|MultiSSOLogin|Allows each domain to have their own login script.|
|MultiSSOLogout|Allows each domain to have their own logout script.|
|MultiSSO\_OIDC\_custom|Allows a user to define a custom Single Sign-on script for OIDC connection.|
|MultiSSO\_OIDC\_logout\_custom|Allows a user to define a custom logout script for OIDC connection.|
|MultiSSO\_Abstract\_Core|Provides a base class for all multi-provider SSO classes.|
|MultiSSO\_ClientHelper|Provides a client callable utility functions for multi-provider SSO.|
|MultiSSO\_DigestedToken|Provides a base system logic for digested token authentication.|
|MultiSSO\_SAML2\_Update1|Provides logic to process SAML 2.0 Update 1 authentication for a multi-tenant single sign-on.|

