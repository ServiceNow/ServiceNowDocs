---
title: Enable multiple \(permission policy and boundary\) checks to ensure that the Role is privileged in AWS/Bedrock
description: Use a system property to determine what checks are used to verify whether a role is allowed to perform a privileged operation.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable multiple \(permission policy and boundary\) checks to ensure that the Role is privileged in AWS/Bedrock

Use a system property to determine what checks are used to verify whether a role is allowed to perform a privileged operation.

AWS Permission can be set using Identity and Access Management \(IAM\) policies such as `bedrock:InvokeModel` that allow an application to call InvokeModel function on all available models in all regions. Boundary in bedrock is used to limit the maximum permission such as `Limit bedrock:InvokeModel` to only the haiku-3.5 model and specific regions.

The **sn\_ai\_security.bedrock\_priviledge.permission\_policy** system property determines whether an application checks both IAM policy and the bedrock boundary configuration to verify whether a role is allowed to perform a privileged operation.

This property enables multiple \(permission policy and boundary\) checks to ensure that the role is privileged in AWS/Bedrock. If it is not set to the recommended value of `false`, then the application relies only on IAM policy to decide whether a role is privileged.

Set the **sn\_ai\_security.bedrock\_priviledge.permission\_policy** system property to `false` or ensure that it doesn't exist in the System Properties \[sys\_properties\] table to help ensure defense in depth.

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.8
-   CVSS score: Medium
-   Security risk details: Unintended unauthorized access to all resources under one IAM policy on AWS bedrock and within multiple regions. This could include all available AI models within all regions of AWS.

</td></tr><tr><td>

Functional impact

</td><td>

Based on the property value, the application checks either IAM policy only within AWS or also checks boundary configuration within AWS/Bedrock along with IAM policy in order to verify whether a role associated to a request is privileged or not.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

