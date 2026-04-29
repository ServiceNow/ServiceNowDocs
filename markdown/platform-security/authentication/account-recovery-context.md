---
title: Account recovery context
description: The account recovery context uses a policy to define how and when the account recovery can be established.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Account recovery context

The account recovery context uses a policy to define how and when the account recovery can be established.

Administrators can view and modify this context and its associated policy by navigating to **Multi-Provider SSO** &gt; **Account Recovery** &gt; **Account Recovery Context**.

**Note:** By default the policy is **Allow Policy**. The Login for users are restricted by default and the login is allowed only if the conditions defined in **Allow Policy** evaluates to true.

Use the fields in the account recovery context record to define how your instance uses the policy.

<table id="table_otz_ngr_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy context. This field is static and cannot be changed.

</td></tr><tr><td>

Description

</td><td>

Description of the context

</td></tr><tr><td>

Default Policy

</td><td>

Defines the default behavior of this context when evaluating the policy. Select from the following options:-   Allow Policy
-   Deny Policy

</td></tr><tr><td>

Allow Policy

</td><td>

This field appears only when the **Default Policy** field is set to **Allow Policy**.

</td></tr><tr><td>

Deny Policy

</td><td>

This field appears only when the **Default Policy** field is set to **Deny Policy**.

</td></tr></tbody>
</table>## Policy inputs and conditions

The **Policy Input** and **Policy Conditions** tabs display the inputs and conditions of the policy selected in the **Allow Policy** or **Deny Policy** field. These tabs serve as a reference, but cannot be used to change the policy inputs or conditions. To modify your policy settings, navigate to the policy using the information icon next to the **Allow Policy** or **Deny Policy** field.

**Note:** Policy conditions can be created from here, but as a good practice it is recommended to add new policy conditions from policy page.

![Account Recovery Context](../image/account-recovery.png)

