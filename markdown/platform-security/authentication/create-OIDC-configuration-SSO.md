---
title: Create an OpenID Connect \(OIDC\) configuration for Single Sign-On \(SSO\)
description: Create or update an OpenID Connect \(OIDC\) configuration by using the Multi-Provider SSO plugin.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [OIDC as a SSO identity provider, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Create an OpenID Connect \(OIDC\) configuration for Single Sign-On \(SSO\)

Create or update an OpenID Connect \(OIDC\) configuration by using the Multi-Provider SSO plugin.

OpenID Connect \(OIDC\) configuration for Single Sign-On \(SSO\)

## Before you begin

-   Register an OIDC application with your Identity Provider \(IdP\) and note the Client ID, Client Secret, and Well-known configuration URL.
-   [Activate Multi-Provider SSO plugin](t_ActivateMultipleProviderSSO.md). Multi-Provider SSO feature supports domain separation, you can specify different IdP's to different domains.
-   [Configure Multi-provider SSO properties](t_ConfigureMultiProviderSSOProps.md)
-   [Activate Approval with e-Signature plugin](activate-approval-esignature.md) to enable eSignature for the OIDC IdP.
-   Role required: admin

If you have a client ID, client secret, and well-known configuration URL of the identity provider, you can directly import the OIDC configuration for SSO.

**Note:**

-   The **Login with OIDC** button is not shown on the login page for OIDC based IDPs if the domain separation plugin is installed.
-   Admin can use OIDC based IdP to enable SSO for a user of specific company or domain.
-   ServiceNow support the JSON Web Encryption \(JWE\) as part of the OIDC SSO flow. To know more, see the [KB Article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2546935).

If you do not have the required information about the identity provider, you can manually configure OIDC for SSO. After completing the configuration, users can log in to ServiceNow applications using third-party social identity providers like Google Okta.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Choose one of the following options.

    -   To update an existing configuration, click an OIDC Identity Provider record.
    -   To create a new configuration, click **New** and select **OpenID Connect**.
3.  For a new configuration, enter the OIDC configuration information in one of the following methods.

<table id="choicetable_okg_pdd_4z"><tbody><tr><td id="d170086e168">

**Import OpenID Connect Well-Known Configuration**

</td><td>

If you have the well-known configuration URL along with your associated client credentials, you can directly import an OIDC configuration.**Note:** If you import the OIDC well-known configuration, all related fields are auto-populated.

</td></tr><tr><td id="d170086e180">

**Manually configure the OIDC Identity Provider form**

</td><td>

If you do not have an existing OAuth OIDC Entity, close the Import OpenID Connect Well-Known Configuration pop-up and manually fill the fields in the OIDC Identity Provider form.

</td></tr></tbody>
</table>    |Property|Description|
    |--------|-----------|
    |Name|Unique name for the OIDC identity provider configuration.|
    |Client ID|Client ID of the application registered in the third-party OIDC identity provider.|
    |Client Secret|Client secret of the application registered in the third-party OIDC identity provider.|
    |Well-known Configuration URL|URL that contains metadata about the third-party OIDC identity provider.|

    All required fields must be filled in on the OIDC Identity Provider form.

    Before you manually fill the OIDC Identity Provider form, ensure that you already have an OAuth Entity Profile for the OIDC IdP.

    If you do not have a OAuth Entity Profile, you can create it using the default External OIDC Provider templates, like Okta, Azure and others.

    The grant type of the OAuth Entity Profile must be with an authorization code. For more information, see [Configure an OAuth OIDC provider on the ServiceNow AI Platform](../../../administer/security/task/add-OIDC-entity.md).

    **Note:** You can use the templates of third-party identity providers, Auth0, Azure AD, Google, and Okta are available in the demo data of the Multiple Provider Single Sign-On Installer plugin.

<table id="table_lf5_c3d_4z"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the OIDC identity provider record.

</td></tr><tr><td>

Active

</td><td>

Option to make the OIDC IdP configuration active. **Note:** This option can only be set to active after a successful test connection.

</td></tr><tr><td>

Default

</td><td>

Option to set the OIDC IdP configuration as default when there are more than one OIDC configurations.

</td></tr><tr><td>

Auto Redirect IdP

</td><td>

Option to enable auto redirection of the users to the login page of the identity provider. This field shows when the **Set as Auto Redirect IdP** option is set under the Related Links section.**Note:** If you make a new Auto Redirect IdP configuration active, the **glide\_sso\_id** cookie automatically updates with the new Auto Redirect IdP. The **glide.authenticate.sso.update.idp.cookie**system property controls this feature.

</td></tr><tr><td>

OIDC Entity Profile

</td><td>

OAuth Entity Profile for the OIDC configuration.

</td></tr><tr><td>

ServiceNow Homepage

</td><td>

The URL of the login page used for authentication. This field is automatically set to your instance URL. The format of the URL is: `https://yourinstance.service-now.com/navpage.do`

</td></tr><tr><td>

External logout redirect

</td><td>

The URL where the integration redirects users after they log out. Typically, the portal, which is used for SSO. This field is automatically set to `external_logout_complete.do` For example, `https://yourinstance.service-now.com/external_logout_complete.do`

</td></tr><tr><td>

Show as login option

</td><td>

Option to display the OIDC IdP as a login option on the login page. The login option appears as the **login with Identity provider** button.

</td></tr><tr><td>

SSO label

</td><td>

Label of the OIDC IdP displayed on the login page. This field appears only when **Show as login option** is enabled.

</td></tr><tr><td>

Logo URL

</td><td>

Publicly available URL that contains logo of the OIDC IdP provider. This field appears only when **Show as login option** is enabled.

</td></tr></tbody>
</table>4.  Enable automatic user provisioning in the User Provisioning tab&gt;User Provisioning tab.

    You can choose to enable automatic user provisioning during user login. When automatic user provisioning is enabled, a user record is automatically created in the ServiceNow instance if that user record does not exist.

    |Property|Description|
    |--------|-----------|
    |Automatically provision users|Option to enable automatic user provisioning. This property creates a user in the instance User \(sys\_user\) table when the user exits on IdP but does not exist in the User table.|
    |Provision using|Data source to use to transform, an `ID Token`, `User Info` endpoint, or `Both ID Token and User Info` to a ServiceNow user. Use the Lookup list to select the pre-defined data source template, then open the record to configure the Transforms table mapping.|
    |Provision data source|ID token data source used for user provisioning.|
    |User Info Datasource|The user info endpoint datasource used for user provisioning. This field is displayed when `User Info` or `Both ID Token and User Info` are selected for the **Provision using** field.|
    |Update User on next login|Option to enable user update during the next login.|
    |Update User Interval Time \(Seconds\)|Minimum time interval in seconds to update a user record between subsequent logins. This field is automatically set to 3,600 seconds. For example, after a user logs in, the user record will be updated after 3,600 seconds until the next login. This field is available only when the **Update User on next login** field is enabled.|
    |User roles applied to provisioned users|List of roles applied to the newly provisioned users.|

5.  OIDC Entity tab

    You can view and modify the OIDC client configuration and OIDC connect flow using the entity record.

6.  OIDC Provider Configuration tab

    You can view and modify the well-know configuration URL of the OIDC IdP or ID token claim validation.

7.  Advanced tab

    Scripts that are run during single sign-on and logout.

    |Property|Description|
    |--------|-----------|
    |Single Sign-On Script|Script that executes during Single Sign-On. This field is automatically set to `MultiSSO_OIDC_custom`.|
    |Logout Script|Script that executes after the user logs out. This field is automatically set to `MultiSSO_OIDC_logout_custom`.|

8.  On the Continuous Authentication tab, configure the following fields:

    **Note:**

    -   The Continuous Authentication tab appears only when you install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) plugin that requires license.
    -   If you're using continuous authentication policy to protect access to table or data class, see [Continuous Authentication](../../authentication/concept/ca-homepage.md).
    ![Continuous Authentication - tab information](../../authentication/images/ca-tab-oidc.png)

