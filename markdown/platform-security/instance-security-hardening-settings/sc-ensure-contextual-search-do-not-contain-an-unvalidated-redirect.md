---
title: Ensure Contextual Search Do Not Contain An Unvalidated Redirect \[New in Security Center 7.0\]
description: Prevent Contextual Search results from containing referral links outside the current domain with a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Ensure Contextual Search Do Not Contain An Unvalidated Redirect \[New in Security Center 7.0\]

Prevent Contextual Search results from containing referral links outside the current domain with a system property.

The Contextual Search plugin displays search results in a new window using the **cxs\_new\_window** UI page. This UI page contains a referral link which can be set by providing a value to **sysparm\_url**. When the **com.snc.contextual\_search.cxs\_new\_window.force\_relative\_link** system property is set to **true**, **sysparm\_url** can only contain links that are relative to the current domain. This restriction prevents the UI page from being used as an unvalidated redirect to an attacker-controlled website. When the property is set to **false**, **sysparm\_url** can link to any website.

Set the **com.snc.contextual\_search.cxs\_new\_window.force\_relative\_link** property to **true**. If the property doesn’t exist on the System Properties \[sys\_properties\] table, the default value is **false**. If the property exists on the table, it defaults to **true**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.contextual\_search.cxs\_new\_window.force\_relative\_link**

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

false

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS score: Medium
-   When set to **false**, **sysparm\_url** can link to any website, which allows the UI page to be used as an unvalidated redirect to an attacker-controlled website.


</td></tr><tr><td>

Functional impact

</td><td>

When set to **true**, **sysparm\_url** is only allowed to contain links that are relative to the current domain. This restriction means that the UI page can only ever link to web pages on the current domain. However, the UI page is meant to display search results from the current domain and should only ever link to the current domain.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The Contextual Search \(com.snc.contextual\_search\) plugin must be active.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

