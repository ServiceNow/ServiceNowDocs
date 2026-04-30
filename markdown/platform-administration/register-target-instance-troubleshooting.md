---
title: General guidelines for registering target instance
description: A reference topic that includes general guidelines to fix errors that occur while registering a target instance.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# General guidelines for registering target instance

A reference topic that includes general guidelines to fix errors that occur while registering a target instance.

When registering a target instance, consider the following guidelines.

<table id="table_ryh_mhy_5gc"><thead><tr><th>

Error Type

</th><th>

Guidelines

</th></tr></thead><tbody><tr><td>

Credentials

</td><td>

-   Provide credentials for the target instance for a user with the admin role.
-   Use a local user account, not an LDAP \(Lightweight Directory Access Protocol\), or SSO \(single sign-on\) user account.

**Note:** Clone requests can’t redirect authentication requests to a single sign-on identity provider. The target instance credentials must exist in the `sys_user` table as a user record or as part of an LDAP integration.


</td></tr><tr><td>

System property

</td><td>

Verify the system property `glide.db.clone.allow_clone_target` is set to `True`. **Note:** By default, this property is enabled on instances whose name ends in Dev, Test, Stage, UAT, or QA.

</td></tr><tr><td>

IP authentication error

</td><td>

If the target instance uses IP range based authentication, it must enable the IP range `10.0.0.0/10.255.255.255` to communicate on a local network.

</td></tr></tbody>
</table>**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)

