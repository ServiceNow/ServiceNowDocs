---
title: Enable early redirection
description: Enable early redirection to redirect authentication to identifier-first login or a portal identity provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/enable-early-redirection.html
release: brazil
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Service Portal early redirection]
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable early redirection

Enable early redirection to redirect authentication to identifier-first login or a portal identity provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select a portal to apply the early redirection.

3.  Select **Enable early redirection**.

    **Note:** Ensure that any custom redirection logic in the login widget is also implemented in the sp\_sso\_early\_redirection.xml UI Macro.

4.  Select **Update**.


**Parent Topic:**[Managing portal access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/service-portal/portal-security.md)

