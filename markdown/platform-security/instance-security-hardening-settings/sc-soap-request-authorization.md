---
title: Require authorization for SOAP requests
description: Use the glide.basicauth.required.soap property to designate if incoming SOAP requests should require basic authorization.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for SOAP requests

Use the **glide.basicauth.required.soap** property to designate if incoming SOAP requests should require basic authorization.

The **glide.basicauth.required.soap** system property controls whether basic authentication is required to make a SOAP request to an instance. If **glide.basicauth.required.soap** is not set to the recommended value of **true**, then unauthenticated users performing SOAP operations are mapped to the soap.guest user. This may enable an unauthenticated user to perform operations on the instance as if a logged in user to the instance. There may be additional impact if the user define within **com.glide.soap.guest\_user** is assigned additional roles.

Ensure that the property **glide.basicauth.required.soap** exists in the System Properties \[sys\_properties\] tableand is set to the value **true**. Alternatively, configure the instance for WS Security by setting the property **glide.soap.require\_ws\_security** to **true** and following the product documentation to configure WS Security Profiles. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.basicauth.required.soap**
-   **glide.soap.require\_ws\_security**

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

-   false
-   false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   true

</td></tr><tr><td>

Category

</td><td>

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Unauthenticated access to SOAP export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of SOAP data on the instance.
-   It restricts any guest users who are currently accessing this data.
-   Create an account for a user who needs access to this content, with the necessary access control permissions.

 To learn more, see [SOAP web service](https://www.servicenow.com/docs/access?context=c_SOAPWebService&version=australia&pubname=australia-api-reference&ft:locale=en-US) and [MID Server authentication credentials and SOAP requests](https://www.servicenow.com/docs/access?context=mid-authentication-soap-requests&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

