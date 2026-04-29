---
title: Configure FIDO2 as an MFA factor
description: Configure policy input and condition to display FIDO2 as an MFA factor policy for authentication.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [FIDO2 as an MFA factor, MFA factor policies, MFA verification methods, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure FIDO2 as an MFA factor

Configure policy input and condition to display FIDO2 as an MFA factor policy for authentication.

## Before you begin

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **MFA Context**.

2.  Select the **MFA Factor Policies** tab.

3.  Select the **Display FIDO2 as an MFA Factor Policy**.

4.  Select **New** to add **Policy Inputs**.

5.  Select the filter criteria that you want to create.

    Following are the types of filter criteria:

    -   [IP Filter Criteria](create-ip-filter-criteria.md)
    -   [Role Filter Criteria](create-role-filter-criteria.md)
    -   [Group Filter Criteria](create-group-filter-criteria.md)
    For example, Role Filter Criteria.

    ![Filter Criteria.](../images/mfa-email-filter.png)

6.  Select **Role Filter Criteria**, fill the fields for the role filter criteria and submit the record.

    The new policy is created. For more information, see [Role Filter Criteria](create-role-filter-criteria.md).

    Let's take an example of using **ITIL** role for the user \(**andrew.och**\) as the policy input and submit.

    ![Policy input](../images/mfa-fido-itil-role.png)

7.  On the Policy - Display FIDO2 as an MFA Factor Policy page, select **Policy Conditions**.

8.  Select **New** to add policy conditions.

9.  On the form, fill in the fields.

<table id="table_mxz_wyp_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name to identify the condition.

</td></tr><tr><td>

Description

</td><td>

Description of the condition.

</td></tr><tr><td>

Condition

</td><td>

Logical combination of multiple policy inputs \(filter criteria\) that is used to evaluate authentication requests.Select the role-based filter criteria policy that was created for the condition.

</td></tr></tbody>
</table>    ![MFA FIDO - Policy conditions](../images/mfa-fido-itil-role-condition.png)

10. Select **Submit**.

    Based on the policy input and condition, if the user \(**andrew.och**\) tries to log in to the instance, the user is shown as the FIDO screen to either enroll and register.

    ![MFA- Biometric or Hardware keys](../images/biometirc-mfa.png)

    To know more about different configuration example and user behaviors, see [Example Configurations and User Behaviors](../concept/mfa-with-fido.md#section_ovx_pgx_bgc).

11. Repeat step 8 to create additional policy conditions.

    **Note:** If you create multiple policy conditions, the final output of the access policy depends on the logical OR output of the all policy conditions. Based on the conditions the policy is evaluated.


