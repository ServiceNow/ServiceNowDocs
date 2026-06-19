---
title: Credentials error
description: Troubleshoot a credentials error that occurs while registering a target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/register-target-instance-1.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshooting for registering target instance, Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Credentials error

Troubleshoot a credentials error that occurs while registering a target instance.

## Condition

The credentials for the target instance are incorrect preventing the target instance from being registered.

## Cause

Clone requests can’t redirect authentication requests to a single sign-on identity provider. The target instance credentials must exist in the `sys_user` table as a user record or as part of a Lightweight Directory Access Protocol \(LDAP\) integration.

## Remedy

-   Provide credentials for the target instance for a user with the admin role.
-   Use a local user account, not an LDAP, or SSO user account.

**Parent Topic:**[Troubleshooting for registering target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/register-target-instance-troubleshooting.md)

