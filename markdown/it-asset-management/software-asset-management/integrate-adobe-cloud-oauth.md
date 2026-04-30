---
title: Integrate Adobe Cloud using OAuth Server-to-Server credentials
description: Integrate your ServiceNow instance with Adobe Cloud services by using OAuth Server-to-Server credentials.Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using OAuth.Create an Adobe Cloud integration profile on your ServiceNow instance by using OAuth credentials to track your software subscriptions and to determine your license compliance.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Integrating with Adobe Cloud, Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrate Adobe Cloud using OAuth Server-to-Server credentials

Integrate your ServiceNow® instance with Adobe Cloud services by using OAuth Server-to-Server credentials.

## Create a project and add APIs using OAuth

Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using OAuth.

### Before you begin

Role required: Adobe Cloud admin

### Procedure

1.  Create a project in the Adobe Developer Console to access the Adobe APIs by selecting **Create new project**.

    For more information, see [Projects Overview](https://developer.adobe.com/developer-console/docs/guides/projects/).

2.  Add an API to your project by selecting **Add API**.

    For more information, see [Add API to project using OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/).

3.  Select **User Management API** for the Adobe service that you want to integrate with.

    This service enables you to access the Adobe user management API. After you successfully add the API to your project, you’re redirected to the API overview page.

4.  Select **Next**.

5.  On the Configure API form, expand **Credentials**.

6.  Select the **OAuth Server-to-Server** authentication.

7.  Provide a name in the **Credential name** field to find the correct API credential easily on the **Admin Console** &gt; **Users** &gt; **API Credentials**.

    You can also modify the name later in your project on the OAuth Server-to-Server credential overview page.

8.  Select **Save configured API**.

    The following values are displayed on the credential overview page:

    -   CLIENT ID
    -   CLIENT SECRET
    -   SCOPES
    -   CREDENTIAL NAME
    -   TECHNICAL ACCOUNT ID
    -   TECHNICAL ACCOUNT EMAIL
    -   ORGANIZATION ID
    **Note:**

    Copy the CLIENT ID and ORGANIZATION ID and also retrieve the CLIENT SECRET to use them later.

9.  Get the Connection URL \(Instance\) URL from the Adobe Developer Console to create and get an OAuth token for Adobe Cloud.

    1.  In the Generate access token section, select **View cURL command**.

    2.  Copy the Connection URL.

        **Note:**

        Copy only the required URL from the entire command.

        For example, here the Connection URL is the highlighted part.

        ![Connection URL in Adobe Developer Console.](../image/access-token-adobe.jpg)


## Create an Adobe Cloud integration profile using OAuth

Create an Adobe Cloud integration profile on your ServiceNow instance by using OAuth credentials to track your software subscriptions and to determine your license compliance.

### Before you begin

Role required: sam\_admin, sam\_integrator

Activate the following plugins:

-   Software Asset Management Professional for Adobe \(com.sn\_samp\_adobe\)
-   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)

### About this task

If you’re using Software Asset Workspace, the option to create the Adobe Cloud integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d330215e394">

Interface

</th><th align="left" id="d330215e397">

Action

</th></tr></thead><tbody><tr><td id="d330215e403">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Adobe Cloud Integration Profile**.


</td></tr><tr><td id="d330215e446">

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

Name of the Adobe Cloud integration profile.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to access Adobe Cloud APIs.-   OAuth 2.0
-   JWT
**Note:**

