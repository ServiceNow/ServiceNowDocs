---
title: Determine what User table field matches the NameID token
description: Identity providers specify what format the NameID token has.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up a NameID policy for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Determine what User table field matches the NameID token

Identity providers specify what format the `NameID` token has.

## Before you begin

Role required: admin

## About this task

Setting up SAML 2.0 requires selecting a field from the User table that matches the format of the `NameID` token. Typically, IdPs offer the option to use an email address as the `NameID` token. Since the User table contains an email field, this field is a logical choice for use as a `NameID` token. To use another field from the User table as the `NameID` token, first verify that the IdP offers a `NameID` format that matches the value of a User table field. This may require adding the field to the User table.

## Procedure

1.  Compare the available formats in the IdP's `NameIDFormat` element to fields in the User table.

2.  Select a `NameID` format where there is a matching value in the User table.

3.  In the The User table field to match with the Subject's NameID element in the SAMLResponse field, enter the name of the User table field to search for matching values in the `NameID` token.

    By default, the integration uses the email field.


