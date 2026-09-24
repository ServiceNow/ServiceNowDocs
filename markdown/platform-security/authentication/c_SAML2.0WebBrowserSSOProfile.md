---
title: SAML
description: The Security Assertion Markup Language \(SAML\) is an XML-based standard for exchanging authentication and authorization data between security domains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/c\_SAML2.0WebBrowserSSOProfile.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# SAML

The Security Assertion Markup Language \(SAML\) is an XML-based standard for exchanging authentication and authorization data between security domains.

SAML exchanges security information between an identity provider \(a producer of assertions\) and a service provider \(a consumer of assertions\). SAML is a product of the OASIS Security Services Technical Committee. When implemented correctly, SAML is one of the most secure methods of single sign-on \(SSO\) available.

The [SAML 2.0](http://saml.xml.org/saml-specifications) integration enables SSO by exchanging XML tokens with an external Identity Provider \(IdP\). The IdP authenticates the user and passes a NameID token to the system. If the system finds a user with a matching NameID token \(for example, the email address\), the instance logs that user in.

**Note:** Banner alerts are displayed on the instance when SAML SP signing or encryption keystores are approaching or past their expiry date. There are two separate banners — one for signing certificates and one for encryption certificates — each linking to a dedicated customer action in Security Center.

If you're using the SAML 2.0 plugin for SSO authentication, you must set the **glide.ui.rotate\_sessions** property to `false`. Otherwise, it interferes with the session information sharing that takes place between the instance and the Identity Provider. Users with the security\_admin elevated privilege can access this property.

**Note:** You can use an existing SAML 2.0 integration upgrade to the [Multi-Provider SSO plugin.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/t_ActivateMultipleProviderSSO.md)

**Related topics**  


[SAML 2.0 concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/c_SAMLConcepts.md)

[SAML 2.0 configuration using Multi-Provider SSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/t_CreateASAML2Upd1SSOConfigMultiSSO.md)

