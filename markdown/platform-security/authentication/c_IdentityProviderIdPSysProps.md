---
title: Identity Provider \(IdP\) system properties
description: An IdP generally offers an XML document containing their authentication and logout metadata.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Identity Provider \(IdP\) system properties

An IdP generally offers an XML document containing their authentication and logout metadata.

For example, [SSOCircle](http://www.ssocircle.com/en/) publishes their [metadata](http://idp.ssocircle.com/) online.

Browse the IdP metadata to find these entries:

-   The `SingleSignOnService` element with a `Binding` attribute that contains a value of `HTTP-Redirect`. The `Location` attribute lists the URL the integration requires for the AuthnRequest service.
-   The `SingleLogoutService` element with a `Binding` attribute that contains a value of `HTTP-Redirect`.The `Location` attribute lists the URL the integration requires for the SingleLogoutRequest service.

**Note:** The SAML 2.0 integration only supports binding to IdP services by HTTP-Redirect.

For example:

```
<SingleSignOnServiceBinding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect"Location="https://idp.ssocircle.com:443/sso/SSORedirect/metaAlias/ssocircle"/>
```

```
<SingleLogoutServiceBinding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect"Location="https://idp.ssocircle.com:443/sso/IDPSloRedirect/metaAlias/ssocircle"ResponseLocation="https://idp.ssocircle.com:443/sso/IDPSloRedirect/metaAlias/ssocircle"/>
```

