---
title: Require authorization for unload requests
description: Use the glide.basicauth.required.unl \(useUnloadFormat\) property to designate if incoming unload requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for unload requests

Use the **glide.basicauth.required.unl** \(useUnloadFormat\) property to designate if incoming unload requests should require basic authentication.

The **glide.basicauth.required.unl** system property performs authentication while retrieving data from tables/pages in the form of unload data on the instance. If **glide.basicauth.required.unl** isn't set to the recommended value of **true**, then the Basic Authentication for the UNL format export processor is disabled. This also could be combined with a wrong role within the guest\_user related property, this will lead to unauthenticated access to instance data.

Ensure the property **glide.basicauth.required.unl** exists in the System Properties \[sys\_properties\] table and is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.unl**

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
-   Security risk details: This property may allow unauthenticated access to unload data exports, especially when combined with misconfigured guest user roles, creating a serious risk of unauthorized exposure of instance configuration and data.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. It performs this authentication while retrieving data from tables/pages in the form of unload data on the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

