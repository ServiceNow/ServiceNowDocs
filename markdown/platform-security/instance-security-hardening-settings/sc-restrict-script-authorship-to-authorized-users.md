---
title: Restrict script authorship to authorized users only
description: The glide.security.scripting\_governance.enabled property controls whether users must hold the script-writer role to create or modify executable script content across the platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-script-authorship-to-authorized-users.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [script authorship, scripting governance, script-writer role, security property, code execution]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict script authorship to authorized users only

The **glide.security.scripting\_governance.enabled** property controls whether users must hold the script-writer role to create or modify executable script content across the platform.

When this property is enabled, users must hold the script-writer role to author or import records containing executable script content. Script content includes business rules, email templates, conditions, workflows, and HTML or XML code.

When this property is turned off, any user can create or modify code without authorization. Disabling this property removes a critical access boundary and allows any user, including low-privilege, guest, or malicious accounts, to inject arbitrary code into the system.

**Important:** This property is a foundational security control that prevents unauthorized code execution. Disabling it exposes the platform to significant security risks including privilege escalation, data exfiltration, and system compromise.

To configure this property:

-   Navigate to /sys\_properties\_list.do on the instance.
-   Ensure **glide.security.scripting\_governance.enabled** doesn't exist in the sys\_properties table or is set to `true`.

<table id="table_6ou_9jk_2ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.scripting\_governance.enabled**

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

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS rating: Low
-   Security risk details: Disabling script governance removes the authorization gate on code authorship platform-wide. Any user can create or modify executable scripts that run with system privileges.

An attacker with low-privilege or guest access can inject malicious code into business rules, conditions, or workflows. The code executes automatically, enabling data theft, privilege escalation, and persistent backdoors.

This completely undermines platform security and enables full system takeover.


</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

