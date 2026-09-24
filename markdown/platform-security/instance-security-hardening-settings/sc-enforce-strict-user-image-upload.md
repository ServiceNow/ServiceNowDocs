---
title: Enforce strict user image upload
description: Use the glide.security.strict.user\_image\_upload property to enable access control for the upload/update of a profile picture when performed on a user record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-strict-user-image-upload.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce strict user image upload

Use the **glide.security.strict.user\_image\_upload** property to enable access control for the upload/update of a profile picture when performed on a user record.

If the **glide.security.strict.user\_image\_upload** system property isn't set to **true**, the hostname and certificate chain presented by remote hosts during a TLS connection initiated from the ServiceNow ServiceNow instance aren't validated.

This vulnerability compromises the security of the TLS connection and allows person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Ensure the **com.glide.communications.httpclient.verify\_hostname** property exists and is set to `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.strict.user\_image\_upload**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: This vulnerability compromises the security of the TLS connection and allows person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.

</td></tr><tr><td>

Functional impact

</td><td>

When the **com.glide.communications.httpclient.verify\_hostname** property is set to `true`, an outbound HTTPS connection is rejected if the remote host's certificate does not match the requested hostname or its certificate chain can't be validated. Outbound integrations to hosts with a mismatched or misconfigured certificate will fail to connect once this property is set to true.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.communications.httpclient.verify\_hostname** property governs hostname and certificate chain validation independently of the **com.glide.communications.httpclient.verify\_revoked\_certificate** property, the overall gate for certificate revocation checking.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

