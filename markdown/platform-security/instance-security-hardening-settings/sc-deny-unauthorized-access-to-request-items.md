---
title: Deny unauthorized access to request items \[Updated in Security Center 1.3\]
description: The glide.sc.req\_for.roles.default property defines a default behavior for the retrieveAddress API.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Deny unauthorized access to request items \[Updated in Security Center 1.3\]

The **glide.sc.req\_for.roles.default** property defines a default behavior for the retrieveAddress API.

This property is functional only when **glide.sc.req\_for.roles** has no values. If **glide.sc.req\_for.roles** has values, then this property has no significance and users with only defined roles are given access to the API.

## More information

<table><tbody><tr><td>

Attribute

</td><td>

Description

</td></tr><tr><td>

Property name

</td><td>

**glide.sc.req\_for.roles.default**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

When there are no roles given in the property, the Client Callable Script Include ScriptServiceCatalogGetLocation can be called by any unprivileged logged-in user and can retrieve the address of any other users in the system. This property protects this API to be exposed to unprivileged users.

</td></tr><tr><td>

Recommended value

</td><td>

deny

</td></tr><tr><td>

Default value

</td><td>

deny

</td></tr><tr><td>

Configuration type

</td><td>

Choicelist \(allow \| deny\)

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) If **glide.sc.req\_for.roles.default** is not set to the recommended value of **deny** \(allow\) and the value of **glide.sc.req\_for.roles** is empty, then any user can request items for other users allowing unauthorized resource access.

</td></tr><tr><td>

References

</td><td>

[Client-callable script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

