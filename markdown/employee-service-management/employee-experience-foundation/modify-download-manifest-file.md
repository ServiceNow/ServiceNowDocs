---
title: Modify and download the manifest file for GCC-H or DoD
description: Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Employee Center and Virtual Agent with Microsoft Teams for GCC-H or DoD, MS Teams for GCC-H or DoD, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Modify and download the manifest file for GCC-H or DoD

Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.

## Before you begin

Role required:external\_app\_install\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Click **New**.

    The **Generic Info** tab appears.

3.  In the **Generic Info** section, enter the details.

    1.  **Short name**: Option to provide a short name for the manifest file.

    2.  **Full name**: Option to provide the complete name for the manifest file.

    3.  **Version**: Version of the manifest file.

        Ex: 1.0.0

    4.  **Unfurl Links**: Option to unfurl the links in Microsoft Teams.

        Link unfurling generates a content-rich preview\(adaptive card\) when a supported link is shared in a conversation with a user in Microsoft Teams. For more details about link unfurling, refer [Unfurl the web links in Microsoft Teams chat](../concept/enable-link-unfurling.md).

    5.  **Short description**: Short description about the manifest file.

    6.  **Description**: Detailed description about the manifest file.

    7.  **Accent Color**: Option to choose a custom color for the conversations in Microsoft Teams as per the company branding and the accent color should be in HTML color code format.

        **Note:** If you want to customize the company branding, clear the **Use default images** option and then upload the icons. For more information on the size of icons, refer [App icons](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/apps-package#app-icons) and [manifest schema icons](https://docs.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema#icons).

4.  Click **Submit**.

    ![Submit manifest file](../images/submit-manifest.png)

5.  In the **Generic Info** section, click **Next** to navigate to **Configure Virtual Agent** tab.

    ![Next option in Generic Info tab](../images/next-tab.png)

6.  In the **Configure Virtual Agent** section, you can do one of the following.

    To configure the Virtual Agent in your instance, click **Configure Virtual Agent**. For more information, see [Conversational Integration with Microsoft Teams](https://www.servicenow.com/docs/access?context=teams-conv-integration&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

    ![Configure Virtual Agent tab](../images/configure-va-tab.png)

    Select **Connect multiple ServiceNow instances to your Microsoft Teams tenant**and select the Virtual agent installed in Step 5.

7.  In the **Configure Tab** section, enter the following.

    1.  **Enable tabs**: Option to add tabs in Microsoft Teams application and this is selected by default.

    2.  **Tab name**: Option to provide a name for the Service portal tab that appears in Microsoft Teams.

    3.  **Enable Activity Feed**: Option to enable activity feed to receive campaign notifications in Microsoft Teams and this option is selected by default.

    4.  Click **Next**.

        For self-configured app, you must provide the Application \(client\) ID and Directory \(tenant\) ID in the **Configure Tab** section.

        ![pre-published app configure tab](../images/multi-tenant-configure-tab.png)

8.  In the **Ready** section, select **Enable Activity Feed** option to receive notifications for campaigns.

    Verify the details provided and click **Download Manifest** to download the manifest file.

    ![Manifest file](../images/activity-feed-manifest-file.png)

    The manifest file downloads in the zip format.


## What to do next

You must upload the manifest file in Microsoft Teams. For more information, refer [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams.md).

**Parent Topic:**[Integrating Employee Center and Virtual Agent with Microsoft Teams for GCC-H or DoD](../concept/ec-teams-va-integration-gcch.md)

