---
title: Require authorization for JSONv2 request \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.jsonv2 property to designate if incoming JSONv2 requests should require basic authorization.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for JSONv2 request \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.jsonv2** property to designate if incoming JSONv2 requests should require basic authorization.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.jsonv2**

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

To enforce JSONv2 requests authorization.

</td></tr><tr><td>

Security risk rating

</td><td>

7.5

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of JSON data on the instance.
-   It restricts any guest users who are currently accessing this data.
-   Create an account for a user who needs access to this content, with the necessary access control permissions.

 To learn more, see [JSONv2 Web Service](https://www.servicenow.com/docs/access?context=c_JSONv2WebService&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) [JSONv2 Web Service](https://www.servicenow.com/docs/access?context=c_JSONv2WebService&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Without appropriate authorization configured on the data source JSON requests, an unauthorized user can access sensitive content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Authentication](../../../integrate/single-sign-on/concept/c_Authentication.md) [Requiring basic authentication for incoming JSONv2 requests](https://www.servicenow.com/docs/access?context=c_ReqBasicAuthIncomJSONv2Requ&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

