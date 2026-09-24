---
title: Require authorization for SOAP requests
description: Use the glide.basicauth.required.soap property to designate if incoming SOAP requests should require basic authorization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-soap-request-authorization.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for SOAP requests

Use the **glide.basicauth.required.soap** property to designate if incoming SOAP requests should require basic authorization.

The **glide.basicauth.required.soap** property controls whether basic authentication is required to make a Simple Object Access Protocol \(SOAP\) request to an instance. If the **glide.basicauth.required.soap** property is not set to **true**, unauthenticated users performing SOAP operations are mapped to the soap.guest user.

This may enable an unauthenticated user to perform operations on the instance as if a logged in user to the instance. There may be additional impact if the user define within **com.glide.soap.guest\_user** is assigned additional roles. The property **glide.soap.require\_ws\_security** \(default false\) controls whether WS-Security header validation is mandatory. When set to **false**, requests without WS-Security are allowed if other auth mechanisms \(basic auth, session\) are present.

When set to **false**, both properties allow unauthenticated SOAP requests to map to the guest user and execute without credential validation, enabling unauthorized data export and system operations.

Ensure the **glide.basicauth.required.soap** property exists and is set to **true**. Alternatively, configure the instance for Web Services \(WS\) Security by setting the **glide.soap.require\_ws\_security** property to **true** and following the product documentation to configure WS security profiles. If the property doesn't exist in the sys\_properties table, add it to the table.

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

-   true
-   false

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   false

</td></tr><tr><td>

Category

</td><td>

[API and web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: When set to **false**, both properties allow unauthenticated SOAP requests to map to the guest user and execute without credential validation, enabling unauthorized data export and system operations.

</td></tr><tr><td>

Functional impact

</td><td>

Disabling either property relaxes SOAP request authentication requirements. Basic authentication is optional or WS-Security validation is optional, allowing unauthenticated or weakly-authenticated requests to proceed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-api-web-service.md)

