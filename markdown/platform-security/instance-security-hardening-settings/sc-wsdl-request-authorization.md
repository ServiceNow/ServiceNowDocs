---
title: Require authorization for WSDL request
description: Use the glide.basicauth.required.wsdl property to designate if incoming WSDL \(Web Services Description Language\) requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for WSDL request

Use the **glide.basicauth.required.wsdl** property to designate if incoming WSDL \(Web Services Description Language\) requests should require basic authentication.

If **glide.basicauth.required.wsdl** system property is not set to the recommended value of **true**, then Basic Authentication for WSDL requests are disabled. WSDL is a protocol that is used to describe web services such as instance table schemas, and is not a mechanism for sharing the data within tables. Setting this property to **true** allows for disclosure of table schemas to unauthenticated users.

Ensure the property **glide.basicauth.required.wsdl** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Note:** If you choose not to require basic authentication for incoming WSDL requests, you must modify Access Control \(ACL\) rules to enable guest users to access the WSDL content.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.wsdl**

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

&lt;none&gt;

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
-   Security risk details: Unauthenticated access to WSDL Requests, when combined with misconfigured guest user role, poses a risk of unauthorized table schema exposure.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of WSDL data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

