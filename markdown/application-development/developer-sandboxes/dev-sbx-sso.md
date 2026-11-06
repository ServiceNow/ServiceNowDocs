---
title: Single sign-on for Developer Sandboxes
description: Sandboxes use the same login credentials as the base instance, including single sign-on \(SSO\) when it's enabled there. Set the required properties on the base instance so developers can use SSO to access sandboxes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/developer-sandboxes/dev-sbx-sso.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [developer sandboxes, single sign-on, SSO, sandbox login]
breadcrumb: [Install and configure, Developer Sandboxes, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Single sign-on for Developer Sandboxes

Sandboxes use the same login credentials as the base instance, including single sign-on \(SSO\) when it's enabled there. Set the required properties on the base instance so developers can use SSO to access sandboxes.

## How sandboxes authenticate users

Sandbox users log in with the same credentials as the base instance. If you use SSO on the base instance, sandboxes use the same SSO configuration, so developers don't need separate local logins for sandboxes.

**Note:** Instances with vanity URLs support SSO.

## Enabling SSO for sandboxes

Developers can access sandboxes using instance credentials and SSO.

The following properties must be set in the base instance before developers can use SSO to access sandboxes:

-   Disable ACR: `sys_property glide.sso.acr.enable = false`
-   Enable SSO: `glide.authenticate.multisso.enabled = true`

**Parent Topic:**[Developer Sandboxes installation and configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-configuring-landing.md)

