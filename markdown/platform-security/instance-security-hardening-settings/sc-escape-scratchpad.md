---
title: Escape scripts in scratchpad \[Updated in Security Center 1.3\]
description: Learn how scratchpad factors into the security posture of your instance and how to manage it so that malicious scripts can't be executed on it.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape scripts in scratchpad \[Updated in Security Center 1.3\]

Learn how scratchpad factors into the security posture of your instance and how to manage it so that malicious scripts can't be executed on it.

The scratchpad is an easy way to set information on the server that you can access in the browser. An admin can script anything to be on it, including arbitrary records. If this property is not set to the recommended value of **true**, then it is possible to execute malicious scripts like a cross-site scripting vulnerability.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.escape\_scratchpad**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: If the property is not set to the recommended value of **true**, then it is possible to execute malicious scripts like a cross-site scripting vulnerability.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Workflow administration](https://www.servicenow.com/docs/access?context=c_WorkflowAdministration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

