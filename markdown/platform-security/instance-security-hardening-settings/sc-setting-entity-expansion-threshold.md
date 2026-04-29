---
title: Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable
description: Use the glide.xmlutil.max\_entity\_expansion property to change the maximum entity expansion limit to a smaller number.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable

Use the **glide.xmlutil.max\_entity\_expansion** property to change the maximum entity expansion limit to a smaller number.

The **glide.xmlutil.max\_entity\_expansion** system property controls the maximum amount of entity expansion within an XML Parser. If **glide.xmlutil.max\_entity\_expansion** isn't set to the recommended value of `3000` or less, then the GlideXMLUtil parsing scriptable may be vulnerable to denial of service attacks.

Ensure that the property **glide.xmlutil.max\_entity\_expansion** is set to `3000` or less.

If the instance is on Washington or later, the default implied value is 3000 if the System Properties \[sys\_properties\] record does not exist. If the instance is not on Washington or later, the recommendation is for the instance admin to create a System Properties \[sys\_properties\] and set the value to `3000`.

**Note:** 500 is the default minimum imposed by the ServiceNow AI Platform, which is considered to be a safe threshold.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

****

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

Less than or equal to 3000

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

3000

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS rating: Medium
-   Security risk details: A Denial-of-Service \(DoS\) vulnerability poses a security risk by allowing attackers to overwhelm or crash a system, rendering it unavailable to legitimate users and potentially disrupting critical operations.

</td></tr><tr><td>

Functional impact

</td><td>

If the customization is using large entity expansion, then, the ServiceNow AI Platform might block further processing.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

