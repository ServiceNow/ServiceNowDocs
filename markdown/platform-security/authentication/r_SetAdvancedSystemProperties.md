---
title: \(Optional\) Advanced SAML properties
description: The following advanced settings allow you to further increase security and debug the integration.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# \(Optional\) Advanced SAML properties

The following advanced settings allow you to further increase security and debug the integration.

Navigate to **All** &gt; **SAML 2 Single Sign-on** &gt; **Properties**.

![](../image/AdvProperties.png "Advanced settings")

|Property|Description|
|--------|-----------|
|The number of seconds "notBefore" constraint, or after "notOnOrAfter" constraint, to consider still valid|Enter the number of seconds to add to the NotBefore and NotOnOrAfter constraints to account for time differences between the IdP clock and SP clock. These constraints prevent against replay attacks by denying requests that are not made within the specified time frame. If the IdP clock and SP clock are significantly different, network latency may result in the SAML request being unauthorized. This property adds a grace period during which SAML requests and responses are still considered valid.|
|Turn on debug logging for SAML 2.0 Authentication|Select **Yes** to enable additional logging information for SAML 2.0 events.|

