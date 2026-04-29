---
title: Require authorization for csv requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.csv property to designate if incoming CSV \(Comma-Separated Values\) requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for csv requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.csv** property to designate if incoming CSV \(Comma-Separated Values\) requests should require basic authentication.

## More information

If the **glide.basicauth.required.csv** system property isn't set to the recommended value of **true**, then Basic Authentication for CSV format export processor is disabled. This also happens when combined with a wrong role within the guest\_user related property \(Ex: high privileged role\). This will lead to unauthenticated access to instance data.

Ensure the property **glide.basicauth.required.csv** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.csv**

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
-   Security risk details: Unauthenticated access to CSV export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control.-   It performs this authentication while retrieving data from tables/pages in the form of CSV data on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see [Retrieving data from a CSV formatted file](https://www.servicenow.com/docs/access?context=t_RetrieveDataFromACSVFormatFile&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

