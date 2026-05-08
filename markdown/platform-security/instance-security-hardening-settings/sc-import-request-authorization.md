---
title: Require authorization for import requests
description: Use the glide.basicauth.required.importprocessor property to designate if incoming import requests should require basic authentication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for import requests

Use the **glide.basicauth.required.importprocessor** property to designate if incoming import requests should require basic authentication.

The **glide.basicauth.required.importprocessor** system property performs this authentication while importing data sources into the instance tables/pages.

It restricts any guest users who are currently accessing this data. If **glide.basicauth.required.importprocessor** isn't set to the recommended value of **true**, then unauthenticated users could access import processor. Additional access controls, such as ACLs, are still enforced, but this value allows a guest user import request to be processed and not summarily denied.

Ensure that the property **glide.basicauth.required.importprocessor** exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.importprocessor**

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
-   Security risk details: This property may allow unauthenticated users to initiate import requests via the import processor, potentially bypassing initial authentication checks and increasing the risk of unauthorized data manipulation despite enforced ACLs.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control.-   It performs this authentication while importing data sources into the instance tables/pages.
-   It restricts any guest users who are currently accessing this data. If applicable, you may need to create a new account for users who need access to this content, with necessary access control permissions.

 To learn more, see Retrieving data from a CSV formatted file.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

