---
title: Integrating with Salesforce CRM
description: Integrating your Software Asset Management application with the Salesforce customer relationship management \(CRM\) services enable you to track your software subscriptions and to reclaim unused licenses.Register an application through the Salesforce admin portal.Create an integration profile to track software subscriptions and optimize licensing for the Salesforce CRM services.Create an integration profile for the first Salesforce organization for which you want to track software subscriptions and optimize licensing.Create an integration profile for each additional Salesforce organization that you want to track software subscriptions and optimize licensing for.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 23
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Salesforce CRM

Integrating your Software Asset Management application with the Salesforce customer relationship management \(CRM\) services enable you to track your software subscriptions and to reclaim unused licenses.

**Note:**

If you’re using Software Asset Workspace, use SaaS Playbook for integrating your ServiceNow instance with the Salesforce CRM. For more information about creating a Salesforce CRM integration profile through Playbook, see [Create a Salesforce CRM integration](../task/playbook-salesforce-crm.md).

The supported Salesforce CRM services include

-   Salesforce Sales Cloud
-   Salesforce Service Cloud
-   Salesforce Platform
-   Salesforce Customer Community
-   Salesforce Partner Community
-   Salesforce Company Community
-   Salesforce Chatter

Both Salesforce Classic and Salesforce Lightning organizations are supported.

**Note:** You can track entitlements for other services that you pay for but aren’t user subscription based by using custom license metrics. See [Add a custom license metric](../task/add-custom-license-metric.md) for more details on how to create a custom license metric.

The Salesforce account that you use to connect the integration requires a Salesforce user license and the following user access permissions.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Salesforce CRM application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

User with the following permissions:-   View Setup and Configuration
-   API Enabled

</td><td>

Application with grant type **Authorization code**:

-   manage your data \(api\)
-   Perform requests on your behalf at any time \(refresh\_token, offline access\)

 Application with grant type **Client Credentials**: manage your data \(api\)

</td></tr><tr><td>

Pull user activity

</td><td>

User with the following permissions:-   View Setup and Configuration
-   API Enabled

</td><td>

Application with grant type **Authorization code**:

-   manage your data \(api\)
-   Perform requests on your behalf at any time \(refresh\_token, offline access\)

 Application with grant type **Client Credentials**: manage your data \(api\)

</td></tr><tr><td>

Reclaim subscription

</td><td>

User with Admin permissions

</td><td>

Application with grant type **Authorization code**:

-   manage your data \(api\)
-   Perform requests on your behalf at any time \(refresh\_token, offline access\)

 Application with grant type **Client Credentials**: manage your data \(api\)

</td></tr><tr><td>

Download consumption

</td><td>

User with the following permissions:-   View Setup and Configuration
-   API Enabled

</td><td>

Application with grant type **Authorization code**:

-   manage your data \(api\)
-   Perform requests on your behalf at any time \(refresh\_token, offline access\)

 Application with grant type **Client Credentials**: manage your data \(api\)

</td></tr></tbody>
</table>These are optional permissions that may be required when minimum permissions are restricted due to your organization's security policies.

|Permission|Enabled|Description|
|----------|-------|-----------|
|View Developer Name|Yes|Allows you to view the DeveloperName field via the API. Salesforce APIs.|
|Manage Internal Users|Yes|Allows you to create and modify internal users. Allows you to view Setup pages.|
|Manage Users|Yes|Allows you to create, edit, and deactivate users. Additionally, you can manage security settings, including profiles and roles.|
|View All Profiles|Yes|Allows you to view all user profiles regardless of the profile filter settings.|
|View All Users|Yes|Allows you to view all users regardless of the sharing settings.|

