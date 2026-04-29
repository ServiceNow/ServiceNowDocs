---
title: Set up a NameID policy for SAML
description: Set up a NameID policy for SAML. SAML 2.0 requires the IdP to exchange a NameID token with the service provider.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Provider \(SP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Set up a NameID policy for SAML

Set up a NameID policy for SAML. SAML 2.0 requires the IdP to exchange a NameID token with the service provider.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

For the SAML 2.0 integration the NameID token must map to a particular field in the User table. The integration uses the NameID token's value to determine what user the IdP authenticates.

## Procedure

1.  Browse the IdP metadata to find the `NameIDFormat` element that contains a value of `emailAddress`.

    The value of this element is the default format that the integration uses.

2.  Review other `NameIDFormat` elements to determine if there are formats that match other fields in the User table.


