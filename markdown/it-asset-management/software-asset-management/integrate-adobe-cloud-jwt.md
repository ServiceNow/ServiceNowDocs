---
title: Integrate Adobe Cloud using Service Account \(JWT\) credentials
description: Integrate your ServiceNow instance with Adobe Cloud services by using Service Account \(JWT\) credentials.Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using a Adobe Service Account \(JWT\).Create an Adobe Cloud integration profile on your ServiceNow instance by using Service Account \(JWT\) credentials to track your software subscriptions and to determine your license compliance.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Integrating with Adobe Cloud, Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrate Adobe Cloud using Service Account \(JWT\) credentials

Integrate your ServiceNow® instance with Adobe Cloud services by using Service Account \(JWT\) credentials.

## Create a project and add APIs using Service Account \(JWT\)

Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using a Adobe Service Account \(JWT\).

### Before you begin

Role required: Adobe Cloud admin

### Procedure

1.  Create a project in the Adobe Developer Console to access the Adobe APIs by selecting **Create new project**.

    For more information, see [Projects Overview](https://developer.adobe.com/developer-console/docs/guides/projects/).

2.  Add an API to your project using a Adobe Service Account \(JWT\).

    For more information, see [Add API to project using Service Account \(JWT\)](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-jwt/).

    Keep the following points in mind when adding an API to your project:

    -   For the Adobe service that you want to integrate with, select **User Management API**. This service enables you to access the Adobe user management API.
    -   When you’re creating a Service Account \(JWT\) credential, which enables you to access the API within the selected Adobe service, select the option to generate a key pair. With this option, the Adobe Developer Console generates both a public key pair and a private key pair that can be used to authenticate your Service Account \(JWT\). The private key is automatically downloaded to your device.
    After you successfully add the API to your project, you’re redirected to the API overview page.

3.  Copy the values in the **CLIENT ID**, **TECHNICAL ACCOUNT ID**, and **ORGANIZATION ID** fields in the Service Account \(JWT\) section of the Overview page.

4.  Select **Retrieve client secret** to view and copy the value in the **CLIENT SECRET** field.

    Save this information in a safe location for later use.

5.  Use the following openssl command to convert the key from the KEY format to the PKS format: `openssl pkcs12 -export -out test1-certificate.pfx -inkey private.key -nocerts`

    The key was automatically downloaded to your device in the previous step. The key must be in the PKS format for you to create a corresponding ServiceNow X.509 certificate for the Adobe Cloud integration.

    You must create a password to convert a key. Use this password in the Key store password and Certificate password fields when creating the ServiceNow integration profile and X.509 certificate in the proceeding steps.

    **Note:** This password must be at least six characters in length.


## Create an Adobe Cloud integration profile using JWT

Create an Adobe Cloud integration profile on your ServiceNow instance by using Service Account \(JWT\) credentials to track your software subscriptions and to determine your license compliance.

### Before you begin

Role required: One of the following roles in combination can create Adobe Cloud integration profile using JWT credentials:

-   admin and sam\_admin
-   admin and sam\_integrator

Activate the following plugins:

-   Software Asset Management Professional for Adobe \(com.sn\_samp\_adobe\)
-   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)

### About this task

If you’re using Software Asset Workspace, the option to create the Adobe Cloud integration profile in Core UI is inactive.

