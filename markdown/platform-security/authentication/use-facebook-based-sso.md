---
title: Use Facebook-based Single Sign-On \(SSO\)
description: Log in to your ServiceNow instance by using your Facebook credentials on the Facebook-based SSO.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [OIDC as a SSO identity provider, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Use Facebook-based Single Sign-On \(SSO\)

Log in to your ServiceNow instance by using your Facebook credentials on the Facebook-based SSO.

## Before you begin

The Facebook-based SSO is shipped along with your ServiceNow instance.

You can define the Identity Provider \(Idp\) configurations to the **OIDC\_Facebook** IdP as your **Identity Providers**. For more information about Idp configurations, see [Configure a Facebook-based Single Sign-On \(SSO\)](configure-facebook-based-sso.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select **OIDC\_Facebook**.

3.  On the OIDC\_Facebook page, specify the following fields:

    **Note:**

    -   Most of the fields are auto-populated when using the default IdP.
    -   Details of the ServiceNow Homepage must be provided.
    -   User-related details such as Client ID and Client Secret from Facebook must be provided within the IdP.
<table id="table_gtj_4r3_jrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the OIDC IdP record. Enter `OIDC_Facebook`.

</td></tr><tr><td>

Default

</td><td>

Option to set the OIDC IdP configuration as default.

</td></tr><tr><td>

OIDC Entity Profile

</td><td>

OAuth Entity Profile for the OIDC configuration. Enter `Facebook default_profile`.

</td></tr><tr><td>

External logout redirect

</td><td>

The URL where the integration redirects users after they log out. Typically, this URL is the portal that is used for SSO. This field is automatically set to **external\_logout\_complete.do**. For example, `https://<yourinstance>.service-now.com/external_logout_complete.do`.

</td></tr><tr><td>

Active

</td><td>

Option to make the OIDC IdP configuration active.**Note:** This option can only be set to active after a successful test connection.

</td></tr><tr><td>

Auto Redirect IdP

</td><td>

Option to enable automatic redirection of the users to the login page of the identity provider.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

The URL of the login page that is used for authentication. This field is automatically set to your instance URL. The format of the URL is `https://<yourinstance>.service-now.com/navpage.do`

</td></tr><tr><td>

Show as Login option

</td><td>

Option to display the OIDC IdP as a login option on the login page. In this case, the login option appears as the **Login with Facebook** button.

</td></tr><tr><td>

SSO Label

</td><td>

Label of the OIDC IdP displayed on the login page. This field appears only when **Show as Login option** is enabled.

</td></tr><tr><td>

Logo URL

</td><td>

Publicly available URL that contains the logo of the OIDC IdP provider. This field appears only when **Show as Login option** is enabled.

</td></tr></tbody>
</table>    ![OIDC Facebook](../images/oidc-facebook.png)

4.  Open the **User Provisioning** tab, and fill in the fields.

    **Note:** You must configure the OIDC-related information such as Client ID and Client Secret of your users from Facebook.

<table id="table_bfv_frd_4z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatically provision users

</td><td>

Option to enable automatic user provisioning. This property creates a user in the instance User \[sys\_user\] table when the user exists on the IdP but doesn’t exist in the User table.**Note:** You can choose to enable automatic user provisioning during user login. When automatic user provisioning is enabled, a user record is automatically created in the ServiceNow instance if that user record doesn’t exist.

</td></tr><tr><td>

Provision using

</td><td>

The data source to use to transform to a ServiceNow user. Choices are as follows:-   **An ID Token**
-   **User Info endpoint**
-   **Both ID Token and User Info**
 Use the Lookup list to select the pre-defined data source template, then open the record to configure the Transforms table mapping.

</td></tr><tr><td>

Provision data source

</td><td>

The ID token data source that is used for user provisioning.

</td></tr><tr><td>

User Info Datasource

</td><td>

The user info endpoint data source used for user provisioning. This field appears only when **User Info** or **Both ID Token and User Info** is selected from the **Provision using** field.

</td></tr><tr><td>

Update User on next login

</td><td>

Option to enable user updates during the next login.

</td></tr><tr><td>

Update User Interval Time \(Seconds\)

</td><td>

Minimum time interval \(in seconds\) to update a user record between subsequent logins. This field is automatically set to 3600 seconds. For example, after a user logs in, the user record will be updated after 3,600 seconds until the next login. This field is available only when the **Update User on next login** field is enabled.

</td></tr><tr><td>

User roles applied to provisioned users

</td><td>

List of roles applied to the newly provisioned users.

</td></tr></tbody>
</table>5.  In the **OIDC Entity** tab, view and modify the OIDC client configuration and OIDC connect flow using the entity record.

    For more information related to OIDC-based configuration, see [Configure an OAuth OIDC provider for accepting third-party token](../../../administer/security/task/add-OIDC-entity.md)

6.  In the **OIDC Provider Configuration** tab, view and modify the well-know configuration URL of the OIDC IdP.

7.  Open the **Advanced** tab, and fill in the fields.

    |Property|Description|
    |--------|-----------|
    |Single Sign-On Script|The script that executes during Single Sign-On.|
    |Logout Script|The script that executes after the user logs out.|

    **Note:** Scripts are run during single sign-on and logout.

8.  To enable and test the configuration, click **Active**.

9.  To update the record, click **Update**.

    The Facebook-based login option is displayed on the login form.

10. When logging in on the login form, do the following:

    1.  Select the Facebook option.

    2.  To log in to the ServiceNow instance, specify your Facebook credentials.


