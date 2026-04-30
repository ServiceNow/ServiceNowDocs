---
title: Integrating with Adobe Cloud
description: Integrate your Software Asset Management application with Adobe Cloud services to track your software subscriptions and to determine your license compliance.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with Adobe Cloud

Integrate your Software Asset Management application with Adobe Cloud services to track your software subscriptions and to determine your license compliance.

The Adobe Cloud integration supports the following Adobe Cloud services:

-   Adobe Creative Cloud
-   Adobe Experience Cloud
-   Adobe Document Cloud

**Note:** You can create an Adobe Cloud integration only if you’re using the Adobe Creative Cloud for Enterprise subscription plan. If you’re using any other subscription plan, such as Adobe Creative Cloud for Teams, Education, or Individuals, you can’t create an integration.

Integrate your Adobe subscriptions with Software Asset Management for compliance reporting using Adobe authentication. For more information about Adobe authentication integrations and certificates, see the [Adobe Authentication Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/).

You can integrate your ServiceNow® instance with Adobe Cloud services using either of the following authentication methods:

-   [Service Account \(JWT\) credential](integrate-adobe-cloud-jwt.md#)
-   [OAuth Server to Server credential](integrate-adobe-cloud-oauth.md#)

**Note:** All new Adobe Cloud integrations must be created using the OAuth authentication type. Adobe is migrating from Service Account \(JWT\) credential to OAuth Server-to-Server credential. For more details, see [Adobe Migration Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Adobe Cloud application|Authentication scopes|
|-------|-------------------------------------------------|---------------------|
|Download subscriptions|System administrator|None|

