---
title: Enable synchronous mode for static analysis
description: The com.glide.script.static\_analysis.enable\_sync property controls whether static analysis security violations block script execution synchronously or are recorded asynchronously. Setting this property to true enables synchronous mode, which blocks scripts with security violations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-synchronous-mode-for-static-analysis.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [static analysis]
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Enable synchronous mode for static analysis

The **com.glide.script.static\_analysis.enable\_sync** property controls whether static analysis security violations block script execution synchronously or are recorded asynchronously. Setting this property to `true` enables synchronous mode, which blocks scripts with security violations.

When set to `false` \(the default\), violations are recorded asynchronously through statistical logs without preventing script execution. When set to `true`, security violations block script execution with a `SecurityException`. Asynchronous mode \(`false`\) is for environments where availability is prioritized. Synchronous mode \( `true`\) is better for high-security environments where blocking malicious scripts is more important than performance.

To configure this property:

-   Navigate to `/sys_properties_list.do` on the ServiceNow instance.
-   Ensure the property **com.glide.script.static\_analysis.enable\_sync** exists and is set to `true`.

## More information

<table id="table_ajc_y23_3ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.static\_analysis.enable\_sync**

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
-   Security risk details: Setting the **com.glide.script.static\_analysis.enable\_sync** property to `false` weakens protection against sandbox escape attempts that the static analyzer would otherwise detect when availability or performance is prioritized over security.

</td></tr><tr><td>

Functional impact

</td><td>

This property determines if static analysis security violations block script execution. The default value of `false` records the violation but does not prevent the script execution. Impact of enabling sync mode \(false → true\):

 -   Every sandbox script execution includes inline static analysis
-   Scripts with security violations fail with SecurityException
-   A small amount of latency added to script execution \(ranging from microseconds to milliseconds depending on script size\)
-   Violations are persisted to the Error log table

 Regression testing:

 -   Run load tests to measure performance impact on script-heavy operations
-   Execute critical business rules, script includes, and background scripts
-   Check error log \(System Log → Errors\) for SecurityException records
-   Monitor response times for pages/APIs that execute sandbox scripts
-   Review statistics logs for latency percentiles \(histogram50ns, histogram90ns, histogram99ns\)
-   Identify any false positives that block legitimate scripts
-   Test under peak load conditions to ensure acceptable performance

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The property **com.glide.script.static\_analysis.disabled** must be set to `false` for the **com.glide.script.static\_analysis.enable\_sync** property to have any effect.

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

