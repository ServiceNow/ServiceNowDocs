---
title: Escape jelly script \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.ui.escape\_all\_script property to force escape of all scripts injected into Jelly.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape jelly script \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.ui.escape\_all\_script** property to force escape of all scripts injected into Jelly.

This property escapes all the JS and HTML strings included in &lt;j:jelly&gt; ... &lt;/j:jelly&gt; before they are written to the output stream, preventing several XSS issues from occurring. If **glide.ui.escape\_all\_script** is not set to the recommended value of true, then escaping of scripts injected into Jelly is disabled. Without this mitigation, the platform becomes widely open to a variety of script injection attacks. An attacker could execute arbitrary Rhino scripts on the instance.

**Warning:** Be careful when using these tags. If user input is displayed here it can open a security vulnerability.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.escape\_all\_script**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

If the property is not set to **true**, developers have to perform several steps on each custom Jelly script to prevent XSS issues. These steps include locating the Jelly variables being sent to output stream to render on web pages, and performing escaping on each of the following tags:

 `$â {JS:expression}`

 `$â {HTML:expression}`

 OR

 `$â {JS,HTML:expression}`

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

7.3

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces Jelly escaping at the parser level. It can have a functionality impact on user interaction with the resulting data.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Input validation has to occur on all the user input being entered on the application. By doing so, injection attacks against the platform can be defended and protected.

</td></tr><tr><td>

Workaround

</td><td>

The UI may be affected because some of the scripts and HTML tags designed for rendering on a web page may appear broken. This remediation sends the output encoded page to the browser to render.

 For example, instead of `'my string here'`, it might display '`<u>my string here</u>` as the `<u>` tag was properly escaped. In this case, to prevent escaping, add the NOESC prefix to Jelly expression to prevent JS escaping. For example:

-   Before: \($\[jvar\_context\_menus\]\);
-   After: `($[NOESC:jvar_context_menus]);`
-   Before: $\[jvar\_ui\_policy\_scripts\]
-   After: `$[NOESC:jvar_ui_policy_scripts]`

 **Warning:** Be careful when using these tags. If user input is displayed here it can open a security vulnerability.

</td></tr><tr><td>

References

</td><td>

[High Security Settings](../../security/concept/c_HighSecuritySettings.md)

 [Jelly tags](https://www.servicenow.com/docs/access?context=r_JellyTags&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

