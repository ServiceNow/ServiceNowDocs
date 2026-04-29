---
title: Require authorization for PDF requests
description: Use the glide.basicauth.required.pdf property to designate if incoming PDF requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for PDF requests

Use the **glide.basicauth.required.pdf** property to designate if incoming PDF requests should require basic authentication.

If **glide.basicauth.required.pdf** is not set to the recommended value of **true**, the Basic Authentication for PDF format export processor is disabled. This also happens when combined with a wrong role within the guest\_user related property \(For example a high privileged user such as Admin\). This leads to unauthenticated access to instance data.

Ensure the property **glide.basicauth.required.pdf** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

****

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

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: Unauthenticated access to PDF export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. -   It performs this authentication while retrieving data from tables/pages in the form of PDF data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see [Web service import sets](https://www.servicenow.com/docs/access?context=c_WebServiceImportSets&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[API and web service](sc-api-web-service.md)