For additional information on the Salesforce CRM services, see the [Salesforce Developer Documentation](https://developer.salesforce.com/docs/).

The **Client Credentials** grant type is supported in Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 16.1.0, Salesforce CRM application 2.0.2, and Salesforce CRM Spoke 2.4.0 version onwards.

## Register a Salesforce application

Register an application through the Salesforce admin portal.

### Before you begin

Salesforce Role required: admin

### Procedure

1.  Log in to [Salesforce](https://login.salesforce.com/?startURL=%2Fsetup%2Fsecur%2FRemoteAccessAuthorizationPage.apexp%3Fsource%3DCAAAAWd_ycj7ME8wMHkwMDAwMDA4T0k2AAAA2CFKH_C6K2jEXMcAAa95DHha0KQ0IeY1ykrwEVRkz67RUi8i4a0jM7Vp8V21BaS_L33r3duBQbWQwqlyiK2ggRW4EpVHap4wptWMLW6rSLEX9sFPr9tx-KL10Co6XYnGi6obC4k1a5vaO0N2nCjm2hZZ9ncAxKjFL7Dg5Yn93smtqoQquTJlPn85UW8f4CtFFRxNmMkvCs8fsBriDWCmolMpA7RSre5FgwDVuhOsLTVi7WcOvYa9KQof9RQDptCwsh3emhXvc0b4eIr_mTHD1q-yCB8LCgtH3PZLh7NlpywhUjvaEcqLC1LIaM-s7zxbvNdJnNiYx7ZBVMgvLc7KuHqTrJqnKEHVqRUAQjDbpNHV7IIsiviaGhEnY1uwJM84XtO2z2NYSjT-ANIriMblKQXaVGMucWCSZjvvT-XzrgEUPQCK6ZloS4-icbOjf7dNOIWxBR_Ps6Ux3mmvZE8wsABMyFuPAa0lJr9JLsS1EYT_LXBJSWGZ8GajEk55_zQzkxZzWRX5H5nkqxXu6xIVqNVUdS6DkiK4SSJ0nkLEFyQ3HoAVdWxegmYkcqVgy0KupBs-i2KSW47vgr6D3dU0pWhPaLkf10V3m1kd_C3ZL6ic8MS4_lUtsoyR7T9NbpRdeQ1gERuDu-tRSVgdcPkVi9Kxn9DUvhuFiQx1Cs8F2tcqE417kbJqONd7_2M1UL9b5Wy3s_T5SD1tbjsi9hwvEK1hfIe-JmxykwGgIZRT5Q4rQ-GlkJWxSiIxZOJrWI5ZoNbZX7_GIcC01InFN8OMveE1EAvO4JuC3KZ8Yxwypmr5jUYqzQLOLWhDB5mjoEwdFbns1PQtgwwkFjRnfEI90yysbVMQwMq2X8rp75vc-KDMrqTWyALTkVDbxsyuMWfLqUZ5NFaHggbtwQO7fK9o3ZESzswI6YBZWnzbEmHYaOPjbSIulXe7XjbLVLEMEXyLyr3V7PAPtGv_t3Y0mEG0NeenO_pi3NfUFxgvTZo571hgbEVqSvEdgtJWzTLYN0VxKIf7iYcJwO_zRRPCEA4vpJqha-ppCesm1EwjzdQPj7g0lh7G4faQ4916YDLiJCH2MFPTzyz4z4ib0Zg4ejnPPt3v7xWDenkSL6SiD8PgYSA7zPiTZSuMbXt0TOVXyIhg-RsVaDx9Nlv1Jz5NdDWXUWsxk_vI6LJv63Ib_Ky-X6yalB2bY-Y5GyuthFOpIgEjv1P-NurpdZkHdfKR3EdxgBzpnl35XW2M_7oyz9M0CK1MbxaYlgS6t0LVKkXJC21oMaMnykekz7coxVVZxg94Y28J_zZ0Hk75Xj4yuwRc04XSWvwhyDvaYGV5cR7zXeimrMmMylEBYQOxr7-UBSzxoSuLIJWuDxW2qaIwwW8s134O1U62SPYe-l6m1vzq3AZ6vlYpkngznqLjS6iVruD2qbw%253D&sdtd=1).

    You can also switch from the Lightning UI.

2.  Select the setup icon ![Personalize list icon.](../image/gear-icon.png) and then select **Setup**.

3.  Search for and select **App Manager** in the setup page search bar.

4.  On the App Manager page, select **New External Client App** to create an external client application.

5.  On the form, fill in the fields.

<table id="table_ylm_f1h_1gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic Information

</td></tr><tr><td>

External Client App Name

</td><td>

Name of your application.

</td></tr><tr><td>

API Name

</td><td>

Name of the API. This field is automatically populated.

</td></tr><tr><td>

Contact Email

</td><td>

The email address that you want to associate with the application.

</td></tr><tr><td>

Distribution State

</td><td>

The scope of distribution of the application.Select **Local** as the distribution state.

</td></tr><tr><td>

Contact Phone

</td><td>

The phone number that you want to associate with the application.

</td></tr><tr><td>

Info URL

</td><td>

The URL of the web page with more information about your application.

</td></tr><tr><td>

Logo URL

</td><td>

The URL of your logo image that is displayed with the connected application.

</td></tr><tr><td>

Icon URL

</td><td>

The URL of the icon for the connected application.

</td></tr><tr><td>

Description

</td><td>

Description of the application.

</td></tr><tr><td class="sub-head" colspan="2">

API \(Enable OAuth Settings\)

</td></tr><tr><td>

Enable OAuth

</td><td>

Option to enable OAuth settings.Select this option to enable the OAuth settings.

</td></tr><tr><td>

Callback URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

</td></tr><tr><td>

OAuth Scopes

</td><td>

OAuth scopes that determine the amount of access that is granted to an access token. When the grant type is **Authorization Code**, use:

-   **Manage user data via APIs \(api\)**
-   **Perform requests at any time \(refresh\_token, offline\_access\)**
When the grant type is **Client Credentials**, use **Manage user data via APIs \(api\)**.

</td></tr><tr><td class="sub-head" colspan="2">

Flow Enablement

</td></tr><tr><td>

Enable Client Credentials Flow

</td><td>

Select this option when the grant type is **Client Credentials**.

</td></tr><tr><td class="sub-head" colspan="2">

Security

</td></tr><tr><td>

Require Secret for Web Server Flow

</td><td>

The option to implement the Require Secret for Web Server Flow in your external client app or connected app settings.-   If the grant type is **Authorization Code**, select this option.
-   If the grant type is **Client Credentials**, clear this option.


</td></tr><tr><td>

Require Secret for Refresh Token Flow

</td><td>

The option in your external client app or connected app while implementing the refresh token flow using a server-side callback handler.-   If the grant type is **Authorization Code**, select this option.
-   If the grant type is **Client Credentials**, clear this option.


</td></tr><tr><td>

Require Proof Key for Code Exchange \(PKCE\) Extension for Supported Authorization Flows

</td><td>

Clear this option.

</td></tr></tbody>
</table>6.  Select **Create**.

    The application registration is complete and you're redirected to the Manage External Client Apps page.

7.  Verify and edit the policies for the registered application by selecting **Edit**.

8.  In the OAuth Policies section, verify that the **Permitted Users** field is set to **Admin approved users are pre-authorized** for the ServiceNow application.

    **Note:** Admin-approved users who are preauthorized enable any users with the corresponding profile or permission set to access the application without prior authorization. For more information, see [Pre-Authorize User App Access Through Connected App Policies](https://help.salesforce.com/s/articleView?id=xcloud.branded_apps_allow_deny_con_app.htm&type=5).

9.  In the App Policies section, select either the profile of the integration user or the profile of the user that you want to use for the integration.

10. If you have selected the **Enable Client Credentials Flow** option, then in the OAuth Flows and External Client App Enhancements section, select **Enable Client Credentials Flow** and enter either the username or email address of the integration user that you want to use for the integration profile.

11. In the App Authorization section, verify that the **Refresh token policy** field is set to **Refresh token is valid until revoked** and the **IP Relaxation** field is set to **Relax IP restrictions**.

12. Select **Save**.

13. Retrieve OAuth credentials.

    1.  Navigate to **Settings** &gt; **OAuth Settings** and then select **Consumer Key and Secret**.

        The Salesforce login page opens in a new window.

    2.  Enter your credentials to log in to Salesforce.

    3.  Copy the **Consumer Key** and **Consumer Secret** and save them in a secure location for later use.


## Create a Salesforce CRM integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Salesforce CRM services.

**Note:** You must create Salesforce CRM integration only in the Global scope.

### Create your first Salesforce CRM integration profile

Create an integration profile for the first Salesforce organization for which you want to track software subscriptions and optimize licensing.

#### Before you begin

To create a Salesforce CRM integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Software Asset Management integration with Salesforce CRM** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

#### About this task

If you’re using Software Asset Workspace, the option to create the Salesforce CRM integration profile in Core UI is inactive.

If you’re using Software Asset Workspace, use SaaS Playbook for integrating your ServiceNow instance with Salesforce CRM. For more information about creating a Salesforce CRM integration profile through Playbook, see [Create a Salesforce CRM integration](../task/playbook-salesforce-crm.md).

#### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d335038e1206">

Interface

</th><th align="left" id="d335038e1209">

Action

</th></tr></thead><tbody><tr><td id="d335038e1215">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Salesforce CRM Integration Profile**.


</td></tr><tr><td id="d335038e1258">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Salesforce CRM** from the drop-down list.
4.  Select **Continue**.

The Playbook launches for Salesforce CRM integration and the next steps aren't valid. For more information, see [Create a Salesforce CRM integration](../task/playbook-salesforce-crm.md).

</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td id="display-name">

Display name

</td><td id="display-name-def">

Name of the integration profile. Enter a name that uniquely identifies the Salesforce organization for which you’re creating this integration profile. For example, `SFDC Org1`.

**Tip:** Keep this name short to help it displays better during reporting.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr id="row_nn5_st5_bgb"><td id="profile-type">

Profile type

</td><td id="profile-type-def">

Type of integration profile. This value is automatically set to **Salesforce CRM Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-salesforce-crm.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

    3.  On the **Download Consumption Subflow** tab, verify that the **Subflow** field is set to **Salesforce CRM Download Consumption**.

4.  Select **Save**.

    **Note:** The Calculate Activity Subflow isn’t required for Salesforce CRM integrations because these integrations use information about last user login from the user records.

    Your instance creates a draft integration profile. You can view consumption counts for the specific consumption based Salesforce CRM application.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_sforce\_v2\_spoke.Salesforce**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field to configure the child alias.

6.  Select **Open Record** in the record preview.

7.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

8.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_nng_qhr_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the connection. Enter a name that uniquely identifies the Salesforce organization for which you’re creating this connection and credential. For example, `SFDC Org1`.

</td></tr><tr><td>

Connection URL \(Instance URL\)

</td><td>

URL that displays after logging in to Salesforce or your custom domain URL of Salesforce.

</td></tr><tr><td class="sub-head" colspan="2">

Credential information

</td></tr><tr><td>

Grant type

</td><td>

The grant type for your application according to your authentication needs. Possible values are: -   **Authorization Code**
-   **Client Credentials**


</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID \(consumer key\) that is assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret \(consumer secret\) that is assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This is generally the URL of the ServiceNow instance that you specified in [Register a Salesforce application](integrate-with-salesforce-crm.md#).

</td></tr></tbody>
</table>9.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-salesforce-crm.md#) table.

10. In the OAuth2 dialog box, log in to the same Salesforce admin account that you used to create your Salesforce application.

    **Tip:** If the dialog box doesn’t open automatically, check to make sure that pop-ups are allowed on your browser.

    If you have selected **Client Credentials** as the grant type, the OAuth2 dialog box doesn't appear.

    Your ServiceNow instance creates an OAuth token for Salesforce.

11. Return to your integration profile by navigating to **SaaS License** &gt; **Administration** &gt; **Direct Integration Profiles** and then selecting the profile from the Integration Profiles list.

12. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

13. After the connection is verified, select **Publish**.

14. In the Publish Confirmation dialog box, select **OK**.


#### Result

After you publish the integration profile, your ServiceNow instance begins retrieving data from your Salesforce CRM services. For organizations with fewer than 100 users, this process typically takes only a few minutes to complete. For organizations with 100–5000 users, this process can take around 15 minutes to complete. For organizations with over 5000 users, this process can take over one hour to complete.

#### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

### Create additional Salesforce CRM integration profiles

Create an integration profile for each additional Salesforce organization that you want to track software subscriptions and optimize licensing for.

#### Before you begin

To create a Salesforce CRM integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Software Asset Management integration with Salesforce CRM** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

#### About this task

If you’re using Software Asset Workspace, the option to create the Salesforce CRM integration profile in Core UI is inactive.

#### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d335038e2137">

Interface

</th><th align="left" id="d335038e2140">

Action

</th></tr></thead><tbody><tr><td id="d335038e2146">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Salesforce CRM Integration Profile**.


</td></tr><tr><td id="d335038e2189">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Salesforce CRM** from the drop-down list.
4.  Select **Continue**.

The Playbook launches for Salesforce CRM integration and the next steps aren't valid. For more information, see [Create a Salesforce CRM integration](../task/playbook-salesforce-crm.md).

</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td id="display-name">

Display name

</td><td id="display-name-def">

Name of the integration profile. Enter a name that uniquely identifies the Salesforce organization for which you’re creating this integration profile. For example, `SFDC Org2`.

**Tip:** Keep this name short to help it display better during reporting.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr id="row_nn5_st5_bgb"><td id="profile-type">

Profile type

</td><td id="profile-type-def">

Type of integration profile. This value is automatically set to **Salesforce CRM**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-salesforce-crm.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

    3.  On the **Download Consumption Subflow** tab, verify that the **Subflow** field is set to **Salesforce CRM Download Consumption**.

4.  Select **Save**.

    **Note:** The Calculate Activity subflow isn’t required for Salesforce CRM integrations because these integrations use information about last user logins from the user records.

    Your instance creates a draft integration profile. You can view consumption counts for the specific consumption based Salesforce CRM application.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_sforce\_v2\_spoke.Salesforce**.

5.  Select the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field to open the connection &amp; credential aliases record.

6.  Select **Open Record** in the record preview.

7.  On the Connection &amp; Credential Aliases form, create a child alias that can uniquely identify the connection and credentials for this integration profile.

    The first Salesforce CRM integration profile that you create uses the default \(parent\) connection and credential alias for Salesforce. Each additional Salesforce CRM integration profile that you create requires a unique child alias that helps differentiate the connection and credentials between each integration profile.

    1.  Select the link under **Child Aliases** &gt; **Parentalias=\*\*\*** to add child aliases.

    2.  Select **New**.

        The Connection &amp; Credential Aliases form for the child alias opens.

    3.  Enter a name for the child alias in the **Name** field.

    4.  Select and hold \(or right-click\) the form header and then select **Save**.

    5.  After the form reloads, select the **Create New Connection &amp; Credential** related link.

    6.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_nng_qhr_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the connection. Enter a name that uniquely identifies the Salesforce organization for which you’re creating this connection and credential. For example, `SFDC Org2`.

</td></tr><tr><td>

Connection URL \(Instance URL\)

</td><td>

URL of the Salesforce instance that you’re connecting to through this integration.

</td></tr><tr><td class="sub-head" colspan="2">

Credential information

</td></tr><tr><td>

Grant type

</td><td>

The grant type for your application according to your authentication needs. Possible values are:-   **Authorization Code**
-   **Client Credentials**


</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID \(consumer key\) that is assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret \(consumer secret\) that is assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication.This is generally the URL of the ServiceNow instance that you specified in [Register a Salesforce application](integrate-with-salesforce-crm.md#).

</td></tr></tbody>
</table>    7.  Select **Create and Get OAuth Token**.

        **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-salesforce-crm.md#) table.

    8.  In the OAuth2 dialog box, log in to the same Salesforce admin account that you used to register your Salesforce application.

        **Tip:** If the dialog box doesn’t open automatically, check to make sure that pop-ups are allowed on your browser.

        If you have selected **Client Credentials** as the grant type, the OAuth2 dialog box doesn't appear.

        Your ServiceNow instance creates an OAuth token for Salesforce.

8.  Return to your integration profile by navigating to **SaaS License** &gt; **Administration** &gt; **Direct Integration Profiles** and then selecting the profile from the Integration Profiles list.

9.  In the **Connection &amp; Credential** field of the Integration Profile form, select the lookup icon to locate and select the child alias that you created in [step 7](integrate-with-salesforce-crm.md#child-alias).

    Selecting the child alias associates the alias with the integration profile. Your ServiceNow instance uses this alias to identify the connection and credentials for this integration profile.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

11. After the connection is verified, select **Publish**.

12. In the Publish Confirmation dialog box, select **OK**.


#### Result

After you publish the integration profile, your ServiceNow instance begins retrieving data from your Salesforce CRM services. For organizations with fewer than 100 users, this process typically takes only a few minutes to complete. For organizations with 100-5000 users, this process can take around 15 minutes to complete. For organizations with over 5000 users, this process can take over one hour to complete.

#### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

