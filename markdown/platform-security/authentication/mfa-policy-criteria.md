---
title: Configure adaptive authentication policy-based multi-factor criteria
description: Use adaptive policies to determine which users must use two-step multi-factor \(MFA\) verification.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MFA criteria, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure adaptive authentication policy-based multi-factor criteria

Use adaptive policies to determine which users must use two-step multi-factor \(MFA\) verification.

## Before you begin

Role required: adaptive\_auth\_admin

**Note:**

-   If the default policy is **Step-Up MFA Policy**, users will be shown with Multi-factor Authentication if policy configured in **Step-Up MFA Policy** evaluates to true. Policy takes precedence over the user or role based configuration.
-   MFA with SSO login will only be available if `glide.authenticate.mfa.with.multisso.enabled` Property is set to true.
-   You can navigate to the Authentication Policy record to Add or Edit the 'Policy Input\(s\)' to the referenced Policy field \(**Step-Up MFA Policy** or **Step-Down MFA Policy**\).

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **MFA Context**.

    The **MFA Context** policy context record opens.

2.  Select the default policy in the **Default Policy** field.

    This selection determines how your instance uses the policy conditions to determine whether to require MFA.

    |Default Policy|Definition|
    |--------------|----------|
    |Step-Up MFA Policy|Select to enforce MFA when the policy conditions defined in **Step-Up MFA Policy** evaluate to true.|
    |Step-Down MFA Policy|Select to bypass MFA when the policy conditions defined in the **Step-Down MFA Policy** evaluate to true.|

3.  In the **Step-Up MFA Policy** field, select a policy to use with this context.

4.  Click **Update**.

    After saving the record, the **Policy Input** and **Policy Conditions** lists update to display the policy inputs and conditions associated with the policy selected in the **Step-Up MFA Policy** field.


