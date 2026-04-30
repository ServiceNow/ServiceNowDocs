---
title: Require authorization for XML requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.xml property to designate if incoming XML requests should require basic authentication.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for XML requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.xml** property to designate if incoming XML requests should require basic authentication.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.xml**

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

To enforce basic authentication on XML requests.

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

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of XML data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see [XML parser step](https://www.servicenow.com/docs/access?context=xml-parser-step-action-designer&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Without appropriate authorization configured on the incoming XML requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Authentication](../../../integrate/single-sign-on/concept/c_Authentication.md)

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

