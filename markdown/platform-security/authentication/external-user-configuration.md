---
title: Configure a user registration configuration for external users
description: Create a user registration configuration record to bootstrap the onboarding process of external users to custom ServiceNow applications. This form guides the external users through the self-registration process.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Self-register to ServiceNow instance, Authentication, Access Management]
---

# Configure a user registration configuration for external users

Create a user registration configuration record to bootstrap the onboarding process of external users to custom ServiceNow applications. This form guides the external users through the self-registration process.

## Before you begin

-   Role required: external\_user\_self\_registration\_admin
-   [Activate External User Self-Registration](external-user-registration-plugin.md)

## Procedure

1.  Navigate to **All** &gt; **External User Self-Registration** &gt; **User Registration Configurations** and click **New**.

2.  On the form, fill in the fields.

<table id="table_nxl_s1m_nlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the registration form. For example, a student parking registration might be Parking Management Students.

</td></tr><tr><td>

Roles assigned to provisioned users

</td><td>

Roles assigned to the provisioned users. The specified roles have to extend or contains the `snc_external` role. The specified role can also be `snc_external` role. For external users, each role must have an `snc_external` to notate an external user. If you have pre-configured roles, the roles should be accessible when you unlock the roles and search for users.

</td></tr><tr><td>

Enable terms and conditions

</td><td>

Option to add a terms and conditions URL to the registration page.

</td></tr><tr><td>

Terms and conditions URL

</td><td>

The publicly accessible URL which contains the terms and conditions of the registration form. This field appears only when **Enable terms and conditions** is selected.

</td></tr><tr><td>

Description

</td><td>

The description of the registration form. This field appears only when you save or submit the configuration. You can add more information about the registration form in this field.**Note:** You can only add a description after you save or update a user registration configuration.

</td></tr><tr><td>

Application

</td><td>

Application containing this record. The application is automatically set to `Global`.

</td></tr><tr><td>

Active

</td><td>

Option which makes the user registration configuration active. This option is selected by default.

</td></tr><tr><td>

Enable CAPTCHA

</td><td>

Option to add a CAPTCHA to the registration form. The default CAPTCHA provider is Google reCAPTCHA.**Note:** To enable CAPTCHA for user registration, follow the steps in [Configure Google reCAPTCHA for external user self-registration](configure-recaptcha-sp.md).

</td></tr></tbody>
</table>3.  Click **Submit**.

    A user registration configuration with the default settings is created.

    ![User Registration Configuration form](../images/user-registration-configuration.png)

4.  Configure the **Registration** tab to show fields and the order that they appear:

    |Column|Description|
    |------|-----------|
    |Display in Registration Form|Set any field you want to display as `True`.|
    |Order|Set an order number to display fields on your form.|
    |Mandatory|Set any field you want to make it mandatory as `True`.|
    |Validation only field|Set any field you want to use only for validation. For example, registration code.|

    You can choose to display the default form fields or you can add custom form fields to the Registration Form. For more information, see [Default registration form fields](../reference/default-reg-form-fields.md).

    ![Registration tab of User Registration Configuration](../images/registration_tab_EU_self-registration.png "Registration tab")

    You can also add custom registration form fields. For more information, see [Add a custom registration form field](add-custom-reg-form-field.md).

5.  Configure the **Verification** tab to verify the identity of the registered users. When the user verification flow triggers, an activation link is sent to the user's registered email address.

<table id="table_bwt_ckb_vlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires user verification

</td><td>

Option to trigger a user verification subflow which runs after user registration. The subflow is for user identity verification.

</td></tr><tr><td>

User verification flow

</td><td>

The subflow used to verify the identity of the user. The subflow triggers only when you enable user verification.The **External User Verification** subflow is available by default. You can create a copy of the default subflow in Workflow Studio and modify it according to your requirements. For more information, see[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md) .

 **Note:** To preview the **External User Verification** subflow in a new tab use the following shortcuts:

-   Macintosh: Command + Click
-   Windows: Control + Click


</td></tr><tr><td>

Activation link expiry time \(in hours\)

</td><td>

The number of hours after which an activation link expires. The default value is 24.

</td></tr></tbody>
</table>    ![Verification tab of User Registration Configuration](../images/verf_tab_EU_self-reg.png "Verification tab")

6.  Configure the **Transformation** tab to map self-registered users and activated users.

    There are two transformation maps \(u\_reg\_xmap\_\[number\]\) which automatically map the registered users from the User Acti Req \[number\] table to the Self Registered User \[number\] table. You can create a copy of these default transformation maps and modify the map according to your requirements. For more information, see [Transform maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_CreatingNewTransformMaps.md).

    ![Transformation tab of User Registration Configuration](../images/transf_tab_eu_self-reg.png "Transformation tab")

7.  Configure the **Onboarding** tab to trigger subflows for onboarding activated users.

    The default **External User Onboarding** subflow sends an email to the user that contains a link to reset their password. You can create a copy of the default subflow and modify it according to your requirements.

    **Note:** When the **External User Onboarding** subflow triggers, the subflow sends an email to the user that contains a link to reset the password.

    ![Onboarding tab of User Registration Configuration](../images/onboard_tab_eu_self-reg.png "Onboarding tab")

8.  Configure the **Advanced** tab to map user tables and redirection pages of the registration form.

    ![Advanced tab of User Registration Configuration](../images/advanced_tab_eu_self-reg.png "Advanced tab")

    |Field|Description|
    |-----|-----------|
    |Registration table|Name of the table where registration form information is saved.|
    |Registration form field configuration|The record associated to the registration form in the Record Producer.|
    |Activation table|Label and name of the table used for user activation. The activation table contains records of the users who have completed verification.|
    |User table|Label and name of the user profile table.|
    |Activation success page|The page to which a user redirects after the activation is successful.|
    |Activation error page|The page to which a user redirects when the activation fails.|
    |Post registration redirect page|The page to which user is redirected after registration.|
    |Registration link label|The button name used for registration from the service portal. The default value is Register.|

    While making changes or after completing all changes in the user registration configuration, you can use the **Preview Registration Form** button to preview changes in the registration form.


