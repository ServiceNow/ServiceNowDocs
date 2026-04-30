---
title: Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]
description: Use the glide.set\_x\_frame\_options property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]

Use the **glide.set\_x\_frame\_options** property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages.

Use the X-Frame-Options HTTP response header to indicate whether browser should be allowed to render a page in a `<frame>` or `<iframe>`. Sites can use this function to avoid clickjacking attacks by ensuring that their content is not embedded into other sites. An attacker could embed your page into their own page and make your page elements perform maliciously. The end user may think the page is legitimate because it resembles your page. The end user may click on elements like usual only to have malicious scripts or elements run.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.set\_x\_frame\_options**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Purpose

</td><td>

To mitigate against ClickJacking attacks.

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

7.1

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation enforces the restriction for rendering a ServiceNow AI Platform application in a third-party application in the form of an iFrame. If you have such an integration, the application wouldn't render in the customized third-party app.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) The Same Origin policy enables you to restrict a domain from retrieving a script or a resource from another domains. All modern browsers support this functionality. The policy validates the connection based on protocol, port, and host. CORS \(Cross Origin Request\) is a modification to Same Origin Policy that enables access to resources/scripts from another domain when explicitly stated as a part of header value.

-   In this case, the X-Frame-Options header controls whether the ServiceNow AI Platform application can be rendered on the third-party website.
-   It reduces the sensitive exposure, because the property value, when set to **SAMEORIGIN** doesn't enable the rendering to happen.

</td></tr><tr><td>

References

</td><td>

[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

 [Configure iFrames](https://www.servicenow.com/docs/access?context=t_IFrame&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

