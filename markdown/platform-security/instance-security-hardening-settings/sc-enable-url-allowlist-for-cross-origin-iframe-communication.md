---
title: Restrict allowed domains for cross-origin iframe communication
description: Use a system property to enable cross-origin communication between iframes.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict allowed domains for cross-origin iframe communication

Use a system property to enable cross-origin communication between iframes.

Use the **glide.ui.concourse.onmessage\_enforce\_same\_origin** property to prevent cross-origin communication from untrusted domains. If not set to the recommended value of `true` then validation is not performed for cross-origin messaging. If set to `true` then domains listed in the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** system property can propagate messages in the UI. Use **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** to control which domains are allowed.

Ensure that the **glide.ui.concourse.onmessage\_enforce\_same\_origin** property exists in the System Properties \[sys\_properties\] table and is set to `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.concourse.onmessage\_enforce\_same\_origin**

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

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: If a web page's event handlers don't perform proper origin validation, then another web page or script from any origin can communicate with it. These pages or scripts can also initiate any functionality performed by the event handler. This property allows potentially untrusted external domains to send messages to the ServiceNow instance, increasing the risk of cross-origin attacks like data theft or UI manipulation.

</td></tr><tr><td>

Functional impact

</td><td>

If you don't add intended domains to the inclusion list in the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** system property, cross-origin messages from that domain aren't allowed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

