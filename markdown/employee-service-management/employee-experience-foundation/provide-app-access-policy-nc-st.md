---
title: Create a Service user to make calls from Microsoft Teams
description: Create a service user role to be able to start online meetings on behalf of users in Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Create a Service user to make calls from Microsoft Teams

Create a service user role to be able to start online meetings on behalf of users in Microsoft Teams.

## Before you begin

Role required: Microsoft Teams admin

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

4.  Run the command below to create a new Application Access Policy in PowerShell.

    Use the bot ID created in step 3 in the section [Create an app in Microsoft Teams to enable making calls](https://servicenow.com/docs/bundle/utah-employee-service-management/page/product/notify2/task/create-app-ms-teams.html) as the AppId for the command.

    For more information on the application access policy, see [Configure application access to online meetings](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

    ```
    Syntax:
    
    New-CsApplicationAccessPolicy -Identity "<PolicyName (can be anything)>" -AppIds "<AppIds>" -Description "<Policy Description>"
    
    Example:
    If you have a Self-configured (single tenant) setup, use the application ID from Azure portal.
    
    For Example: New-CsApplicationAccessPolicy -Identity "OnlineMeetingsAccessPolicy" -AppIds "aaaaaaaa-1234-er4r-8dc9-123456789012" -Description "Grant OnlineMeeting Application Permission"
    ```

    ![App access policy in Powershell](../../meeting-extensibility/image/app-access-policy.png)

    Upon successfully creating the policy, the details are displayed in PowerShell.

    ![App access policy success message in Powershell](../../meeting-extensibility/image/powershell-app-access-success.png)

5.  Run the user permission policy in PowerShell.

    1.  Go to the [Microsoft Azure portal](https://portal.azure.com/).

    2.  Navigate to **Home** &gt; **Users**.

    3.  Select the user created.

    4.  Copy the **Object ID** of the user to notepad.

    5.  Use the policy name created in the previous step as the **PolicyName** of the command and the **Object ID** as the **UserAzureID** respectively in the command to execute in PowerShell.

        ```
        Syntax:
        
        Grant-CsApplicationAccessPolicy -Identity "<UserAzureID>" -PolicyName "<PolicyName>"
        
        Example:
        
        Grant-CsApplicationAccessPolicy -Identity "fdcd9c17-ceae-468f-906f-2er76b4dd0f4" -PolicyName "OnlineMeetingsAccessPolicy"
        
        ```

        ![User permissions](../../meeting-extensibility/image/powershell-user-permissions.png)


**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

