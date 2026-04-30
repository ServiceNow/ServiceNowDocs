---
title: Set the IdP NameID policy
description: Specify what format the IdP uses for the NameID token.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up a NameID policy for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Set the IdP NameID policy

Specify what format the IdP uses for the `NameID` token.

## Before you begin

Role required: admin

## About this task

This format is listed as part of the IdP's metadata.

## Procedure

1.  In the property The NameID policy to use for returning the Subject's NameID in the SAMLResponse. Your SAML identity provider will have to support this by declaring the policy in its metadata. The NameID value is used to match with the specified field in the User table to lookup the user., enter the value of the`NameIDFormat` element the integration uses.

    By default, the integration uses the SSOCircle `NameIDFormat` for email addresses.

2.  Click **Save**.


