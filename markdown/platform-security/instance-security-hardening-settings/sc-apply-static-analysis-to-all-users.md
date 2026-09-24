---
title: Apply static analysis to all users
description: Configure static analysis to examine scripts from both authenticated and unauthenticated users rather than limiting analysis to guest users only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-apply-static-analysis-to-all-users.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [static analysis, security, authenticated users, unauthenticated users, script security]
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Apply static analysis to all users

Configure static analysis to examine scripts from both authenticated and unauthenticated users rather than limiting analysis to guest users only.

By default, static analysis examines all scripts regardless of user authentication status. Setting the **com.glide.script.static\_analysis.only\_check\_unauthenticated\_users** property to `true` limits analysis to unauthenticated users only, creating a security gap for authenticated users. Setting the property to `false` confirms comprehensive security coverage across all user types.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the &lt;ph keyref="var.company-no-reg-tm"/&gt; instance.
2.  Verify the **com.glide.script.static\_analysis.only\_check\_unauthenticated\_users** property is set to `false`.

## More information

<table id="table_property_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.static\_analysis.only\_check\_unauthenticated\_users**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(`/sys_properties_list.do`\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: Medium
-   CVSS score: 6.8
-   Security risk details:

When this property is set to `true`, static analysis applies only to unauthenticated users, creating significant security gaps:

    -   Authenticated users can execute malicious scripts without detection.
    -   Insider threats from legitimate users bypass static analysis.
    -   Attacks that use stolen credentials or session hijacking avoid analysis.
    -   Assumes authenticated users are trusted which may not be valid in all environments.
    -   Service accounts and integration users may have elevated privileges but bypass analysis.

</td></tr><tr><td>

Functional impact

</td><td>

Setting this property to `false` brings authenticated-user scripts under static analysis. Existing authenticated-user scripts using patterns like Array.prototype access may trigger security violations. Test critical business rules, script includes, and scheduled jobs before rolling out this property.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.script.static\_analysis.disabled** must be set to `false` for the **com.glide.script.static\_analysis.only\_check\_unauthenticated\_users** property to have any effect.

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

