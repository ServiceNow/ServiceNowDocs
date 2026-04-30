---
title: Activate Slack as a channel provider
description: Activate Slack by validating the Slack connection.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Slack chat connector for major security incidents, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate Slack as a channel provider

Activate Slack by validating the Slack connection.

## Before you begin

Role required:

-   sn\_msi.workspace\_admin - Write
-   sn\_msi.chat\_collab\_provider - Read

Once the connection is activated and validated, an information message is displayed that the Provider connection is validated successfully. You can modify the channel configuration by adding and removing users, and possibly adding more channels or renaming existing channels.

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **Chat Channel** &gt; **Chat Provider Configuration**.

2.  Select **Slack** to open the Slack chat provider configuration.

    ![Slack Chat Provider Configuration](../image/msim-provider-config-slack.png "Slack Chat Provider Configuration")

3.  Select **Download Slack manifest** to download the `slack_manifest.json` file.

    The `slack_manifest.json` file contains the complete configuration for the Slack setup and enables you to configure Slack automatically. You need to upload this JSON file into the Slack configuration.

4.  Open the `slack_manifest.json` file, and perform the following steps:

    1.  Go to the `api.slack.com/apps` URL on your web browser.

    2.  Select **Create New App** action.

    3.  In the Create an app pop-up, choose the **From an app manifest** option.

    4.  In the Pick a workspace to develop your app pop-up, choose a workspace from the list and select **Next**.

        For example, MSIM Slack Workspace.

    5.  In the Enter app manifest below pop-up, select the **JSON** tab, and copy paste the code from the `slack_manifest.json` file.

    6.  Select **Next**.

    7.  In the Review summary &amp; create your app pop-up, select **Create**.

        Now your app has been created.

    8.  In the Basic Information page, select **Install to Workspace**.

        The Slack integration bot requests your permission to access the MSIM Slack Workspace.

    9.  Select **Allow**.

    10. In the App Credentials section, fill in the details by navigating back to the ServiceNow instance.

    11. Select **All** &gt; **Slack Configurations**.

        You need the sn\_msi.workspace\_admin role for this action.

    12. Select a **Signing Secret** property.

    13. Copy the Signing Secret and paste it in the App Credentials section of Slack.

    14. In the ServiceNow instance, navigate to **All** &gt; **Flow Designer**.

    15. Navigate to **Connections** &gt; **Slack** &gt; **View Details** &gt; **Configure**.

    16. On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name of this connection. For example, Slack.|
        |Connection URL|URL of this connection. For example, https://slack.com|
        |Credential Name|Name of the credentials. For example, Slack credentials.|
        |OAuth Name|Name of the OAuth. For example, Slack OAuth.|
        |OAuth Client ID|The Client ID that was generated for the account that you created in Slack.|
        |OAuth Client Secret|The Client secret for the account that you created in Slack.|
        |OAuth Redirect URL|OAuth redirect instance name. For example, msimslack.service-now.com/oauth\_redirect.do|

    17. Select **Configure and Get OAuth Token**.

        The Slack integration bot requests your permission to access the MSIM Slack Workspace.

    18. Select **Allow**.

        The OAuth Access token is available and will expire on &lt;YYYY-MM-DD&gt; &lt;HH:MM:SS&gt;.

5.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **Chat Channel** &gt; **Chat Provider Configuration**.

6.  Select the **Active** check box to activate the Chat Provider record.

7.  Select **Validate Connection** to test the connection.

    A confirmation message displays that the Provider connection is validated successfully.

8.  Right-click the record and select **Save**.

    After that the connection between Slack and ServiceNow AI Platform instance is successfully established.

9.  Navigate to **api.slack.com/apps** &gt; **Features** &gt; **OAuth &amp; Permissions**.

    1.  Verify if all the scopes are correct.

    2.  Navigate to **Features** &gt; **Event Subscriptions**.

    3.  In the Request URL field, select **Retry**.

        You can see a verified message.

    4.  Select **Save**.


**Parent Topic:**[Configure Slack chat connector for major security incidents](../concept/configure-slack-chat-connector-msi.md)

