---
title: Validate SOAP content type \[Updated in Security Center 1.3\]
description: Use the glide.soap.require\_content\_type\_xml property to enable validation of a content type as text/xml and protect against invalid SOAP requests.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Validate SOAP content type \[Updated in Security Center 1.3\]

Use the **glide.soap.require\_content\_type\_xml** property to enable validation of a content type as text/xml and protect against invalid SOAP requests.

-   When set to **true**, the ServiceNow AI Platform validates the content type as text/xml and protects against invalid SOAP requests.
-   If set to **false**, any content-type value is allowed.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.soap.require\_content\_type\_xml**

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

Protect against invalid SOAP requests

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enables validation of SOAP content type for all the inbound SOAP requests. -   If you are using a content type other than text/xml for inbound requests, it may cause potential failure of SOAP transactions.
-   If you are not using the correct MIME type, it could disrupt third-party integrations.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) When accepting inbound SOAP requests, the appropriate validation is performed to ensure that the relevant content type is being defined as a part of the request. It restricts the invalid SOAP responses that can be viewed as a security risk.

</td></tr><tr><td>

Reference

</td><td>

[Content types](https://www.servicenow.com/docs/access?context=c_ContentTypes&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[API and web service](sc-api-web-service.md)

