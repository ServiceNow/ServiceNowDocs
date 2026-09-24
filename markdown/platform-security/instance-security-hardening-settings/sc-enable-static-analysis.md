---
title: Enable static analysis
description: Enable static analysis to provide compile-time security checks for JavaScript code in the scripting sandbox.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-static-analysis.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [static analysis, security, JavaScript sandbox, script security]
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Enable static analysis

Enable static analysis to provide compile-time security checks for JavaScript code in the scripting sandbox.

When this property is set to `false`, static analysis is enabled and provides compile-time security analysis. When set to `true`, all static analysis security checks are bypassed. This feature allows you to rapidly respond to JavaScript sandbox security exploits.

to configure this property:

1.  Navigate to `/sys_properties_list.do` on the ServiceNow instance.
2.  Ensure the **com.glide.script.static\_analysis.disabled** either doesn't exist or is set to `false`.

## More information

<table id="table_2lu_9jk_2ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.static\_analysis.disabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

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

-   Severity score: 6.8
-   CVSS rating: Medium
-   Security risk details:

Disabling static analysis removes protections against sandbox escape attempts that the static analyzer would otherwise detect. While other runtime protections exist in the sandbox, disabling static analysis weakens the overall security posture. Sandbox escapes enables users to execute unauthorized and privileged script.


</td></tr><tr><td>

Functional impact

</td><td>

Depending on the configuration of additional properties, sandbox scripts which match static analysis rules are logged or blocked.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

