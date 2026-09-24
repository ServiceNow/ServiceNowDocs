---
title: Enable IAM and boundary checks for Amazon Bedrock access
description: Enable IAM and Boundary Checks for Amazon Bedrock access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-multiple-permission.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable IAM and boundary checks for Amazon Bedrock access

Enable IAM and Boundary Checks for Amazon Bedrock access.

AWS permissions for Amazon Bedrock are set using Identity and Access Management \(IAM\) policies. For example, the `bedrock:InvokeModel` policy allows an application to call `InvokeModel` function on all available models in all AWS regions. Bedrock boundaries restrict the scope of permissions granted by IAM policies. For example, a boundary can limit the `bedrock:InvokeModel` permission to only the Haiku 3.5 model and specific regions.

The **sn\_ai\_security.bedrock\_priviledge.permission\_policy** system property determines whether an application checks both the IAM policy and the Bedrock boundary configuration to verify whether a role is allowed to perform a privileged operation.

When set to the recommended value of `false`, the application validates both checks. If it is set to `true`, then the application checks only on the IAM policy to decide whether a role is privileged.

Set the **sn\_ai\_security.bedrock\_priviledge.permission\_policy** system property to `false` or ensure that it doesn't exist in the sys\_properties table to support defense in depth.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_ai\_security.bedrock\_priviledge.permission\_policy**

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

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.8
-   CVSS score: Medium
-   Security risk details: Unintended unauthorized access to all resources under one IAM policy on Amazon Bedrock and within multiple AWS regions. This could include all available AI models within all regions.

</td></tr><tr><td>

Functional impact

</td><td>

Based on the property value, the application either checks only the IAM policy or checks both the IAM policy and the Amazon Bedrock boundary configuration to verify whether a role has the required privileges.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