-   For the existing Adobe Cloud integration profiles before upgrade to Software Asset Management - SaaS License Management 13.1.0 version or later, this field is automatically set to **JWT**. For more information, see [Integrate Adobe Cloud using Service Account \(JWT\) credentials](integrate-adobe-cloud-jwt.md#).
-   For all the new Adobe Cloud integration profiles, this field is automatically set to **OAuth 2.0**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Adobe subscription.

</td></tr></tbody>
</table>3.  In the Process configuration section, view the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:**

    The **Download subscriptions** check box is selected by default and you can't clear it.

    For more information about the required roles and scopes, see [Minimal user permissions](adobe-cloud-integration.md) table.

4.  Select **Submit**.

    The **Connection &amp; Credential** field appears on the form and is automatically set to **sn\_sam\_saas\_int.Adobe\_OAuth**.

5.  Select the preview icon \(![Preview icon](../image/preview-icon.png)\) beside the **Connection &amp; Credential** field to open the Connection &amp; Credential Aliases record.

6.  Select the **Create New Connection &amp; Credential** related link.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the Adobe Cloud connection.|
    |Connection URL \(Instance URL\)|URL for the connection. This field is automatically set to `https://<Instance Name>.adobelogin.com`. For more information about the steps to get the URL, see Step 9 in [Create a project and add APIs using OAuth](integrate-adobe-cloud-oauth.md#).|
    |OAuth Client ID|Client ID that you generated while [creating an Adobe Cloud OAuth credential](integrate-adobe-cloud-oauth.md#).|
    |OAuth Client Secret|Client Secret that you retrieved while [creating an Adobe Cloud OAuth credential](integrate-adobe-cloud-oauth.md#).|
    |OAuth Redirect URL|`https://<instance_name>/oauth_redirect.do`, where the instance name is the name of your ServiceNow instance.|
    |Organization ID|Adobe Cloud Organization ID that you find while [creating an Adobe Cloud OAuth credential](integrate-adobe-cloud-oauth.md#).|

8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](adobe-cloud-integration.md) table.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.


### Result

Adobe subscription data is pulled into Software Asset Management when the **SAM - Import Adobe User Subscriptions** scheduled job runs. When the subscription data is pulled, the **SAM - Optimize Adobe Subscriptions** scheduled job runs monthly to optimize the Adobe Creative Cloud subscriptions.

This job completion results in the following:

-   An optimization candidate that consolidates three \(configurable\) or more Single App or individual product subscriptions and recommends Adobe Creative Cloud All Apps when it isn't installed.
-   A reclamation candidate that reclaims Single App or individual product subscriptions with dual licenses when Adobe Creative Cloud All Apps is installed.

    Let's say, a user is subscribed to Adobe Creative Cloud All Apps and also consumes licenses for Single App or individual products such as Adobe Acrobat and Adobe Photoshop. In this dual license scenario, the Software Asset Management application recommends reclaiming the licenses for Single App or individual product subscriptions.

-   A reclamation candidate that reclaims three \(configurable\) or more Single App or individual product subscriptions that are actively used and an optimization candidate that recommends assigning Adobe Creative Cloud All Apps.

    Let's say, a user is subscribed to Adobe Acrobat, Adobe Illustrator, and Adobe Photoshop and uses all these products actively. In this scenario, the Software Asset Management application recommends reclaiming the licenses for these individual product subscriptions and recommends using Adobe Creative Cloud All Apps.

-   A reclamation candidate that reclaims Adobe Creative Cloud All Apps when less than three \(configurable\) individual products are actively used and an optimization candidate that recommends assigning Single App or individual product subscriptions that are actively used.

    Let's say, a user is subscribed to Adobe Creative Cloud All Apps but is using less than three individual Creative Cloud products actively. In this scenario, the Software Asset Management application reclaims the Adobe Creative Cloud All Apps license and recommends assigning these individual product subscriptions that are actively used.


### What to do next

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

View the subscription data by navigating to **All** &gt; **SaaS License** &gt; **All User Subscriptions**. You can check the status of the **SAM - Import Adobe User Subscriptions** job by navigating to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Job Results**.

You can also view information about your Adobe subscriptions, compliance, and costs on the [Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic](sam-saas-subscription-dash.md).

After creating an integration profile, you can view information about software models, unrecognized subscription identifiers, scheduled jobs, scheduled job results, and software subscriptions in the Software Asset Workspace. Navigate to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**.

**Related topics**  


[Publisher optimizations for Adobe](../reference/pub-opt-adobe.md)

