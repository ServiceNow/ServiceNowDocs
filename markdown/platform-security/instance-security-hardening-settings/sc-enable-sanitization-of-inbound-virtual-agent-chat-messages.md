---
title: Enable sanitization of inbound virtual agent chat messages
description: The glide.cs.sanitize\_inbound\_messages.enabled property controls whether Virtual Agent runs a dedicated HTML sanitization check on inbound chat messages sent from a requester to an agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-sanitization-of-inbound-virtual-agent-chat-messages.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable sanitization of inbound virtual agent chat messages

The **glide.cs.sanitize\_inbound\_messages.enabled** property controls whether Virtual Agent runs a dedicated HTML sanitization check on inbound chat messages sent from a requester to an agent.

When set to `true` \(recommended\), the platform strips unsafe HTML content from each inbound message. If content is removed, both the requester and the agent \(in live-agent conversations\) are notified that sanitization occurred. When set to `false`, inbound messages instead pass through only the legacy system-message sanitization path, and the dedicated inbound-content check is skipped.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Set the **glide.cs.sanitize\_inbound\_messages.enabled** property to `true`.

## More information

<table id="table_8ui_j23_3ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.cs.sanitize\_inbound\_messages.enabled**

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

[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS rating: Low
-   Security risk details: If this property is not set to `true`, Virtual Agent chat messages from requesters skip this dedicated sanitization check. The message is delivered to the agent unfiltered. A requester can inject malicious HTML or script content into their message. When the agent views the message, the browser renders this content in the agent's session, creating a reflected cross-site scripting \(XSS\) attack against the agent.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this property adds an additional sanitization pass to every inbound Virtual Agent chat message. Messages containing certain markup are flagged, stripped, and replaced with a system warning to the requester and agent. Live-agent handoffs receive the same treatment rather than delivery as originally typed.

 Availability impact is minimal because the control affects message content and rendering only—not conversation flow or session continuity.

 **Test these scenarios:**

 -   &gt;Inbound consumer and live-agent chat conversations
-   Messages containing HTML-like syntax or rich-control content \(for example, topic-picker selections\)

 Verify that legitimate messages are delivered without false warnings.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

No effect unless **com.glide.cs.html.sanitizer.enabled** is set to `true`.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

