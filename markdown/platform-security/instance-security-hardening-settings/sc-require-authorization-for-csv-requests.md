---
title: Require authorization for csv requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.csv property to designate if incoming CSV \(Comma-Separated Values\) requests should require basic authentication.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for csv requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.csv** property to designate if incoming CSV \(Comma-Separated Values\) requests should require basic authentication.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.csv**

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

To enforce basic authentication on CSV requests.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

7.5

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control.-   It performs this authentication while retrieving data from tables/pages in the form of CSV data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see [Retrieving data from a CSV formatted file](https://www.servicenow.com/docs/access?context=t_RetrieveDataFromACSVFormatFile&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Without appropriate authorization configured on the incoming CSV requests, an unauthorized user can get access to sensitive content and data on the target instance. Ensure that **glide.basicauth.required.csv** exists in the sys\_properties table and is set to true.

</td></tr><tr><td>

References

</td><td>

[Web service security](../../security/concept/c_WebServiceSecurity.md)

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

