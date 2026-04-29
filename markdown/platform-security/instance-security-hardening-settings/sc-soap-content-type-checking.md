---
title: Validate SOAP content type
description: Use the glide.soap.require\_content\_type\_xml property to enable validation of a content type as text/xml and protect against invalid SOAP requests.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Validate SOAP content type

Use the **glide.soap.require\_content\_type\_xml** property to enable validation of a content type as text/xml and protect against invalid SOAP requests.

If the **glide.soap.require\_content\_type\_xml** system property is not set to the recommended value of **true**, then there is no validation for the SOAP request.

Ensure that the property **glide.soap.require\_content\_type\_xml** is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.soap.require\_content\_type\_xml**

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

-   Severity score: 8.8
-   CVSS rating: High
-   Security risk details: This lack of validation can enable Cross-Site Request Forgery \(CSRF\) attacks, allowing malicious actors to trick authenticated users into sending unauthorized SOAP requests.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enables validation of SOAP content type for all the inbound SOAP requests. -   If you are using a content type other than text/xml for inbound requests, it may cause potential failure of SOAP transactions.
-   If you are not using the correct MIME type, it could disrupt third-party integrations.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

