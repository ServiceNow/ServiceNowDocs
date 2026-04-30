---
title: Configure SMS as MFA factor
description: Configure policy input and condition to display SMS OTP as an MFA factor policy for authentication.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Multi-factor authentication with SMS, Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Configure SMS as MFA factor

Configure policy input and condition to display SMS OTP as an MFA factor policy for authentication.

## Before you begin

Plugin required: Multi-factor authentication with SMS \(`com.snc.authentication.sms_mfa`\).

Role required: admin

**Note:** The MFA context policy must be evaluated as `true` to apply the SMS factor policy.

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **MFA Context**.

2.  Click the **MFA Factor Policies** tab.

3.  Select the **Display SMS OTP as an MFA Factor Policy**.

    ![SMS - Factor](../images/sms-factor.png)

4.  Click **New** to add **Policy Inputs**.

    ![Policy Inputs](sms-mfa.png)

5.  Select the filter criteria that you want to create.

    Following are the types of filter criteria:

    -   [IP Filter Criteria](create-ip-filter-criteria.md)
    -   [Role Filter Criteria](create-role-filter-criteria.md)
    -   [Group Filter Criteria](create-group-filter-criteria.md)
    For example, Role Filter Criteria.

    ![Filter Criteria.](../images/mfa-email-filter.png)

6.  Click **Role Filter Criteria**, fill the fields for the role filter criteria and submit the record.

    The new policy is created. For more information, see [Role Filter Criteria](create-role-filter-criteria.md).

7.  On the Policy - Display SMS OTP as an MFA Factor Policy page, click Policy conditions.

    ![Policy form with Policy Conditions highlighted.](sms-mfa-condition.png)

8.  Click **New** to add **Policy Conditions**.

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
</table>10. Click **Submit**.

11. Repeat step 8 to create additional policy conditions.

    **Note:** If you create multiple policy conditions, the final output of the access policy depends on the logical OR output of the all policy conditions. This means that the policy evaluates to true if any one of your policy conditions is met.

    Based on the role filter \(users\) policy and the conditions specified for the role is matched, the SMS as MFA factor is shown as an option for authentication for the users.


