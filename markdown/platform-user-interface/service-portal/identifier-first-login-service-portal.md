---
title: Enable identifier-first login in Service Portal
description: Service Portal uses an identifier-first login \(IFL\) authentication method where the authentication path is determined by the username or email entered. The path is evaluated against configured IFL policies. IFL takes precedence over any identity provider or local login options configured for the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/identifier-first-login-service-portal.html
release: brazil
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable identifier-first login in Service Portal

Service Portal uses an identifier-first login \(IFL\) authentication method where the authentication path is determined by the username or email entered. The path is evaluated against configured IFL policies. IFL takes precedence over any identity provider or local login options configured for the portal.

## Before you begin

-   The multi-provider SSO plugin is installed and activated on your instance. For more information, see [Multi-Provider single sign-on \(SSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_MultipleProviderSingleSignOn.md).
-   IFL policies are configured on your platform instance. For more information, see [Policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/next-gen-login-experience.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select a portal to apply the identifier-first login authentication.

3.  In the **Authentication Settings** section, select **Enable portal-specific authentication**.

4.  Select **Identifier first login**.

    **Note:** The identifier-first login field appears when the multi-provider SSO plugin is active. If this field is not visible, confirm that the multi-provider SSO plugin is installed and enabled on your instance.

5.  Clear conflicting login options such as local login and portal identity provider.

6.  Select **Update**.

    **Note:** If a login widget for a portal is customized or copied, manually update the login widget with the IFL changes or revert to the original login widget.


## Result

When accessing the portal login page with IFL applied, a username/email entry field appears first. Only the IFL configuration is applied to the portal.

**Parent Topic:**[Managing portal access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/service-portal/portal-security.md)

