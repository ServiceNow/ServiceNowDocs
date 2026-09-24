---
title: Restrict exposure of validation error details to end users
description: Configure the platform to return generic error messages instead of detailed validation error text to end users in conversational AI interfaces when skill validation fails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-exposure-of-validation-error-details-to-end-users.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [validation error messages, conversational AI, information disclosure, error handling, security]
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Restrict exposure of validation error details to end users

Configure the platform to return generic error messages instead of detailed validation error text to end users in conversational AI interfaces when skill validation fails.

The **glide.cs.enable\_validation\_error\_messages** property controls whether the platform returns detailed validation and actionable error messages to end users in a conversational AI interface when skill validation fails during a conversation. At the recommended setting of `false`, the platform withholds the specific validation-failure text extracted from internal skill-validation errors and returns only a generic context-profile message. This limits the amount of internal system detail exposed through the conversational interface.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the ServiceNow instance.
2.  Verify the **glide.cs.enable\_validation\_error\_messages** property is set to `false`.

## More information

<table id="table_property_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.cs.enable\_validation\_error\_messages**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(`/sys_properties_list.do`\)

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

[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: Medium
-   CVSS score: 4.3
-   Security risk details:

Displaying detailed internal error text to end users can reveal implementation details about how a system validates and processes requests. An attacker who receives this information can use it to understand internal logic, identify weaknesses, and craft more effective targeted attacks. Sensitive operational details may also be disclosed to users who have no legitimate requirement to see them.

Failure to enforce this control may result in information disclosure that helps an attacker map the system and escalate an intrusion.


</td></tr><tr><td>

Functional impact

</td><td>

Changing this property affects only the error message returned to end users from conversational AI skills. No other flows or features read this property. Availability risk is low because the change only toggles which error string is returned, not control flow.

 Regression-test the affected conversation flow and confirm end users see the generic message rather than the detailed validation error text after deployment.

</td></tr><tr><td>

Dependencies and Prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

