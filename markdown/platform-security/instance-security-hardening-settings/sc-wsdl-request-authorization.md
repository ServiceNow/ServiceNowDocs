---
title: Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.basicauth.required.wsdl property to designate if incoming WSDL \(Web Services Description Language\) requests should require basic authentication.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.basicauth.required.wsdl** property to designate if incoming WSDL \(Web Services Description Language\) requests should require basic authentication.

If **glide.basicauth.required.wsdl** is not set to the recommended value of true, then , then this will disable Basic Authentication for WSDL requests. WSDL is a protocol that is used to describe web services such as instance table schemas, and is not a mechanism for sharing the data within tables. Setting this property to true allows for disclosure of table schemas to unauthenticated users.

**Note:** If you choose not to require basic authentication for incoming WSDL requests, you must modify Access Control \(ACL\) rules to enable guest users to access the WSDL content.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.wsdl**

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

To enforce basic authentication on WSDL requests.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

5.3

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of WSDL data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) Without appropriate authorization configured on the WSDL web services, an unauthorized user can get access to sensitive WSDL content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Web service security](../../security/concept/c_WebServiceSecurity.md)

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

