---
title: Web Embeddables
description: Secure the web embeddables feature for authenticating the ServiceNow's web components that are used in third-party portals.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authentication, Access Management]
---

# Web Embeddables

Secure the web embeddables feature for authenticating the ServiceNow's web components that are used in third-party portals.

The web embeddables capability enables you to embed the ServiceNow web components into external websites outside ServiceNow. You can use these web components to interact with the ServiceNow using dedicated APIs that allow for real-time data exchange and functionality use without requiring users to directly access the ServiceNow interface.

While using the web embeddables, it is important to authenticate to the ServiceNow web components securely and restrict or remove high privilege roles to the users. During authentication an embedded session is established to display information from ServiceNow within the web components.

The \(`/now/client/authenticate`\) API end point is used for authenticating the request from a third-party to establish the embedded session of ServiceNow.

**Note:** You must use a dedicated `Custom URL` to authenticate the request from a third-party.

To use this end point, you need to send a valid bearer auth JWT based token in the authorization header as part of authentication request. When a valid token is sent, the session is considered as embedded with the removal of `admin` and `security admin` roles to the user.

Further, you can perform role relegation to further configure the roles that are required to be removed during an embedded session. To learn more about embedded session role configuration, see [Configure client session access role](../task/configure-client-session-access-role.md).

To know more about the configuration of web embeddables, see [Configure Web Embeddables](https://www.servicenow.com/docs/access?context=using-web-embeddables&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

By default, the policy can be configured with only **Embedded Session** filter criteria. You can leverage **Zero Trust Access \(ZTA\)** plugin to further enhance its usage with filters such as IP, Location, Role, Group, Identity Provider Attributes. You can add these filters to the policies created in the **Client Access Role Configuration** table. This ensures further strengthening the access complexity and have a better security posture while establishing an embedded session. For more information about ZTA, see [Zero Trust Access \(ZTA\)](session-access.md).

**Note:**

-   Embedded client access \(`com.glide.security.client_access`\) plugin is used for including capabilities such as role relegation for Web Embeddables feature. This plugin is auto-installed when the Web Embeddable plugin is installed.
-   You must set **glide.uxf.lib.embeddables.enabled** property to `true` for using the \(`/now/client/authenticate`\) end point.

You can also implement these additional security measures to further have a stronger control over the privileges of the user when using the web components:

-   Configure the client type to **Embedded** for the corresponding OIDC \(OAuth Entity\) record. To set the client type as **Embedded**, you must install **Zero Trust Access \(ZTA\)** plugin.
-   Use the **IsEmbeddedSession** as a security attribute for the access controls \(ACLs\). The **IsEmbeddedSession** security attribute is added when installing the Embedded client access \(`com.glide.security.client_access`\) plugin. For more information, see [OOB \(Out-of-Box\) Security Attributes](../../../administer/contextual-security/reference/oob-security-attributes.md).

