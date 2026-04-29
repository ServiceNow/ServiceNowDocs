---
title: Specify URL allow list for cross-origin iframe communication
description: Use a system property to specify which domains you trust for cross-origin communication.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Specify URL allow list for cross-origin iframe communication

Use a system property to specify which domains you trust for cross-origin communication.

Use the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** property to enable cross-origin communication between iframes from trusted domains you specify in an inclusion list. This property specifies list of trusted origins for message propagation \(sent via window.postMessage\) in the UI. If this property isn't set to a list of trusted/allowed origins for cross domain messaging, then cross origin messages can be allowed from domains which contain malicious scripts. The property values should contain a list of origins should be separated by a comma. If the property value is empty then all domains are blocked.

Ensure that the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** system property contains only a list of trusted domains to be used for cross origin messaging. If the list is empty no domains are allowed.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

</td></tr><tr><td>

Recommended value

</td><td>

a comma separated list of trusted domains or empty

</td></tr><tr><td>

Default value

</td><td>

empty

</td></tr><tr><td>

Fallback value

</td><td>

empty

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Invalid trusted origins can allow untrusted domains to inject malicious payloads via window.postMessage, leading to cross-origin attacks such as data exfiltration, session hijacking, UI manipulation or DOM based XSS. If a web page contains event handlers that do not perform proper origin validation, a web page, or script from any origin, can communicate with it. It can also initiate any functionality performed by the event handler. Communication with iframes from other domains is a security risk.

</td></tr><tr><td>

Functional impact

</td><td>

If you don't add intended domains to the inclusion list, cross-origin messages from that domain are not allowed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

