---
title: Sanitize HTML in the Description Fields of the Impact Workspace Module
description: Sanitize the HTML in the description fields by removing HTML tags that are sources of HTML injection attacks with the sn\_impact\_common.blacklist\_tags\_HTML\_injection property.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-06-09"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Sanitize HTML in the Description Fields of the Impact Workspace Module

Sanitize the HTML in the description fields by removing HTML tags that are sources of HTML injection attacks with the **sn\_impact\_common.blacklist\_tags\_HTML\_injection** property.

The Impact Workspace module allows HTML in the following description fields:

-   The customer\_notes field of the sn\_impact\_common\_capabilities\_map and sn\_impact\_common\_par\_version\_phase\_app\_mapping tables.
-   The manual\_description field of the sn\_impact\_common\_manual\_capability\_description table.

When this system property contains a comma-separated list of HTML tags \(for example, scripts\), those tags and their contents are removed from the HTML portions of the listed fields. Removing these tags helps sanitize the HTML in the description fields by removing HTML tags that are sources of HTML injection attacks. If this property isn’t set in the System Properties \[sys\_properties\] table, the value defaults to a default list of denied HTML tags. If the property is empty, all HTML tags are allowed.

Use the **sn\_impact\_common.blacklist\_tags\_HTML\_injection** provide a comma-separated list of HTML tags which are removed from the description fields for the Impact Workspace module. This removal helps to prevent HTML injection attacks. At minimum, this list should contain the contents of the default list. If the property isn’t set in the System Properties \[sys\_properties\] table, it defaults to the list `script,iframe,object,embed,form,onerror,onload,style,img,video,audio,source,button`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**sn\_impact\_common.blacklist\_tags\_HTML\_injection**

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

Sanitize the HTML in the description fields by removing HTML tags that are sources of HTML injection attacks.

</td></tr><tr><td>

Recommended value

</td><td>

At minimum, the default value of `script,iframe,object,embed,form,onerror,onload,style,img,video,audio,source,button`

</td></tr><tr><td>

Default value

</td><td>

`script,iframe,object,embed,form,onerror,onload,style,img,video,audio,source,button`

</td></tr><tr><td>

Security risk rating

</td><td>

4.4

</td></tr><tr><td>

Functional impact

</td><td>

If an HTML tag is added to default list, it may limit the required HTML functionality of the description fields. The exact impact is dependent on the customer instance.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\)

</td></tr><tr><td>

References

</td><td>

[High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

