---
title: Disable AJAXEvaluate
description: Use the glide.script.allow.ajaxevaluate to protect the system API from vulnerabilities of Client script execution through AJAX calls.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable AJAXEvaluate

Use the **glide.script.allow.ajaxevaluate** to protect the system API from vulnerabilities of Client script execution through AJAX calls.

Elevation to the security\_admin role is required to edit the property.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.script.allow.ajaxevaluate**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

To prevent a user from executing scripts as an admin privilege.

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Configuration type

</td><td>

Boolean

</td></tr><tr><td>

Functional impact

</td><td>

This remediation forces the AJAXEvaluate processor to be turned off. It could impact functionality if you are explicitly using the AJAX evaluate processor as part of any customized scripts.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) The AjaxEvaluator processor executes Client scripts in sandbox, however there are several additional properties which can allow the scope of activities in the sandbox to expand.

</td></tr><tr><td>

Security risk rating

</td><td>

7.3

</td></tr><tr><td>

References

</td><td>

This property belongs to the same family of properties that secure and restrict execution of scripts originating from the client, such as **glide.script.allow.ajaxevaluate**. For more information, see [Enable AJAXEvaluate](sc-disable-ajaxevaluate.md).

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

