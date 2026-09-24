---
title: Enforce signature verification for Flow Designer artifacts
description: The com.glide.hub.code\_signing.full.validation.enabled property controls the strictness of checks enforced when Code Signing is fully enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-signature-verification-for-flow-designer-artifacts.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [code signing, flow designer, signature verification, security]
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Enforce signature verification for Flow Designer artifacts

The **com.glide.hub.code\_signing.full.validation.enabled** property controls the strictness of checks enforced when Code Signing is fully enabled.

When set to `true`, stricter checks are enforced and certain Flow Designer features incompatible with [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-landing.md) are blocked. If set to `false` or left unset, legacy checks are performed instead, and a subset of Code Signing-incompatible Flow Designer features are allowed to execute.

To configure this property:

1.  You must have the security\_admin role.
2.  The Code Signing plugin \(com.glide.code\_signing\) must be fully enabled. See [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/config-code-signing.md).
3.  Navigate to `/sys_properties_list.do` on the instance.
4.  Set the **com.glide.hub.code\_signing.full.validation.enabled** property to `true`.

## More information

<table id="table_property_details-enforce-signature-verification-for-flow-designer-artifacts"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.hub.code\_signing.full.validation.enabled**

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

`true`

</td></tr><tr><td>

Default value

</td><td>

`false`

</td></tr><tr><td>

Fallback value

</td><td>

`false`

</td></tr><tr><td>

Category

</td><td>

[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating:Medium
-   CVSS score: 4.4
-   When signature validation is turned off, Flow Designer artifacts execute without cryptographic verification of their origin or integrity. This allows attackers to inject unsigned or tampered flows that execute with system privileges.

An attacker could modify a flow to exfiltrate data, escalate privileges, or create backdoors without detection because digest validation is bypassed entirely. Disabling this control removes a critical safeguard that verifies only authorized, unmodified code executes through Flow Designer.


</td></tr><tr><td>

Functional impact

</td><td>

When enabled, Flow Designer artifacts are validated for cryptographic signatures and integrity digests. Unsigned or tampered flows are flagged as untrusted in guardrails reports and require explicit review before deployment. When disabled \(the default\), signature verification and digest validation are skipped, allowing unsigned or tampered flows to execute without verification. Although this reduces scan overhead, it eliminates the detection of unsigned or tampered code. Organizations should enable this property in all production environments to enforce artifact integrity and prevent execution of unverified flows. The default disabled state represents a significant security gap.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This property requires Code Signing to be fully enabled on the instance.

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-malicious-code.md)

