---
title: Time limited authentication with SMS - Twilio Tutorial
description: Set up time limited authentication with MFA factors such as SMS using Twilio.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Time limited authentication, Token based authentication \(User logins\), Authentication, Access Management]
---

# Time limited authentication with SMS - Twilio Tutorial

Set up time limited authentication with MFA factors such as SMS using Twilio.

## Before you begin

Role required: adaptive\_auth\_admin, user\_admin

Plugins required:

-   `com.snc.authenticate.time_limited_authentication` \(Time Limited Authentication\)
-   `com.snc.authentication.sms_mfa` \(Multi-factor authentication with SMS\)

**Note:** Time limited authentication \(TLA\) is very specific to ServiceNow instance, the customized links for users can only be created within ServiceNow.

The tutorial instructions provided enable the admin to provide a link-based login with SMS as second factor \(MFA\) for users with a specific role.

After a successful configuration, the system generates a link, and then shares the link with the user through notification \(Email/SMS\) channel. Clicking the link, the user is prompted to specify the OTP sent to Email or SMS factor based on user role \(configuration\).

**Note:**

-   TLA should always be followed by MFA and MFA should be enabled by admin using Adaptive Authentication for TLA login. To know more about how to configure MFA with Adaptive Authentication, see [Multi-factor Authentication context](../concept/mfa-auth-context.md).
-   TLA should be used for the users who have limited privileges.

## Procedure

1.  Creating a Twilio configuration.

    1.  Create a Twilio test account. For more information, see [Twilio](https://www.twilio.com/login).

    2.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **Twilio Direct Configuration**.

    3.  Provide the **Account SID** and **Auth token** \(created from Twilio\) and save the record.

    **Note:** You can create your own provider configuration and use that for TLA. In this example, it is Twilio. To know more about how to create a MFA provider configuration, see [Configure MFA Provider](configure-mfa-provider.md).

2.  Configuring and enabling Time limited authentication\(TLA\) record.

    1.  Navigate to **All** &gt; **Time Limited Authentication Config records** and click **New**.

    2.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the record.|
        |One time use|Enable to use the TLA link once.|
        |Expiry|Specify the seconds for the link expiry. The default is 45 minutes.|
        |Failed Redirect|Enter the URL to redirect users after a failed authentication.|
        |Single Sign-On Script|Details of the SSO script that you want to use.|
        |Active|Option to make the configuration active.|
        |Max login attempts|Specify the number of attempts allowed with the generated TLA link for login. Un-check the **One time use** checkbox to provide the max number of attempts.|
        |External logout redirect|Enter the URL to redirect users after logout.|

    3.  Click **Submit**.

        ![TLA Record](../images/tla-new-record.png)

    4.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Administration** &gt; **Properties** and enable the **Enable multiple provider SSO** property and **Save**.

3.  Allowing TLA to only a specific user persona using the post-authentication context policy.

    1.  Navigate to **Roles** and create a role. For example: remote\_worker.

    2.  Create a user with a valid email id and mobile number. To know how to create a user see, Create a user.

    3.  Assign the role to the user. To know how to assign the role to the user, see Assign a role to a user.

    4.  To create a role filter criteria, navigate to **All** &gt; **Adaptive Authentication** &gt; **Role Filter Criteria**, create a new filter **remoteworkerrole** and condition **Role is remote\_worker**.

        ![Role Filter Criteria](../../../administer/users-and-groups/task/role-filter-tla.png)

    5.  To add policy condition based on the deny policy context based on the IdP and role filter criteria, navigate to **All** &gt; **Adaptive Authentication** &gt; **Post Authentication Context**.

    6.  Click the information icon and **Open the Record**.

        ![Deny Policy](../../../administer/users-and-groups/task/tla-deny-policy.png)

    7.  In the Policy Input, click **Edit** and add the role \(remoteworkerrole\) and **Save**.

        ![Edit Members](../../../administer/users-and-groups/task/tla-edit-members.png)

    8.  In the Policy Condition, add the condition for the policy input and **Submit** the record.

4.  Configuring the step-up authentication policy - MFA context.

    1.  Navigate to **All** &gt; **Multi-factor Criteria**.

    2.  Select the **Role based multi-factor authentication** and add the role under Multi-factor Roles section and **Update**. In this example: **remote\_worker**.

        ![MFA - Role Criteria](../../../administer/users-and-groups/task/tla-mfa-criteria.png)

    3.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **MFA Context**.

    4.  Make sure the following:

        -   Default Policy field is **Step-up MFA Policy**
        -   Step-Up MFA Policy is **Step-up MFA Policy**
    5.  Click the Information icon and **Open Record**.

        ![Step-Up MFA Policy](../../../administer/users-and-groups/task/step-up-tla.png)

    6.  On the Step-Up MFA Policy form, in the Policy Inputs, click **Edit**.

    7.  Add the **Role based multi-factor authentication** to the list and **Save**. In this example, **remoteworkerrole**.

    8.  In the Policy Condition, click **Enforce MFA if Role based or User based MFA settings are true**.

    9.  In the Enforce MFA if Role based or User based MFA settings are true page, make sure **Role Based MFA** is **true**.

5.  Enforcing MFA to use SMS as a MFA factor policy.

    1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **MFA Context**.

    2.  On MFA Context page, click **MFA Factor Policies** and click on policy **Display SMS OTP as an MFA Factor Policy**.

    3.  Click **Edit** and add **remoteworkerrole** in the **Policy Inputs**.

    4.  Click **Policy Conditions** and create a Policy condition.

        ![SMS - condition](../../../administer/users-and-groups/task/tla-mfa-sms.png)

    5.  Click **Submit**.

        The TLA link generated and shared to the users assigned with **remoteworkerrole** as role will be promoted to use the SMS code as a second factor to login the instance.

6.  Enabling the other required properties.

    1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Properties**.

    2.  Enable the following check-boxes.

        -   **Enable Multi-factor authentication**
        -   **Enable Multi-factor Authentication with SSO**
    3.  Save the record.

    4.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **Properties**.

    5.  Enable the **Enable Authentication Policy** checkbox.

    6.  Save the record.

7.  Generating a TLA link – Example.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts – Background**.

    2.  Use the following API by providing user sysid and config id.

        `var tla=new global.TimeLimitedAuthentication(); gs.info(tla.generateNonce("user_sysid", "config1_sys_id","IAR2"));`

        **Note:** The source \(IAR2\) is not a mandatory parameter.

    3.  Query Parameter is returned as shown:

        `nonce=VCeinfboDt0M&glide_sso_id=b3277f1b44351110f8779b5a2d9909f3&user=3b0277d344351110f8779b5a2d99099a&source=IAR2`

    4.  Create a URL in the below format:

        `https://<instance-url> /login_with_sso.do?uri=<encoded url>& nonce=2olIQSxdgkjs&glide_sso_id=0c15bf09c3711110c5ec4e483c40dd7a&user=62826bf03710200044e0bfc8bcbe5df1&source=IAR `

8.  Click the URL, the following MFA screen is displayed for login.