<table id="table_klg_xrx_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Continuous Authentication Configured

</td><td>

Select the check-box to set the configuration active.

</td></tr><tr><td>

Continuous Authentication Consumer URL

</td><td>

Provide the Consumer URL from the Identity Provider.

</td></tr><tr><td>

Continuous Authentication Script

</td><td>

Select the look-up icon to choose the script provided from the platform. In this configuration, for OIDC Okta: **ContinuousAuth\_Okta\_StepUp\_Script**

</td></tr></tbody>
</table>9.  On the eSignature Approval tab, configure the eSignature for the OIDC Idp.

    **Note:** The eSignature Approval tab appears only when you install the **Approval with e-Signature** plugin \(com.glide.e\_signature\_approvals\).

    |Property|Description|
    |--------|-----------|
    |Assertion Consumer URL for eSignature authentication|If you employ a customized method of handling the OIDC authentication for eSignature, you can set up your own consumer URL. For example, if you are using Multi-Provider SSO, you do not need to use this property. This format of the URL is `https://yourinstance.service-now.com/consumer.do`|
    |Authentication pop-up Dialog Width|Width of the authentication pop-up dialog. This field is automatically set to `800`.|
    |Authentication pop-up Dialog Height|Height of the authentication pop-up dialog. This field is automatically set to `900`.|

10. Navigate to the login page of the instance to verify that IdP appears as a login option.

    The URL should be in the following format: `https://yourinstance/login_with_sso.do?glide_sso_id=sysId_IdP`

    **Note:** If you have enabled **Selected as login Option**, you can go to the login URL of the instance.


