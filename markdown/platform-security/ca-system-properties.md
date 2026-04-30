---
title: System properties
description: Use system properties to enable and customize continuous authentication \(CA\) to meet your zero trust access security requirements.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore CA, Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# System properties

Use system properties to enable and customize continuous authentication \(CA\) to meet your zero trust access security requirements.

## Properties

To access the properties page, navigate to **All** &gt; **Continuous Authentication**, select **Properties** tab.

![CA System Properties](../images/ca-system-properties.png)

Following are the different system properties for CA:

<table id="table_vkg_2wf_twb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**General Properties**

</td></tr><tr><td>

Continuous Authentication \(**glide.zta.continuous\_authentication.enabled**\)

</td><td>

Enable to use Continuous Authentication feature

</td></tr><tr><td>

Enable Debugging \(**glide.zta.continuous\_authentication.debug.enabled**\)

</td><td>

Enable to view the debugging information related to continuous authentication.

</td></tr><tr><td colspan="2">

**High Assurance**

</td></tr><tr><td>

High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\)

</td><td>

Specify the high assurance session length, after which the end-users should re-authenticate. Default: 10 mins.**Note:** The value must be between 1 and 480.

</td></tr><tr><td>

Default high-assurance session length upon login \(**glide.zta.default.high\_assurance.session.lifespan**\)

</td><td>

Specify the duration in minutes for the default high-assurance session length upon user login. Default value: **5** minutes.**Note:** The property is only applicable for local login.

</td></tr><tr><td>

Configure end-user display message \(**glide.zta.high\_assurance.session.message**\)

</td><td>

Specify the message that is displayed to the end-user for re-authentication. Default message: `One or more resources require additional authentication due to a policy created by your administrator`.

</td></tr><tr><td>

Total times failed authentication before user account lock-out \(**glide.zta.high\_assurance.session.max.login.failed\_attempts**\)

</td><td>

Set the maximum failed authentication attempts before the users are logged out.**Note:** The value must be between 3 and 10.

</td></tr><tr><td colspan="2">

**Audit properties**

</td></tr><tr><td>

Total no of days to keep audit records \(**glide.zta.continuous\_authentication.audit.lifespan**\)

</td><td>

Specify the no of days you want to save the audit records for CA.**Note:** The value must be between 1 and 180.

</td></tr><tr><td>

Total no. of days after which policies will be deleted after deactivated \(**glide.zta.continuous\_authentication.policy.lifespan**\)

</td><td>

Specify the no of days after which the CA policies are deleted.

</td></tr></tbody>
</table>**Important:**

-   By default, high-assurance sessions are not required for mobile app sessions, even when a continuous authentication policy is active on source. To change this behavior and block access from mobile app sessions, update the **glide.zta.high\_assurance.mobile.session.allowed** property value to `false`.
-   The **sys\_properties**, **sys\_continuous\_auth\_policy**, **sys\_user** tables are excluded for CA and cannot be added to the CA policy configuration.

**Related topics**  


[Explore Continuous Authentication](explore-continuous-auth.md)

[Policies](ca-policies.md)

[Metrics](ca-metrics.md)

[Pre-work for Continuous Authentication](pre-work-ca.md)