**Note:** All new Adobe integrations must be created using the OAuth authentication type. For more information, see [Integrate Adobe Cloud using OAuth Server-to-Server credentials](integrate-adobe-cloud-oauth.md#). Adobe is migrating from Service Account \(JWT\) credential to OAuth Server-to-Server credential. For more information about the migration, see [Adobe Migration Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d52933e381">

Interface

</th><th align="left" id="d52933e384">

Action

</th></tr></thead><tbody><tr><td id="d52933e390">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Adobe Cloud Integration Profile**.


</td></tr><tr><td id="d52933e432">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Adobe Cloud** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_x3l_x4d_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the Adobe integration profile.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to access Adobe Cloud APIs.-   OAuth 2.0
-   JWT
**Note:**

-   For the existing Adobe Cloud integration profiles before upgrade to Software Asset Management - SaaS License Management 13.1.0 version or later, this field is automatically set to **JWT**.
-   For all the new Adobe Cloud integration profiles, this field is automatically set to **OAuth 2.0**. For more information, see [Integrate Adobe Cloud using OAuth Server-to-Server credentials](integrate-adobe-cloud-oauth.md#).


</td></tr><tr><td>

Client Id

</td><td>

Client ID that is assigned to your Adobe Service Account \(JWT\) while [creating a project and adding APIs](integrate-adobe-cloud-jwt.md#).

</td></tr><tr><td>

Organization Id

</td><td>

Adobe Organization ID that is assigned to your Adobe Service Account \(JWT\) while [creating a project and adding APIs](integrate-adobe-cloud-jwt.md#).

</td></tr><tr><td>

Technical account Id

</td><td>

Adobe Technical Account ID that is assigned to your Adobe Service Account \(JWT\) while [creating a project and adding APIs](integrate-adobe-cloud-jwt.md#).

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Adobe subscription**.

</td></tr><tr><td>

Client secret

</td><td>

Client secret that is assigned to your Adobe Service Account \(JWT\) while [creating a project and adding APIs](integrate-adobe-cloud-jwt.md#).

</td></tr><tr><td>

Certificate

</td><td>

ServiceNow X.509 certificate for the Adobe Cloud integration.

</td></tr><tr><td>

Certificate password

</td><td>

Certificate password that you create when converting your key from the KEY format to the PKS format.

</td></tr></tbody>
</table>3.  Add an X.509 certificate to your integration profile.

    This certificate is based on the key from your Adobe Service Account \(JWT\) credential.

    1.  Navigate to the X.509 Certificate form.
        -   For Core UI:
            1.  On the Integration Profile form, select the search icon \(![Search icon.](../image/search-icon.png)\) next to the **Certificate** field.
            2.  In the X.509 Certificates dialog box, select **New**.
        -   For Software Asset Workspace:
            1.  Navigate to **System Definitions** &gt; **Certificates**.
            2.  Select **New**.
    2.  On the form, fill in the fields.

<table id="table_ixn_nlk_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Certificate name.

</td></tr><tr><td>

Expiration notification

</td><td>

Option to send a notification when the certificate is about to expire.

</td></tr><tr><td>

Notify on expiration

</td><td>

Users that you want to notify when the certificate expires.This field is available only when **Expiration notification** is selected.

</td></tr><tr><td>

Warn in days to expire

</td><td>

Number of days prior to certificate expiration that you want to send a notification.This field is available only when **Expiration notification** is selected.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the certificate is active.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the certificate.

</td></tr><tr><td>

PEM Certificate

</td><td>

Base-64 encoded PEM-formatted text containing the DER certificate. The instance decodes the certificate to populate the **Valid from**, **Expires**, **Expires in days**, **Issuer**, and **Subject** fields.

</td></tr><tr><td>

Format

</td><td>

Format of the certificate.

</td></tr><tr><td>

Type

</td><td>

Certificate type. Set this field to **PKCS12 Key Store**.

</td></tr><tr><td>

Expires in days

</td><td>

Number of days remaining until the certificate expires. This field populates automatically.

</td></tr><tr><td>

Key store password

</td><td>

Certificate password that you created when converting your key from the KEY format to the PKS format in Step 3.

</td></tr></tbody>
</table>    3.  Upload your key \(PKS file\) by selecting the manage attachments icon \(![Manage attachments icon.](../image/manage-attachments-icon.png)\) on the X.509 Certificate form header.
    4.  In the Attachments dialog box, select **Choose file** to locate and select your key.

        The dialog box closes, and you return to the X.509 Certificate form.

    5.  Validate the certificate by selecting the **Validate Stores/Certificates** related link.
    6.  After the certificate is validated, select **Submit**.
4.  In the Process configuration section, view the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:**

    The **Download subscriptions** check box is selected by default and you can't clear it.

    For more information about the required roles and scopes, see [Minimal user permissions](adobe-cloud-integration.md) table.

5.  Select **Submit**.

6.  After the form reloads, select the **Validate Adobe Credential** related link to complete the connection.

7.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.


### Result

Adobe subscription data is pulled into the Software Asset Management application when the **SAM - Import Adobe User Subscriptions** scheduled job runs. When the subscription data is pulled, the **SAM - Optimize Adobe Subscriptions** scheduled job runs monthly to optimize the Adobe Creative Cloud subscriptions.

The completion of these two jobs results in the following scenarios:

-   An optimization candidate that consolidates three \(configurable\) or more Single App or individual product subscriptions and recommends Adobe Creative Cloud All Apps when it isn't installed.
-   A reclamation candidate that reclaims Single App or individual product subscriptions with dual licenses when Adobe Creative Cloud All Apps is installed.

    Let's say, a user is subscribed to Adobe Creative Cloud All Apps and also consumes licenses for Single App or individual products such as Adobe Acrobat and Adobe Photoshop. In this dual license scenario, the Software Asset Management application recommends reclaiming the licenses for Single App or individual product subscriptions.

-   A reclamation candidate that reclaims three \(configurable\) or more Single App or individual product subscriptions that are actively used and an optimization candidate that recommends assigning Adobe Creative Cloud All Apps.

    Let's say, a user is subscribed to Adobe Acrobat, Adobe Illustrator, and Adobe Photoshop and uses all these products actively. In this scenario, Software Asset Management recommends reclaiming the licenses for these individual product subscriptions and recommends using Adobe Creative Cloud All Apps.

-   A reclamation candidate that reclaims Adobe Creative Cloud All Apps when less than three \(configurable\) individual products are actively used and an optimization candidate that recommends assigning Single App or individual product subscriptions that are actively used.

    Let's say, a user is subscribed to Adobe Creative Cloud All Apps but is using less than three individual Creative Cloud products actively. In this scenario, Software Asset Management reclaims the Adobe Creative Cloud All Apps license and recommends assigning these individual product subscriptions that are actively used.


### What to do next

View the subscription data by navigating to **All** &gt; **SaaS License** &gt; **All User Subscriptions**. You can check the status of the **SAM - Import Adobe User Subscriptions** job by navigating to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Job Results**.

You can also view information about your Adobe subscriptions, compliance, and costs on the [Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic](sam-saas-subscription-dash.md).

After creating an integration profile, you can view information about software models, unrecognized subscription identifiers, scheduled jobs, scheduled job results, and software subscriptions in the Software Asset Workspace. Navigate to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**.

**Related topics**  


[Publisher optimizations for Adobe](../reference/pub-opt-adobe.md)

