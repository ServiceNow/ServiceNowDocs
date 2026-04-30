---
title: Integrate with Docusign at Organization level
description: Integrating your Software Asset Management application with the Docusign service at the organization level enables you to track your software subscriptions and envelope consumption data.Register a Docusign application through the Docusign admin portal.Generate RSA keys to integrate the Docusign application with your ServiceNow instance.Generate a Java Key Store \(JKS\) certificate for the JSON Web Token \(JWT\) authentication of your Docusign integration profile.Create an integration profile to track software subscriptions and optimize licensing for the Docusign service.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-11-07"
reading_time_minutes: 10
breadcrumb: [Integrating with Docusign, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with Docusign at Organization level

Integrating your Software Asset Management application with the Docusign service at the organization level enables you to track your software subscriptions and envelope consumption data.

**Note:** Integration with Docusign at the organization level is done using the Data feed API, so the user's last activities aren’t tracked as part of this integration.

For more information about the Docusign service, see [the DocuSign Developer site](https://developers.docusign.com/ios_sdk/developer.html).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Docusign application|Authentication scopes|
|-------|----------------------------------------------|---------------------|
|Download subscriptions|admin|No scopes|
|Download consumption|admin|No scopes|

This process is applicable for Zurich patch 4, Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 16.0.8, and Software Asset Management \(sn\_itam\_samp\) 2.1.0 version onwards.

## Register a Docusign application

Register a Docusign application through the Docusign admin portal.

### Before you begin

Docusign Role required: admin

### Procedure

1.  Log in to your Docusign demo \(non-production\) account.

    You can use any subaccount for logging in that is later promoted to the corresponding production account.

2.  Go to the Admin tab.

    -   If you already have an API integration key from a previous integration ready for use in production, skip to [step 14](integrate-with-docusign-org.md#docusign-prod-login).
    -   If you don't have your API integration key saved, you must generate a new one.
3.  On the side navigation pane, select **Account Profile** and copy the **Organization ID** to secure it for later use.

4.  Navigate to **INTEGRATIONS** &gt; **Apps and Keys**.

5.  In the **Apps and Integration Keys** section, select **Add App and Integration Key**.

6.  On the Add Integration Key form, enter a unique name for your application in the **App Name** field and select **CREATE APP**.

7.  On the profile page of your application, select **Third-party integration key** in the **Integration Type** field.

8.  Copy the value of the **Integration Key** and secure it for later use.

    **Important:** You must request the Docusign support team for enabling the Data feed API on the integration key that you’re generating. If you’re using an Enterprise Pro plan, the Data feed API is free for you with organization management. If you’re using a low-tier plan, you can opt for organization management as an add-on. For further information, contact the Docusign support team.

9.  Select **Save**.

10. In the **Apps and Integration Keys** section, locate the application that you just created in the App Name list.

11. Select **Actions** &gt; **Select Go-Live account**.

    A window pops up prompting you to enter the credentials for your Docusign production account.

12. Enter the Docusign production account credentials to which you want to promote your integration key.

    The **Go Live Status** field changes to **Pending approval**. For a successful Go-Live review, your app must meet the requirements for Go-Live for each API that it uses. For more information on the Go-Live review stages, see [Docusign documentation](https://developers.docusign.com/platform/go-live/).

13. After the integration is approved, the **Go Live Status** changes to **View in production**.

14. Log in to your Docusign production account and verify that the same integration key is present in the production account.


## Generate RSA keypair for Docusign integration

Generate RSA keys to integrate the Docusign application with your ServiceNow instance.

### Before you begin

Docusign requirements:

-   Docusign account
-   Docusign app configured to integrate with ServiceNow
-   Role required: Docusign administrator

### About this task

The integration of Docusign at the organization level enables access to all subaccounts using a single integration key generated in any one subaccount.

### Procedure

1.  Log in to your Docusign production content account.

2.  Go to the Admin tab.

3.  Navigate to **INTEGRATIONS** &gt; **Apps and Keys**.

4.  Next to your application, select **Actions** &gt; **Edit**.

5.  Select **Generate RSA** and save the Key Pair ID, Public Key, and Private Key for later use.


## Generate a Java Key Store certificate

Generate a Java Key Store \(JKS\) certificate for the JSON Web Token \(JWT\) authentication of your Docusign integration profile.

### Before you begin

Role required: admin

### Procedure

1.  Open a text editor for code, such as Sublime Text, and create a file.

2.  Paste the Private key that you had generated from your Docusign integrator app.

    For more information, see [Generate RSA keypair for Docusign integration](integrate-with-docusign-org.md#).

    **Note:** Make sure to include both the beginning and ending of the private key.

3.  Save the file with the .key extension.

    For example, `privatekey.key`.

4.  Open the command line interface \(CLI\) and navigate to the directory where you saved the file with the .key extension.

5.  Create a CA signed certificate using your private key by executing the command:

    ```
    openssl req -new -x509 -key <file-name>.key -out <certificate-name>.pem -days 1095
    ```

    You're prompted to provide details such as country name and province name.

6.  Enter the required details.

7.  Create a PKCS 12 file using your private key and CA signed certificate by executing the command:

    ```
    openssl pkcs12 -export -in <certificate-name>.pem -inkey <file-name>.key -certfile <certificate-name>.pem -out <PKCS-12-file-name>.p12
    ```

    You're prompted to provide a password for the file.

8.  Enter the export password or the source keystore password.

9.  Create the JKS file by executing this command:

    ```
    keytool -importkeystore -srckeystore <PKCS-12-file-name>.p12 -srcstoretype pkcs12 -destkeystore <JKS-certificate-filename>.jks -deststoretype JKS
    ```

    You're prompted to provide a password for the JKS file.

10. Provide the same password for the destination and source keystore passwords.


## Create a Docusign integration profile at Organization level

Create an integration profile to track software subscriptions and optimize licensing for the Docusign service.

### Before you begin

To create a Docusign integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

An organization level integration profile uses the Docusign Data feed API that retrieves detailed subscription and consumption data across an entire organization. It aggregates data from all subaccounts under an organization, offering a centralized view of envelope activity and usage.

If you’re using Software Asset Workspace, the option to create the Docusign integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d94344e807">

Interface

</th><th align="left" id="d94344e810">

Action

</th></tr></thead><tbody><tr><td id="d94344e816">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **DocuSign Integration Profile**.


</td></tr><tr><td id="d94344e858">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **DocuSign** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td>

Display name

</td><td>

Name of the integration profile. For example, `DocuSign Integration`

</td></tr><tr><td>

Integration type

</td><td>

The default value is set to **Organization Level**.

</td></tr><tr id="row_qnx_rt5_bgb"><td>

Contract start date

</td><td>

The date on which the contract agreement became effective.This date is not same as the date when your Docusign account was created.

</td></tr><tr id="row_nn5_st5_bgb"><td>

Profile type

</td><td>

Type of integration profile. This value is automatically set to **DocuSign Subscription**.

</td></tr><tr><td>

Organization Id

</td><td>

The organization ID to which this account belongs.You can find this value in your Docusign account on the Admin tab. Navigate to **Account Profile** and copy the **Organization ID**.

![Docusign account profile highlighting the Organization ID](../image/docusign-org-id.png)

</td></tr><tr><td>

Renewal period \(months\)

</td><td>

The frequency at which envelope consumption gets renewed.For example, if you enter a renewal period of three months, then the consumption data is renewed every three months. The renewal period governs the consumption cycle and is separate from the overall contract term.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Process configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see the [Minimal user permissions](integrate-with-docusign-org.md#) table.

    The **Download subscriptions** check box is selected by default and you can't clear it.

    The **Download Consumption** check box is selected by default.

4.  Select **Submit**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_sam\_saas\_int.Docusign\_OAuth\_with\_JWT**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the connection.|
    |Connection URL|This field is automatically set to **https://api.docusign.net**.|
    |Credential Information|
    |Integration Key|The API integration key that you had generated in the [Register a Docusign application](integrate-with-docusign-org.md#) procedure.|
    |Key Pair ID|The key pair ID of the private key that you had generated in the [Generate RSA keypair for Docusign integration](integrate-with-docusign-org.md#) procedure.|
    |Audience URI|Enter `account.docusign.com` as the URI.|
    |Keystore Password|Password associated with the uploaded JKS file that you had created in the [Generate a Java Key Store certificate](integrate-with-docusign-org.md#) procedure.|

8.  Locate the JKS file on your device by selecting **Keystore**.

    For more information on creating the JKS file, see [Generate a Java Key Store certificate](integrate-with-docusign-org.md#).

9.  Select **Create and Get OAuth Token**.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Scheduled Jobs
-   Scheduled Job Results
-   Unrecognized Subscription Identifiers
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

