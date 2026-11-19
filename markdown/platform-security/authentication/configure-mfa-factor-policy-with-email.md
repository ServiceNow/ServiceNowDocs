---
title: Configure Email as an MFA factor
description: Configure policy input and condition to display Email OTP as an MFA factor policy for authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/configure-mfa-factor-policy-with-email.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Email as an MFA factor, MFA factor policies, MFA verification methods, Configure MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure Email as an MFA factor

Configure policy input and condition to display Email OTP as an MFA factor policy for authentication.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **MFA Context**.

2.  Click **MFA Factor Policies** tab.

    **Note:** The **EMAIL** as **MFA Factor with a Policy** is available by default. You can edit the policy and specify the policy inputs and conditions.

3.  Select the **Display Email OTP as an MFA Factor Policy**.

    \[Omitted image "email-factor.png"\] Alt text: Email - Factor

4.  Click **New** to add **Policy Inputs**.

5.  Select the filter criteria that you want to create.

    Following are the types of filter criteria:

    -   [IP Filter Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-ip-filter-criteria.md)
    -   [Role Filter Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-role-filter-criteria.md)
    -   [Group Filter Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-group-filter-criteria.md)
    For example, Role Filter Criteria.

    \[Omitted image "mfa-email-filter.png"\] Alt text: Filter Criteria

6.  Click **Role Filter Criteria**, fill the fields for the role filter criteria and submit the record.

    The new policy is created. For more information, see [Role Filter Criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-role-filter-criteria.md).

7.  On the Policy - Display Email OTP as an MFA Factor Policy page, click **Policy conditions**.

8.  Click **New** to add **Policy Conditions**.

9.  On the form, fill in the fields:

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

Logical combination of multiple policy inputs \(filter criteria\) that is used to evaluate authentication requests.Select the role based filter criteria policy that was created for the condition.

</td></tr></tbody>
</table>10. Click **Submit**.

11. Repeat step 8 to create additional policy conditions.

    **Note:** If you create multiple policy conditions, the final output of the access policy depends on the logical OR output of the all policy conditions. This means the policy will evaluate to true if any one of your policy conditions is met.

    Based on the role filter \(users\) policy and the conditions specified for the role is matched, the Email MFA factor is shown as an options for authentication for the users.


