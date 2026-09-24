---
title: Enable KittyScript sandbox security enforcement
description: KittyScript sandbox enforcement prevents untrusted scripts from executing with unrestricted system privileges. The following properties control enforcement activation, level, and timing. Configuring them incorrectly can cause malicious code to bypass security protections and access restricted APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-kittyscript-sandbox-security.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [sandbox security]
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable KittyScript sandbox security enforcement

KittyScript sandbox enforcement prevents untrusted scripts from executing with unrestricted system privileges. The following properties control enforcement activation, level, and timing. Configuring them incorrectly can cause malicious code to bypass security protections and access restricted APIs.

-   **`com.glide.script.sandbox.ks.watchdog.enabled`** \(default: `true`\): Master control for the KittyScript sandbox security interpreter in ServiceNow Guarded Scripts framework. When set to `true`, all untrusted scope scripts are subject to sandbox enforcement. When set to `false`, disables KittyScript entirely.
-   **`com.glide.script.sandbox.ks.watchdog.auto.advance`**: Controls whether the watchdog automatically advances from Phase 1 \(detection-only\) to Phase 3 \(full rejection\).
-   **`com.glide.script.sandbox.ks.watchdog.phase.duration.days`**: Specifies how long each active phase persists before advancing to the next phase.
-   **`com.glide.script.sandbox.ks.watchdog.phase`**: Sets the enforcement level \(Phase 1–3\) for authenticated script execution. Phase 3 enforces full restrictions.

Verify the following properties exist in the `sys_properties` table and set them to the specified values if they exist:

-   `com.glide.script.sandbox.ks.watchdog.enabled` = `true`
-   `com.glide.script.sandbox.ks.watchdog.auto.advance` = `true`
-   `com.glide.script.sandbox.ks.watchdog.phase.duration.days` = `14`
-   Create or update the `com.glide.script.sandbox.ks.watchdog.phase` property. Set the value to `3`.

## More information

<table id="table_u1q_2z3_bkc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.sandbox.ks.watchdog.enabled**

 **com.glide.script.sandbox.ks.watchdog.auto.advance**

 **com.glide.script.sandbox.ks.watchdog.phase.duration.days**

 **com.glide.script.sandbox.ks.watchdog.phase**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean, Boolean, Integer, Integer

</td></tr><tr><td>

Recommended value

</td><td>

true, true, 14, 3

</td></tr><tr><td>

Default value

</td><td>

true, true, 14, 0

</td></tr><tr><td>

Fallback value

</td><td>

true, true, 14, 0

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8
-   CVSS rating: High
-   Security risk details:

Disabling the **com.glide.script.sandbox.ks.watchdog.enabled** property removes all sandbox protections for untrusted scripts, allowing malicious or poorly-written code to execute with full system privileges and access restricted APIs. This can lead to data theft or system compromise.

Disabling the **com.glide.script.sandbox.ks.watchdog.auto.advance** property freezes enforcement at Phase 1 \(detection-only\), allowing scripts with unsupported features to continue executing indefinitely without sandbox restrictions, indefinitely deferring security hardening platform-wide.

Setting the **com.glide.script.sandbox.ks.watchdog.phase.duration.days** property to a value too high delays enforcement phase transitions. This leaves the platform in permissive phases \(1-2\) longer than intended and extending the window where malicious scripts can bypass sandbox protections.

Setting the **com.glide.script.sandbox.ks.watchdog.phase** property to permissive phases \(1-2\) allows untrusted scripts to execute without sandbox enforcement. This enables attackers to exploit vulnerable code paths, access unauthorized APIs, and potentially escalate privileges or exfiltrate data.


</td></tr><tr><td>

Functional impact

</td><td>

**When set with recommended values:** The system checks all scripts for security violations. Restrictions progressively enforce, blocking scripts from accessing unauthorized data or APIs. This is the secure, standard operating mode.

 **When turned off:** All script security checks are turned off. Scripts execute without restrictions, creating significant security risks. While disabling enforcement can temporarily resolve broken scripts during emergencies, it exposes the system to malicious or poorly written code.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

