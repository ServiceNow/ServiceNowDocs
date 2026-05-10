---
title: Display recommendations for high risk UI pages
description: Decrease the likelihood of authorization errors, and unintended information disclosure by displaying recommendations for high risk UI pages.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Display recommendations for high risk UI pages

Decrease the likelihood of authorization errors, and unintended information disclosure by displaying recommendations for high risk UI pages.

Use the **glide.script.ui\_page.customer\_scoped.security\_msgs\_enabled** system property to determine whether to display security recommendations to users configuring UI pages when:

-   An ACL is missing
-   GlideRecord/GlideDBQuery APIs are used instead of GlideRecordSecure
-   the page is configured as public in the "sys\_public" table

When the property is enabled, recommendations when the preceding conditions are met, decreasing the likelihood of authorization errors, and helping prevent unintended information disclosure.

Set the system property **glide.script.ui\_page.customer\_scoped.security\_msgs\_enabled** to **true** to display these recommendations.

## More information

<table id="table_zyc_nlf_32c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical configuration name

</td><td>

glide.script.ui\_page.customer\_scoped.security\_msgs\_enabled

</td></tr><tr><td>

Plugin applicability

</td><td>

None

</td></tr><tr><td>

Security risk

</td><td>

Setting this system property to **false** increase the likelihood of authorization errors, and unintended information disclosure.

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) score

</td><td>

5.3

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) rating

</td><td>

Medium

</td></tr><tr><td>

Functional impact

</td><td>

Displays security recommendations to users configuring UI pages.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Base system value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Access control](sc-access-control.md)

