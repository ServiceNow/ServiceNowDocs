---
title: MFA enforcement exception
description: FAQ related to MFA enforcement exception and why it’s important.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Frequently asked questions, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA enforcement exception

FAQ related to MFA enforcement exception and why it’s important.

1.  How can the MFA mandate be relaxed for specific users?

    In the Yokohama release, a new user group, MFA Exempted User Group record is added. Based on the default condition, there’s an MFA policy added, any user who is a member of this group is enforced with MFA.

    ![MFA Exempted User Group](../images/mfa-exempted-group.png)

    To relax MFA for specific users, follow the procedure:

    -   Navigate to **MFA context**. The Step-Up MFA Policy associated with the MFA context record should be “Enforce MFA for non-SSO logins.![Policy](../images/mfa-excempted-policy.png)
    -   Under the **Policy Input** related list, select the **Is a member of MFA exempted group** filter criteria record.
    -   Select **MFA Exempted User Group**.![Policy Input](../images/mfa-exempted-input.png)
    -   Add users to this group as a member to exempt them from MFA enforcement.![Add users](../images/mfa-exempted-add-user.png)
    **Note:** If you have a different policy associated with the MFA context, you can add “Is a member of MFA exempted group” filter criteria to your policy and modify the policy conditions to exempt users of this group from MFA enforcement.

2.  How can the MFAs mandate be relaxed for certain roles?

    In the Yokohama release, an empty new role **Has MFA exempted role** filter criterion is added. There are conditions added to the MFA policy to exempt users who have the roles part of exempted role criteria from the MFA enforcement.

    ![MFA Relaxed](../images/mfa-excempted-relaxed.png)

    To relax MFA for specific roles, follow the procedure:

    -   Navigate to **MFA context**. The Step-Up MFA Policy associated with the MFA context record should be **Enforce MFA for non-SSO logins**.![MFA exempted role](../images/mfa-exempted-relaxed-policy.png)
    -   Under the **Policy Input** related list, select **Has MFA exempted role** filter criteria record.![Policy Input](../images/mfa-exempted-relaxed-input.png)
    -   Add the roles that you want to add to the condition. You can add multiple roles using the OR operator.
    **Note:** If you have a different policy associated with the MFA context, you can add **Has MFA exempted role** filter criteria to your policy. Modify the policy conditions to exempt users with exempted roles from the MFA enforcement.

3.  How can the MFAs mandate be relaxed for certain groups?

    In the Yokohama release, a user group **MFA Exempted User Group** is added. Based on the default, condition added to the MFA policy, the user or group who is a member of this group isn’t enforced with MFA.

    ![Exempted Group](../images/mfa-exempted-group.png)

    To relax MFA for specific groups, follow the procedure:

    -   Navigate to **MFA context**. The Step-Up MFA Policy associated with the MFA context record should be **Enforce MFA for non-SSO logins**.![Policy Input](../images/mfa-excempted-user-group-input.png)
    -   Under the **Policy Input** related list, select the **Is a member of MFA exempted group** filter criteria record.
    -   Select **MFA Exempted User Group**.![Group Filter Criteria](../images/mfa-excempted-user-input-group.png)
    -   Add the groups that you want to exempt from the MFA enforcement to this group.![Add Group](../images/mfa-exempted-user-group-add.png)
4.  How can the MFAs mandate be relaxed for trusted networks?

    -   Navigate to **Adaptive Authentication** &gt; **Filter Criteria** &gt; **IP Filter Criteria**.
    -   Create a criterion to specify a trusted network. You can specify a list of IP ranges or subnets as part of the trusted network.![IP Filter Criteria](../images/mfa-exempted-ip.png)
    -   Navigate to **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **MFA context**.
    -   Open the policy associated with the context.![Modilfy Policy](../images/mfa-exempted-ip-edit.png)
    -   Select the edit to add the **IP Filter Criteria** that you created to the **Policy inputs-related** list.![Policy selection](../images/mfa-exempted-ip-policy.png)
    -   Modify the policy condition to confirm it evaluates to false when users are part of the trusted network.![Modify the policy inputs](../images/mfa-exempted-ip-change.png)
    **Note:** If you have a different policy associated with the MFA context, you can add the IP filter criteria created as part of Step 1 to your policy and modify the policy conditions to exempt MFA enforcement on the trusted network.

5.  How can the MFAs mandate be relaxed for trusted locations?

    You can use Location Filter Criteria which is available with the **Zero Trust – Location Based Access** \(requires an additional subscription\) plugin.

6.  How to control the frequent MFA enforcement?

    Use the Location Filter Criteria which is available with the **Zero Trust – Location-Based Access** \(requires an additional subscription\) plugin.

    On the MFA validation page, there's a check box to remember a browser. MFA isn’t enforced on the remembered browser:

    ![MFA do not challenge](../images/mfa-enforcement-delay.png)

    -   The duration specified by this system property. `glide.authenticate.multifactor.browser.fingerprint.validity`. The default value of the property is 8 hours. This duration can be increased by up to 24 hours. Similarly using the `glide.authenticate.multifactor.remember.browser.default` system property the default value of the check box can be set to true.
    -   Navigate to **Multi-factor Authentication** &gt; **Properties** and adjust these four properties to control the remembered browser feature.![Property changes](../images/mfa-enforcement-property-change.png)
7.  How does MFA work for accounts shared by users?

    Single accounts shared by multiple users are a security risk. It isn’t recommended to share an account with multiple users.


