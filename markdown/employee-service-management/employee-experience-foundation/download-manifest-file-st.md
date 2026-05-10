---
title: Create and download the manifest file for self-configured apps
description: Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create and download the manifest file for self-configured apps

Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.

## Before you begin

Role required: external\_app\_install\_admin

## About this task

You can connect multiple ServiceNow instances to one Microsoft Teams tenant. For more information, see [Integrating multiple ServiceNow instances with a single Microsoft Teams tenant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-integ-single-teams.md).

Multiple self-configured app environments can be connected to the Microsoft Teams tenant as you can create separate Azure apps for each self-configured app environment.

This process is for configuring a Microsoft Teams manifest file, which dictates how an application would behave in Microsoft Teams. For information about the manifest generation provided by ITSM/HR, see [Auto-generate the manifest file for uploading on Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/generate-manifest-file-msteams.md), which includes more available configurations.

**Note:** You can only connect one pre-published app setup to the Microsoft Teams tenant. For information about creating a manifest file for pre-published apps, see [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md).

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Select **New**.

    The **Generic Info** section opens.

3.  In the **Generic Info** section, fill in the fields.

<table id="table_hd5_kbn_m1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Short name for the manifest file.

</td></tr><tr><td>

Full name

</td><td>

Complete name for the manifest file.

</td></tr><tr><td>

Version

</td><td>

Version of the manifest file. For example, `1.0.0`.

</td></tr><tr><td>

Unfurl Links

</td><td>

Option to unfurl the links in Microsoft Teams.Link unfurling generates a content-rich preview\(adaptive card\) when a supported link is shared in a conversation with a user in Microsoft Teams. For more details about link unfurling, refer [Unfurl the web links in Microsoft Teams chat](../concept/enable-link-unfurling.md).

</td></tr><tr><td>

Short description

</td><td>

Short description about the manifest file.

</td></tr><tr><td>

Description

</td><td>

Detailed description about the manifest file.

</td></tr><tr><td>

Accent Color

</td><td>

Custom color for the conversations in Microsoft Teams according to the company branding. The accent color must be in the HTML color code format.

</td></tr><tr><td>

Use default images

</td><td>

Option to use the default images for branding.**Note:** If you want to customize the company branding, clear the **Use default images** option and then upload the icons. For more information on the size of icons, see [App icons](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/apps-package#app-icons) and [manifest schema icons](https://docs.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema#icons).

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select **Next**.

    ![Next option in Generic Info tab](../images/next-tab.png)

    The **Configure Virtual Agent** section opens

6.  In the **Configure Virtual Agent** section, select either of the following options.

    -   Select **Connect a single ServiceNow instance to your Microsoft Teams Tenant** to connect one ServiceNow instance to a Microsoft Teams tenant. The Virtual Agent Bot ID is auto-populated when you select this option. This is applicable for pre-published apps. For more information, see [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md).
    -   Select **Connect multiple ServiceNow instances to your Microsoft Teams tenant** to connect multiple ServiceNow instances to one Microsoft Teams tenant.
    ![Configure Virtual Agent tab](../images/configure-va-tab.png)

    To configure the Virtual Agent in your instance, select **Configure Virtual Agent**. For more information, see [Conversational Integration with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/teams-conv-integration.md).

    To integrate Virtual Agent with Microsoft Teams by configuring your own bots, see [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-integ-teams-self-configured-bot.md).

7.  In the **Configure Tab** section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Enable tabs|Option to add tabs in the Microsoft Teams application. This option is selected by default.|
    |Tab name|Name of the service portal tab that appears in the Microsoft Teams application.|
    |Enable Activity Feed|Option to enable the activity feed to receive campaign notifications in Microsoft Teams. This option is selected by default.|
    |Application \(client\) ID|The client ID of the Azure app.|
    |Directory \(tenant\) ID|The tenant ID of the Azure app.|

    For a self-configured app, you must provide the Application \(client\) ID and Directory \(tenant\) ID in the **Configure Tab** section. The Tenant ID and Client ID \(App ID\) can be fetched from the Azure portal.

    ![self-configured app options](../images/single-tenant-configure-tab2.png)

8.  Select **Next**.

    The **Ready** section opens.

9.  In the **Ready** section, select the **Enable Activity Feed** option to receive notifications for campaigns.

10. Navigate to the Application registry record and view the OIDC Provider Configuration record.

    -   Select the link in the information message at the top of the page.
    -   Navigate to **System OAuth** &gt; **Application Registry** and select **Azure AD - &lt;Tenant-ID&gt;**.
    The User Claim is part of the **id\_token** that is fetched from Microsoft Entra ID \(Entra ID\). The **User Field** must be configured so that the value fetched from the User \[sys\_user\] table matches the User Claim value.

    **Note:** If none of the configured fields match the User Claim value, you can create a custom field and enter the required value.

11. Verify the details provided and select **Download Manifest**.

    ![Manifest file](../images/manifest-ready-state-st.png)

    The manifest file is downloaded in the zip format and an application registry is created.


## What to do next

You must upload the manifest file in Microsoft Teams. For more information, refer [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams.md).

**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_s_tnt.md)

