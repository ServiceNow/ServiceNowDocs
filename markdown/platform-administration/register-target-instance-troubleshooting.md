---
title: Troubleshooting for registering target instance
description: A reference topic that includes troubleshooting to try to resolve errors that occur while registering a target instance.Troubleshoot a credentials error that occurs while registering a target instance.Troubleshoot a system property error that occurs while registering a target instance.Troubleshoot a IP authentication error that occurs while registering a target instance
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer]
---

# Troubleshooting for registering target instance

A reference topic that includes troubleshooting to try to resolve errors that occur while registering a target instance.

When registering a target instance, consider the following guidelines.

**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)

## Credentials error

Troubleshoot a credentials error that occurs while registering a target instance.

### Condition

The credentials for the target instance are incorrect preventing the target instance from being registered.

### Cause

Clone requests can’t redirect authentication requests to a single sign-on identity provider. The target instance credentials must exist in the `sys_user` table as a user record or as part of a Lightweight Directory Access Protocol \(LDAP\) integration.

### Remedy

-   Provide credentials for the target instance for a user with the admin role.
-   Use a local user account, not an LDAP, or SSO user account.

## System property error

Troubleshoot a system property error that occurs while registering a target instance.

### Condition

By default, `glide.db.clone.allow_clone_target` is enabled on instances whose name ends in Dev, Test, Stage, UAT, or QA. An error occurs if the property isn't set to `True`.

**Note:** If it's a production instance, set this property back to `False` to avoid accidental clones over production in future.

### Cause

The `glide.db.clone.allow_clone_target` system property is set to `False`.

### Remedy

### Procedure

1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

2.  Search for `glide.db.clone.allow_clone_target` in the system properties list.

3.  Select the property.

4.  If the value is set to `False`, set the value to `True`.

5.  Select **Update**.


## IP authentication error

Troubleshoot a IP authentication error that occurs while registering a target instance

### Condition

A failure to authenticate an IP address prevents the target instance from being registered.

### Cause

The IP address for the target instance is outside of the IP range.

### Remedy

If the target instance uses IP range based authentication, it must enable the IP range `10.0.0.0/10.255.255.255` to communicate on a local network. See [IP range based authentication](https://www.servicenow.com/docs/access?context=c_IPRangeBasedAuthentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

