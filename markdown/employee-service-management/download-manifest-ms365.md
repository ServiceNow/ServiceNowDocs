---
title: Create and download manifest file for Employee Center and Microsoft 365 integration
description: Create and download the manifest file from your instance to make Employee Center available in Microsoft 365 applications.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Microsoft 365 for Employee Experience, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Create and download manifest file for Employee Center and Microsoft 365 integration

Create and download the manifest file from your instance to make Employee Center available in Microsoft 365 applications.

## Before you begin

Role required: external app install admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Select **New**.

    The **Generic Info** tab appears.

3.  In the Generic Info section, fill in the following fields.

<table id="table_ekx_5my_dyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Option to provide a short name for the manifest file.

</td></tr><tr><td>

Full name

</td><td>

Option to provide the complete name for the manifest file.

</td></tr><tr><td>

Version

</td><td>

Version of the manifest file. For example, 1.0.0

</td></tr><tr><td>

Unfurl Links

</td><td>

Option to unfurl the links in Microsoft Teams.Link unfurling generates a content-rich preview \(adaptive card\) when a supported link is shared in a conversation with a user in Microsoft Teams. For more details about link unfurling, refer [Unfurl the web links in Microsoft Teams chat](../concept/enable-link-unfurling.md).

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

Option to choose a custom color for the conversations in Microsoft Teams as per the company branding.The accent color should be in HTML color code format.

**Note:** If you want to customize the company branding, clear the **Use default images** option and then upload the icons. For more information on the size of icons, refer [App icons](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/apps-package#app-icons) and [manifest schema icons](https://docs.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema#icons).

</td></tr></tbody>
</table>4.  Select **Submit**.

    ![Submit manifest for Microsoft 365 applications](../images/submit-manifest-ms365.png)

5.  In the Generic Info section, select **Next** to navigate to **Configure Virtual Agent** tab.

6.  Configure the Virtual Agent in your instance by selecting **Configure Virtual Agent**.

    For more information, see [Conversational Integration with Microsoft Teams](https://www.servicenow.com/docs/access?context=teams-conv-integration&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    ![Configure Virtual Agent tab](../images/configure-va-tab-ms365.png)

7.  In the Configure Virtual Agent section, to connect to a single or multiple ServiceNow instances.

    -   If you want to connect one ServiceNow instance to a Microsoft Teams tenant, select **Connect a single ServiceNow instance to your Microsoft Teams Tenant**.

        The Virtual Agent Bot ID is auto-populated if you select this option.

    -   If you want to connect multiple ServiceNow instances to one Microsoft Teams tenant, select **Connect multiple ServiceNow instances to your Microsoft Teams tenant**.
    To integrate Virtual Agent with Microsoft Teams by configuring your own bots, see [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](https://www.servicenow.com/docs/access?context=va-integ-teams-self-configured-bot&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

8.  In the Configure Tab section, fill in the following fields and select **Next**.

<table id="table_udz_vc4_f5bbx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable tabs

</td><td>

Option to add tabs in Microsoft Teams application.

 This field is automatically selected.

</td></tr><tr><td>

Tab name

</td><td>

Option to provide a name for the Service portal tab that appears in Microsoft Teams.

</td></tr><tr><td>

Enable Activity Feed

</td><td>

Option to enable activity feed to receive campaign notifications in Microsoft Teams.

 This option is automatically selected.

</td></tr></tbody>
</table>9.  For self-configured apps, provide the Application \(client\) ID and Directory \(tenant\) ID in the **Configure Tab** section.

    ![self-configured app options](../images/single-tenant-configure-tab-ms365.png)

    **Important:** The above step is not applicable for pre-published apps.

10. Receive notifications for campaigns by selecting **Enable Activity Feed** option in the Ready section.

11. Verify the details provided and select **Download Manifest** to download the manifest file.

    ![Manifest file](../images/manifest-ready-ms365.png)

    The manifest file downloads in the zip format.


## Result

An application registry is created.

**Parent Topic:**[Integrating ServiceNow with Microsoft 365 applications for Employee Experience](../concept/setup-sn-ms-teams-ms365.md)

