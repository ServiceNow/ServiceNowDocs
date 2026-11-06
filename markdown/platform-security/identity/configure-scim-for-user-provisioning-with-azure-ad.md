---
title: Configure SCIM for user provisioning with a provider
description: Configuring SCIM automatically provisions and de-provisions users and groups to ServiceNow by using the provider's provisioning service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/configure-scim-for-user-provisioning-with-azure-ad.html
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Configure SCIM for user provisioning with a provider

Configuring SCIM automatically provisions and de-provisions users and groups to ServiceNow by using the provider's provisioning service.

## Before you begin

The SCIM plugin must be installed.

Role required: scim\_admin

**Warning:** Grant this role carefully. The scim\_admin role is equivalent to giving the user the admin role, where the scim\_admin can add or update Personally Identifiable Information \(PII\).

## About this task

You can provision users using SCIM by the following authentication methods:

-   [Provision users using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/provisioning-user-basic-auth.md)
-   [Provision users using OAuth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/provisioning-user-oauth.md)

