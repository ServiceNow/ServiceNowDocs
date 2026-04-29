---
title: Create a Service user to make calls from Microsoft Teams
description: Configure Notify connector for Microsoft Teams in your environment by creating a Service user to have a seamless conference call experience in Microsoft Teams.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create a Service user to make calls from Microsoft Teams

Configure Notify connector for Microsoft Teams in your environment by creating a Service user to have a seamless conference call experience in Microsoft Teams.

## Before you begin

Role required: Microsoft Azure admin

**Note:** You must create a service user role, which will be able to start online meetings on behalf of users.

## Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/).

2.  Create a Service user.

    1.  Navigate to **Azure services** &gt; **User**.

    2.  Select **New user**.

    3.  On the form, fill the fields.

        |Field|Description|
        |:----|:----------|
        |User name|Option to provide the user name for the user.|
        |Name|Option to provide the name of the user.|

    4.  Select **Create**.

    5.  Select the created user to view the details.

        **Note:** Ensure that the Service User has the required license/subscription and a valid usage location set to make conference calls from Microsoft Teams.

3.  Run the PowerShell command from Terminal on macOS or from the Command prompt on Windows OS.

    1.  Type the command `pwsh` and press **Enter**.

    2.  Connect your Microsoft tenant with PowerShell.

    3.  Run the following command in PowerShell.

        ```
        connect-microsoftteams
        ```

        ![PowerShell connect Teams command](../../meeting-extensibility/image/powershell-connect-teams-command.png)

        Upon successful connection, a confirmation message is displayed in the browser.

        ![Authentication message in browser](../../meeting-extensibility/image/authentication-message-browser.png)

        PowerShell will also display the tenant details.

        ![Powershell confirmation](../../meeting-extensibility/image/powershell-confirmation.png)

4.  Run the Application Access Policy in PowerShell.

    For more information on the application access policy, see [Configure application access to online meetings](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

    Run the following command in PowerShell.

    Use the App ID `ced2c8b2-7075-49fb-8dc9-7ebb41f89769` to grant permission to the Notify connector app. You can find the App ID in Microsoft Azure portal in the path: **Home** &gt; **Enterprise applications** &gt; **All applications**. Select the app created for Notify connector for Microsoft Teams.

    ![Notify connector app](../image/app-id.12png.png)

    ```
    Syntax:
    
    New-CsApplicationAccessPolicy -Identity "<PolicyName (can be anything)>" -AppIds "<AppIds>" -Description "<Policy Description>"
    
    Example:
    If you have a Pre-published (multi tenant) setup, use the application ID from Azure portal.
    
    For Example: New-CsApplicationAccessPolicy -Identity "OnlineMeetingsAccessPolicy" -AppIds "ced2c8b2-7075-49fb-8dc9-7ebb41f89769" -Description "Grant OnlineMeeting Application Permission"
    ```

    ![App access policy in Powershell](../../meeting-extensibility/image/app-access-policy.png)

    Upon successfully granting the permissions, the details are displayed in PowerShell.

    ![App access policy success message in Powershell](../../meeting-extensibility/image/powershell-app-access-success.png)

5.  Run the user permission policy in PowerShell.

    1.  Go to the [Microsoft Azure portal](https://portal.azure.com/).

    2.  Navigate to **Home** &gt; **Users**.

    3.  Select the user created.

    4.  Copy the **Object ID** of the user to notepad.

    5.  Run the user policy command in PowerShell with PolicyName same as created in the previous step.

        ```
        Syntax:
        
        Grant-CsApplicationAccessPolicy -Identity "<UserAzureID>" -PolicyName "<PolicyName>"
        
        ```

        You must provide your user ID in **UserAzureID** field and run the command in PowerShell.

        ```
        Example:
        
        Grant-CsApplicationAccessPolicy -Identity "fdcd9c17-ceae-468f-906f-2er76b4dd0f4" -PolicyName " OnlineMeetingsAccessPolicy"
        
        ```

        ![User permissions](../../meeting-extensibility/image/powershell-user-permissions.png)

6.  As a user with sn\_notify\_msteams.admin role, configure Microsoft Teams.

    1.  Open your ServiceNow instance.

    2.  Navigate to **Notify** &gt; **Microsoft Teams** &gt; **Configuration**.

        ![Notify Microsoft Teams configuration](../../meeting-extensibility/image/notify-teams-configuration.png)

    3.  Paste the **Object ID** of the user in **Service user Azure ID** field.

        If you have performed an upgrade to Notify connector for Microsoft Teams, you must manually enable the **Enable create online meeting option**. You can then update the value in the Service user Azure ID field.

    4.  Select **Update**.


**Parent Topic:**[Integrate Notify connector pre-published app with Microsoft Teams](../concept/setup-notify-ms-teams-multi-tenant.md)

