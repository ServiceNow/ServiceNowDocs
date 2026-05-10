---
title: Require AJAXGlideRecord ACL checking
description: Use the glide.script.secure.ajaxgliderecord property to perform access control rule \(ACL\) validation when server-side records, such as tables, are accessed using GlideAjax APIs within a client script.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require AJAXGlideRecord ACL checking

Use the **glide.script.secure.ajaxgliderecord** property to perform access control rule \(ACL\) validation when server-side records, such as tables, are accessed using GlideAjax APIs within a client script.

The **glide.script.secure.ajaxgliderecord** systm property toggles ACL validation for GlideAjax API calls. If **glide.script.secure.ajaxgliderecord** is not set to the recommended value of **true**, then ACL validation will not be completed for GlideAjax requests.

Ensure that the property **glide.script.secure.ajaxgliderecord** is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.secure.ajaxgliderecord**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: This could lead to server-side resources being accessed by users without proper authorization.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces the ACL relationship with server-side records when the requests are made using the AJAXGlideRecord API calls. If the ACL configuration is not properly configured, then there is potential impact. For more details on its impact, and how to identify it, see Refer to [Audit and review client-side GlideRecord \(AJAXGlideRecord\) transactions \[KB0550828\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0550828).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Access control](sc-access-control.md)

