---
title: Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: Use the glide.basicauth.required.soap property to designate if incoming SOAP requests should require basic authorization.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]

Use the **glide.basicauth.required.soap** property to designate if incoming SOAP requests should require basic authorization.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.basicauth.required.soap****glide.soap.require\_ws\_security**

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

To enforce soap requests authorization.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of SOAP data on the instance.
-   It restricts any guest users who are currently accessing this data.
-   Create an account for a user who needs access to this content, with the necessary access control permissions.

 To learn more, see [SOAP web service](https://www.servicenow.com/docs/access?context=c_SOAPWebService&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) and [MID Server authentication credentials and SOAP requests](https://www.servicenow.com/docs/access?context=mid-authentication-soap-requests&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) Without appropriate authorization configured on the data source SOAP requests, an unauthorized user can access sensitive content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Authentication](../../../integrate/single-sign-on/concept/c_Authentication.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[API and web service](sc-api-web-service.md)

