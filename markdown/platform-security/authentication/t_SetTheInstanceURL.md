---
title: Set the instance URL for SAML
description: Set the instance-specific URLs so that the IdP can authenticate users.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Set the instance URL for SAML

Set the instance-specific URLs so that the IdP can authenticate users.

## Before you begin

Role required: admin

## Procedure

1.  In the property The URL to the Service-now instance \(usually this instance\), enter the URL \(including login page\) of the instance for which the IdP authenticates.

    For example: https://yourinstance.service-now.com/navpage.do

2.  In the property The entity identification, or the issuer, enter the base URL \(excluding login page\) of the instance for which the IdP authenticates.

    For example: https://yourinstance.service-now.com/


