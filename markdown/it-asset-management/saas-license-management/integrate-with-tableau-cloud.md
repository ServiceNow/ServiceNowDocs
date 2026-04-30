---
title: Integrating with Tableau Cloud
description: Integrating your Software Asset Management application with the Tableau Cloud application enables you to track your software subscriptions and to reclaim stale licenses.Register a Tableau Cloud application through the Tableau Cloud admin portal.Create an integration profile to track software subscriptions and optimize licensing for the Tableau Cloud service.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Tableau Cloud

Integrating your Software Asset Management application with the Tableau Cloud application enables you to track your software subscriptions and to reclaim stale licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Tableau Cloud application|Authentication scopes|
|-------|---------------------------------------------------|---------------------|
|Download subscriptions|site administrator|None|
|Pull user activity|site administrator|None|
|Reclaim subscription|site administrator|None|

## Register a Tableau Cloud application

Register a Tableau Cloud application through the Tableau Cloud admin portal.

### Before you begin

-   Activate the Tableau spoke. For more information, see [Tableau spoke](https://www.servicenow.com/docs/access?context=tableau-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
-   Tableau Cloud Role required: site administrator

### Procedure

1.  Use one of the following authentication types to validate ServiceNow instance requests with Tableau Cloud.

    -   Personal Access Token \(PAT\)
    -   JSON Web Token \(JWT\)
    1.  Validate ServiceNow instance requests with Tableau Cloud using the PAT authentication type.

        1.  Log in to the Tableau Cloud account using admin credentials.
        2.  Select your profile icon.
        3.  Select **My Account Settings**.
        4.  Scroll down to the **Personal Access Tokens** section on your profile page.
        5.  In the text field, provide a token name.

            For example, `Test 1`.

        6.  Select **Create Token**.

            The Personal Access Token is generated with a Token name and Secret.

        7.  To copy the Personal Access Token Secret, select **Copy Secret**.

            **Important:**

            Keep the Personal Access Token Secret at a secure place. You would need it when you create a connection record for Tableau.

    2.  Validate ServiceNow instance requests with Tableau Cloud using the JWT authentication type.

        1.  Log in to the Tableau Cloud account using admin credentials.
        2.  Select your profile icon.
        3.  From the left-pane, select **Settings**.
        4.  Select the **Connected Apps** tab.
        5.  On the Connected Apps page, select the **Direct Trust** option from the **New Connected Apps** drop-down list.
        6.  In the **Create Connected App** dialog box, fill in the Connected app name, Access level, and Domain allow list details.
        7.  Select **Create**.

            The Connected App that you created gets displayed on the Connected Apps page. By default, the Connected App is inactive.

        8.  To enable the Connected App, select the ellipsis icon \(![Ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg)\) next to the Connected App name and then select **Enable**.

            The status of the Connected App shows as enabled.

        9.  Select the Connected App name.

            Keep the Secret ID and Secret value at a secure place. You would need it when you create a connection record for Tableau.

        10. To copy the Client ID, select **Copy Client ID**.

            Keep the Client ID at a secure place. You would need it when you create a connection record for Tableau.


## Create a Tableau Cloud integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Tableau Cloud service.

### Before you begin

To create a Tableau Cloud integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

ServiceNow Role required: admin or sam\_integrator

**Important:** You must select the **Software Asset Management integration with Tableau** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using the Software Asset Workspace, the option to create the integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d39492e495">

Interface

</th><th align="left" id="d39492e498">

Action

</th></tr></thead><tbody><tr><td id="d39492e504">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Tableau Cloud**.


</td></tr><tr><td id="d39492e546">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Tableau Cloud** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_m4c_prp_qqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Tableau integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you haven't published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Tableau Cloud Subscription.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-tableau-cloud.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Tableau Cloud Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Tableau Cloud Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_tableau\_spoke.TableauCloud**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../../../common/image/Form_ReferenceLookupIcon.png)\) beside the **Connection &amp; Credential** field.

6.  Select **Open Record** in the record preview.

7.  Select the **Create New Connection &amp; Credential** related link.

8.  On the form, fill in the fields.

<table id="table_g5k_ngv_mjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td colspan="2">

Please Enter the Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the connection.This field is automatically set to `Tableau Cloud Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

The URL used for connecting to the server on which Tableau Cloud is installed. For example, `https://<server>.online.tableau.com/api/`.

</td></tr><tr><td>

Content URL

</td><td>

The permanent name of the site to sign in to. The content URL appears in the URL path of Tableau content in your browser address bar after the Tableau Server URL. mySite is the content URL in the following example: `http://<server or cloud URL>/#/site/mySite/explore`.

</td></tr><tr class="sub-head"><td colspan="2">

Please Enter the Credential InformationSelect the Personal Access Token \(PAT\) or JSON Web Token \(JWT\) authentication type. The fields change based on the authentication type that you select.

</td></tr><tr class="sub-head"><td colspan="2">

Fields for the PAT authentication type

</td></tr><tr><td>

Token Name

</td><td>

The Token name that you provided while registering the Tableau Cloud application by using the PAT authentication type.For more information, see [Register a Tableau Cloud application](integrate-with-tableau-cloud.md#).

</td></tr><tr><td>

Token Secret

</td><td>

The Token secret that you copied while registering the Tableau Cloud application by using the PAT authentication type.For more information, see [Register a Tableau Cloud application](integrate-with-tableau-cloud.md#).

</td></tr><tr><td>

Expiry Interval \(sec\)

</td><td>

Life span of the generated Personal Access Token \(PAT\).Default value: 14400 sec

**Important:** You mustn't modify the value of this field.

</td></tr><tr class="sub-head"><td colspan="2">

Fields for the JWT authentication type

</td></tr><tr><td>

Secret ID

</td><td>

The Secret ID that you copied while registering the Tableau Cloud application by using the JWT authentication type.For more information, see [Register a Tableau Cloud application](integrate-with-tableau-cloud.md#).

</td></tr><tr><td>

Secret Value

</td><td>

The Secret value that you copied while registering the Tableau Cloud application by using the JWT authentication type.For more information, see [Register a Tableau Cloud application](integrate-with-tableau-cloud.md#).

</td></tr><tr><td>

Username

</td><td>

User name, that is, email address of the authenticated Tableau Cloud user.

</td></tr><tr><td>

Client ID

</td><td>

The Client ID that you copied while registering the Tableau Cloud application by using the JWT authentication type.

</td></tr><tr><td>

Expiry Interval \(sec\)

</td><td>

Life span of the generated JSON Web Token \(JWT\).Default value: 3600 sec

**Important:** You mustn't modify the value of this field.

</td></tr></tbody>
</table>9.  Select **Create**.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

11. Select **Publish**.

12. In the Publish Confirmation dialog box, select **OK**.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

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

