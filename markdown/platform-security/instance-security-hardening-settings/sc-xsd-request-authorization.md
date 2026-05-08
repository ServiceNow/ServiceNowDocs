---
title: Require Authorization for XSD Requests
description: Use the glide.basicauth.required.xsd property to designate if incoming XSD \(XML Schema Definition\) requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require Authorization for XSD Requests

Use the **glide.basicauth.required.xsd** property to designate if incoming XSD \(XML Schema Definition\) requests should require basic authentication.

The **glide.basicauth.required.xsd** system property controls whether authentication is required in order to make a XSD request to an instance. If **glide.basicauth.required.xsd** is not set to the recommended value of **true**, then authentication is disabled for XSD requests on the instance.

Ensure the property **glide.basicauth.required.xsd** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.xsd**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

&lt;None&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS rating: Medium
-   Security risk details: This property allows unauthenticated access to XSD processor leaking sensitive information.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of XSD data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see Non-interactive sessions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

