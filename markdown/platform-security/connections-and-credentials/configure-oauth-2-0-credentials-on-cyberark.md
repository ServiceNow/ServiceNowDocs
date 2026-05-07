---
title: Configure OAuth 2.0 credentials on CyberArk
description: Configure your CyberArk vault with OAuth 2.0 credentials that the ServiceNow instance requests.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Configure CyberArk, OAuth 2.0 authentication via MID Server using external credential storage, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure OAuth 2.0 credentials on CyberArk

Configure your CyberArk vault with OAuth 2.0 credentials that the ServiceNow instance requests.

## Before you begin

Role required: Admin

## About this task

To store OAuth 2.0 credentials, first create an OAuth 2.0 credential template in the CyberArk vault. This process must only be completed once for the vault.

## Procedure

1.  Do the following steps, if you're configuring the OAuth 2.0 credentials for the first time.

    1.  Log in to CyberArk in Administration mode.

    2.  Navigate to the **Administration** tab.

    3.  Select **Platform Management**.

        The Platform Management page displays the platforms under the Targets tab.

    4.  Expand a platform type.

    5.  Select the settings icon \(![Platform settings icon.](../image/platform-icon.png)\) that corresponds to a platform template and select **Duplicate**.

    6.  In the Duplicate Platform window, enter a name for the template and select **Create**.

        **Note:** Note the system type under which you had created a duplicate template. For example, Cloud Service is a system type.

    7.  Select the settings icon \(![Platform settings icon.](../image/platform-icon.png)\) that corresponds to the duplicate platform template that you created and select **Edit**.

    8.  Add the property.

        Name as Username and Display Name as Client ID.

    9.  Rename the other properties.

        **Tip:** Choose property names relevant to OAuth 2.0.

    10. Select **Apply**.

        The updates are applied.

    11. Select **OK**.

    12. On the left panel, navigate to Accounts.

    13. Select **Add Account**.

    14. Under the System Type heading, select the system type under which you had created the platform template.

        The System Type shows the platform templates.

    15. Under the Select Platform heading, select the platform template that you had created.

    16. Select Safe.

        Save the Safe value for later use.

    17. Fill in the information in for the Client ID, Password \(provide Client Secret as value\), and other fields as required.

    18. Select **Add**.

        The account is added.

    19. On the Account View page, open an account.

    20. Select the **Details** tab.

    21. Copy the value stored under the Account name section and save it for later use.

        The value that you copied and stored is used as the credential identifier in the ServiceNow instance.

2.  Do the following steps, if you're not configuring the OAuth 2.0 credentials for the first time.

    1.  Log in to CyberArk in Administration mode.

    2.  Navigate to the **Account** section and select **Add account**.

    3.  Select the system type from **System Type** under which the template for storing OAuth 2.0 exists.

    4.  Select the required platform template that you had created and select **Safe**.

        Save the Safe value for later use.

    5.  Fill in the information in for the Client ID, Password \(provide Client Secret as value\), and other fields as required.

    6.  Select **Add**.

        The account is added.

    7.  On the Account View page, open an account.

    8.  Select the **Details** tab.

    9.  Copy the value stored under the Account name section and save it for later use.

        The value that you copied and stored is used as the credential identifier in the ServiceNow instance.


**Parent Topic:**[Configure CyberArk](configure-cyberark.md)

