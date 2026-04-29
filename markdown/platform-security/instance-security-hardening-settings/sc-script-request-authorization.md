---
title: Require authorization for script requests
description: Use the glide.basicauth.required.scriptedprocessor property to designate if incoming script requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for script requests

Use the **glide.basicauth.required.scriptedprocessor** property to designate if incoming script requests should require basic authentication.

The **glide.basicauth.required.scriptedprocessor** system property determines whether basic auth is required to invoke a scripted processor. Any records accessed by the scripted processor still use other access controls, such as ACLs, before returning any data. If **glide.basicauth.required.scriptedprocessor** isn't set to the recommended value of **true**, then an attacker could access sensitive information such as an unauthenticated \(guest\) user attempting to access an email through the EmailDisplay sys\_processor.

Ensure the property **glide.basicauth.required.scriptedprocessor** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.scriptedprocessor**

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

-   Severity score: 7.2
-   CVSS rating: High
-   Security risk details: This property may allow unauthenticated users to invoke scripted processors, potentially exposing sensitive information despite existing ACLs.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces the authentication in the form of Basic authorization.-   It performs this authentication while processing script requests on the instance.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

