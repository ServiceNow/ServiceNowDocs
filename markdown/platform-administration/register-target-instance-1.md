---
title: Credentials error
description: Troubleshoot a credentials error that occurs while registering a target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/register-target-instance-1.html
release: australia
topic_type: topic
last_updated: "2026-08-31"
reading_time_minutes: 1
breadcrumb: [Troubleshooting for registering target instance, Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Credentials error

Troubleshoot a credentials error that occurs while registering a target instance.

## Condition

The credentials for the target instance are incorrect preventing the target instance from being registered.

## Cause

Starting with Australia Patch 5, clone requests can redirect authentication requests to a single sign-on identity provider. This applies when both the source and target instances are on Australia Patch 5 or later.

For instances on earlier releases, the target instance credentials must exist in the `sys_user` table. The credentials can be a user record or part of a Lightweight Directory Access Protocol \(LDAP\) integration.

## Remedy

-   Provide credentials for the target instance for a user with the admin role.
-   If using OAuth authentication, verify that the OAuth configuration is correct and that the OAuth provider is accessible from both instances.

**Parent Topic:**[Troubleshooting for registering target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/register-target-instance-troubleshooting.md)

