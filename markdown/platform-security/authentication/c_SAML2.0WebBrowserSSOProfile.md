---
title: SAML
description: The Security Assertion Markup Language \(SAML\) is an XML-based standard for exchanging authentication and authorization data between security domains.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# SAML

The Security Assertion Markup Language \(SAML\) is an XML-based standard for exchanging authentication and authorization data between security domains.

SAML exchanges security information between an identity provider \(a producer of assertions\) and a service provider \(a consumer of assertions\). SAML is a product of the OASIS Security Services Technical Committee. When implemented correctly, SAML is one of the most secure methods of single sign-on \(SSO\) available.

The [SAML 2.0](http://saml.xml.org/saml-specifications) integration enables SSO by exchanging XML tokens with an external Identity Provider \(IdP\). The IdP authenticates the user and passes a NameID token to the system. If the system finds a user with a matching NameID token \(for example, the email address\), the instance logs that user in.

If you are using the SAML 2.0 plugin for SSO authentication, you must set the glide.ui.rotate\_sessions property to false. Otherwise, it interferes with the session information sharing that takes place between the instance and the Identity Provider. Users with the security\_admin elevated privilege can access this property.

**Note:** It is recommended that customers using an existing SAML 2.0 integration upgrade to the [Multi-Provider SSO plugin.](../../single-sign-on/task/t_ActivateMultipleProviderSSO.md)

