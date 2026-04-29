---
title: Enable Guardian for External Agents
description: Use a system property to protect your Language Learning Models \(LLMs\) with Guardian.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable Guardian for External Agents

Use a system property to protect your Language Learning Models \(LLMs\) with Guardian.

Use the **sn\_aia.external\_agent\_guardian\_check** system property to enable Guardian, which monitors requests sent to Language Learning Models \(LLMs\) and their responses to help protect you, your users, and your data. There are three types of content that are monitored for:

-   offensive or harmful content
-   prompt injection attempts
-   filtered subjects

Ensure that the **sn\_aia.external\_agent\_guardian\_check** system property does not exist in the System Properties \[sys\_properties\] table, or exists and is set to a value of `true`.

## More information

<table id="table_w2n_pqs_4hc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_aia.external\_agent\_guardian\_check**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:4.1
-   CVSS score: Medium
-   Security risk details: Prompt injection is a type of attack where bad actors override the normal instructions of an LLM to access restricted information or elicit unexpected behaviors. Prompt injection detection is based on the LLM which has been trained on various types of prompt injection techniques such as role playing, paraphrasing, repetition, instructions to ignore other instructions, persuasion, etc.

</td></tr><tr><td>

Functional Impact

</td><td>

Guardian may produce false positives and block legitimate requests.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

