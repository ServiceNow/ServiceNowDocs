---
title: Configure MFA with SSO
description: Enforce MFA with SSO for your users within or outside your organization.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Multi-factor authentication with Single Sign-On, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Configure MFA with SSO

Enforce MFA with SSO for your users within or outside your organization.

## Before you begin

The MFA with SSO feature is offered as a part of the Adaptive Authentication plugin \(com.snc.adaptive\_authentication\). You must enable the Adaptive authentication property for using MFA with SSO feature. To know more on how to set up Adaptive authentication, see [Adaptive authentication](../concept/adaptive-authentication.md).

**Note:** MFA with SSO login is available if the **glide.authenticate.mfa.with.multisso.enabled** property is set to **true**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Properties**.

2.  Enable the **Enable Multi-factor authentication** and **Enable Multi-factor Authentication with SSO** check boxes.

    ![Enable MFA for SSO.](../images/mfa-sso-properties.png)

3.  Click **Save**.

4.  Navigate to **Multi-factor Authentication** &gt; **MFA Context**.

    The MFA Context form appears.![MFA Auth Context](../images/mfa-auth-context.png)

    **Note:** By default, the policy is **Step-Up MFA Policy**. Users are shown with Multi-factor Authentication if a condition configured in **Step-Up MFA Policy** evaluates to **true**. Policy takes precedence over the user or role-based configuration.

5.  To edit a policy, go back to the Authentication Policy record, change the conditions, and come back.

    When you navigate to the Authentication Policy record, you can add or edit the 'Policy Inputs' to the referenced Policy fields, **Step-Up MFA Policy** or **Step-Down MFA Policy**.

6.  To set a new policy condition, click **Policy Conditions**.

7.  Click **New**.

8.  On the form, fill in the fields.

<table id="table_ihs_5ym_bmb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for the condition that you want to create for the label.

</td></tr><tr><td>

Description

</td><td>

The policy condition description.

</td></tr><tr><td>

Conditions

</td><td>

The type of condition that you want to apply for the policy. You can add filter conditions and 'OR' clauses.**Note:** Adding various filter conditions and clauses enables you to challenge MFA for specific users.

</td></tr></tbody>
</table>    ![Condition - New record](../images/mfa-sso-new-record.png)

    To set up your conditions, consider the following example. Assume that you want the authentication scheme with the identity provider as your condition for external users. You can set the conditions as follows:

    1.  Select **Authentication Scheme** and set the criteria as **Single Sign-On** or **Username and Password**.

        Based on this selection, the user is provided with an SSO-based login or login form to specify the user name and password.

    2.  Select **Identity Provider** and specify the provider as the IDP record for which you want to enable MFA. For example, **Okta**.
    Based on this selection, if the user logs in with SSO, the user is not challenged with MFA. In contrast, if the user logs in using Okta, then the user is challenged with MFA.

9.  Click **Submit**.


**Related topics**  


[Adaptive authentication](../concept/adaptive-authentication.md)

[t_ActivateMultifactorAuthenticator]

[Multi-factor authentication with Single Sign-On](../concept/mfa-sso.md)

