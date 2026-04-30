---
title: Common IdP connection errors
description: The following table describes some of the common IdP connection errors and their solutions.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Testing IdP connections, Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Common IdP connection errors

The following table describes some of the common IdP connection errors and their solutions.

|Error messages|Solution|
|--------------|--------|
|User Field validation failed. Invalid User Field '&lt;field name&gt;' is not a field on sys\_user table.|Verify the contents of the User table field you selected matches the SAML NameID token.|
|Assertion issuer is invalid.|Verify **Identity Provider URL** contains a valid URL to your IdP. Each IdP URL must be unique.|
|AudienceRestriction validation failed.|Verify the **Audience URI** contains a valid URL to your instance.|
|Cannot logout of IdP's session.|Verify the **SingleLogoutRequest** URL contains a valid URL to your IdP's logout service.|
|Signature did not validate against the credential's key.|Verify the IdP has a valid certificate installed.|

