---
title: Require authorization for script requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.scriptedprocessor property to designate if incoming script requests should require basic authentication.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for script requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.scriptedprocessor** property to designate if incoming script requests should require basic authentication.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.scriptedprocessor**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Purpose

</td><td>

To enforce basic authentication on scripts requests.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

7.2

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation enforces the authentication in the form of Basic authorization.-   It performs this authentication while processing script requests on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Without appropriate authorization configured on the incoming script requests, an unauthorized user access sensitive content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Authentication](../../../integrate/single-sign-on/concept/c_Authentication.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[API and web service](sc-api-web-service.md)

