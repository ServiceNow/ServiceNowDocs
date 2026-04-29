---
title: Create and download the manifest file for pre-published apps
description: Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create and download the manifest file for pre-published apps

Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.

## Before you begin

Role required: external\_app\_install\_admin

## About this task

You can connect multiple ServiceNow instances to one Microsoft Teams tenant. For more information, see [Integrating multiple ServiceNow instances with a single Microsoft Teams tenant](https://www.servicenow.com/docs/access?context=va-integ-single-teams&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

Only one pre-published app setup can be connected to the Microsoft Teams tenant.

**Note:** You can connect multiple self-configured app environments to the Microsoft Teams tenant as you can create separate Azure apps for each self-configured app environment. For information about creating a manifest file for self-configured apps, see [Create and download the manifest file for self-configured apps](download-manifest-file-st.md#).

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Select **New**.

    The **Generic Info** section opens.

3.  On the **Generic Info** section, fill in the fields.

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

    -   Select **Connect a single ServiceNow instance to your Microsoft Teams Tenant** to connect one ServiceNow instance to a Microsoft Teams tenant. The Virtual Agent Bot ID is auto-populated when you select this option.
    -   Select **Connect multiple ServiceNow instances to your Microsoft Teams tenant** to connect multiple ServiceNow instances to one Microsoft Teams tenant. This is applicable for self-configured apps. For more information, see [Create and download the manifest file for self-configured apps](download-manifest-file-st.md#).
    ![Configure Virtual Agent tab](../images/configure-va-tab.png)

7.  Configure the Virtual Agent in your instance.

    For more information, see [Conversational Integration with Microsoft Teams](https://www.servicenow.com/docs/access?context=teams-conv-integration&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

8.  In the **Configure Tab** section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Enable tabs|Option to add tabs in the Microsoft Teams application. This option is selected by default.|
    |Tab name|Name of the service portal tab that appears in the Microsoft Teams application.|
    |Enable Activity Feed|Option to enable the activity feed to receive campaign notifications in Microsoft Teams. This option is selected by default.|

    For a self-configured app, you must provide the Application \(client\) ID and Directory \(tenant\) ID in the **Configure Tab** section.

    ![pre-published app configure tab](../images/multi-tenant-configure-tab.png)

9.  Select **Next**.

    The **Ready** section opens.

10. In the **Ready** section, select the **Enable Activity Feed** option to receive notifications for campaigns.

11. Navigate to the Application registry record and view the OIDC Provider Configuration record.

    -   Select the link in the information message at the top of the page.
    -   Navigate to **System OAuth** &gt; **Application Registry** and select **Azure AD - sso - &lt;Tenant-ID&gt;**.
    The User Claim is part of the **id\_token** that is fetched from Microsoft Entra ID \(Entra ID\). The **User Field** must be configured so that the value fetched from the User \[sys\_user\] table matches the User Claim value.

    **Note:** If none of the configured fields match the User Claim value, you can create a custom field and enter the required value.

12. Verify the details provided and select **Download Manifest**.

    ![Manifest file](../images/activity-feed-manifest-file.png)

    The manifest file is downloaded in the zip format.


## What to do next

You must upload the manifest file in Microsoft Teams. For more information, see [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams.md).

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)

