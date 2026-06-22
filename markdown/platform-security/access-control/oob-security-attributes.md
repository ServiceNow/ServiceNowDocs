---
title: OOB \(Out-of-Box\) Security Attributes
description: Commonly used, generalized Security Attributes roles ready for use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/access-control/oob-security-attributes.html
release: australia
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create Security Attributes, Security Attributes, Access Management]
---

# OOB \(Out-of-Box\) Security Attributes

Commonly used, generalized Security Attributes roles ready for use.

## Overview

The OOB\(Out-of-Box\) Security Attributes are an easy way to begin using and learning the capabilities of Security Attributes with a series of preconfigured Security Attribute roles. The OOB Security Attribute roles are commonly used access control roles.

To create your own Security Attribute, or expand an OOB Security Attributes capabilities see [Compound Security Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/compound-security-attributes.md)

|Attribute|Description|
|---------|-----------|
|Group|User is member of a specified group|
|GroupExplicit|User is an explicit member of a specific group|
|HasAdminRole|User has the admin persona|
|Impersonating|User is impersonated|
|InteractiveSession|Current session interactive|
|LoggedIn|User is logged-in and authenticated|
|NetworkCriteria|Additional Network Criteria|
|Role|User has specific role|
|RoleExplicit|User has specific role explicitly defined|
|SessionIsEmbeddedGuest|Verifies whether a transaction originates from a Web Embeddables component guest session. This attribute is set as needed through the Web Embeddables capability. For more information about how Web Embeddables are configured and used, see [Configure Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/using-web-embeddables.md).|

## Security attributes for client session

Following security attributes are added for client session \(plugin: `com.glide.client_session_security_attributes`\):

-   **IsIframeEmbeddedSession**: The attribute is used in embedded iframe in third party portals. For example, Engagement messenger, Virtual Agent Web Client, Embedded Session, and so on.
-   **IsIntegrationAsAServiceSession**: The attribute is used in messaging apps like Virtual Agent in teams, Virtual Agent in slack, Virtual Agent in whatapp.
-   **IsIntegrationAsAUserSession**: The attribute is used in integration account user or web service user.
-   **Is Servicenow Web Session**: The attribute is used in web interactive session.
-   **Is Mobile App Session**: The attribute is used if the **mobile\_client** property is true in the **oauth\_entity** record.

**Note:** You must use the **IsIframeEmbeddedSession**, **IsIntegrationAsAServiceSession**, and **IsIntegrationAsAUserSession** only while configuring client type for OAuth and SSO records. To learn more, see [Configure client type for OAuth and SSO records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/client-type.md).

## Non-explicit and explicit behavior explained

Security Attributes address nuanced permission needs with an explicit vs. non-explicit \(inherited\) evaluation of roles permissions.

## Separate an IT persona access from HR role file access

We will define a Security Attribute that enables Admin to see HR related files but does not allow the Admin file access. Presume the Admin role is not defined as part of the HR group, but is \_\_\_\_\_\_\_. The **Role** sees \_\_\_\_\_\_\_

