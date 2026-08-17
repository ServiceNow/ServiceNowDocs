---
title: Create an AI connection for Copilot Studio \(v3.1.7\)
description: Create an AI connection for Copilot Studio in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.1.7\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-copilot-studio.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 2
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Copilot Studio \(v3.1.7\)

Create an AI connection for Copilot Studio in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.1.7\).

## Copilot Studio prerequisites

Complete the following steps in your Power Platform environment before creating a Copilot Studio connection.

Register an Application in Microsoft Entra ID

Register an application to obtain OAuth credentials for the connector.

To register the application:

-   Follow the [Microsoft Entra app registration](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app) quick start guide to create an application.
-   Record the Client ID and Client Secret from the registration.

Grant application access to your Copilot Studio environment

Configure the application as a user in your Copilot Studio environment.

To configure application access:

1.  Open the [Power Platform admin Center](https://admin.powerplatform.microsoft.com/home).
2.  Navigate to Environments and select your Copilot Studio environment.
3.  Go to Settings &gt; Users + Permissions &gt; Application users.
4.  Select New App User and add your application using the Client ID from step 1.
5.  Assign the following security roles to the application user:
    -   Basic User
    -   System administrator

If you don't want to create a System administrator role, you can create a Copilot Studio dataverse custom role. For custom role creation, see [Create a Copilot Studio Dataverse custom role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/create-a-copilot-studio-dataverse-custom-role.md).

**Note:** You can obtain the Environment ID from Settings &gt; Session details &gt; Environment ID in your environment.

Multi-environment Support

You can discover agents from multiple Copilot Studio environments using a single connection.

To configure multi-environment discovery:

-   Enter multiple environment IDs as comma-separated values in the Environment ID field \(examples: env-id-1, env-id-2, env-id-3\).
-   The same OAuth credentials \(Client ID and Client Secret\) are used for all environments.
-   Verify that the application user is configured in each environment with the required security roles.
-   Each environment will be tested and discovered separately during the import process.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AI connector for Microsoft** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to review the setup instructions and automation script.

4.  Select **I have read the setup instructions** check box.

5.  Select **Continue**.

    Select authentication type page appears.

6.  Choose the authentication type from the drop-down and select **Submit**.

7.  Select **Client credentials** and skip to step 10.

8.  Select **Certificate-based authentication**.

9.  Create X.509 certificate:

    **Note:** You can create certificate or use an existing one.

    1.  Select **New**.

    2.  Enter the**Name**.

    3.  Enter the **Key store password**.

    4.  Select **+Add file** to add an attachment.

    5.  Select **Save**.

    6.  Select the newly created certificate and select **Continue**.

10. Create and test connection:

    1.  Under **Select source systems** select the **Copilot** check box.

    2.  Enter the **Connection Name**.

    3.  Enter the **Tenant ID**.

    4.  Enter the **OAuth Client ID**.

    5.  Enter the **Keystore**.

    6.  Enter the **Keystore password**.

    7.  Enter the **Thumbprint**.

    8.  Enter the **Environment URLs**.

        **Note:** The Region and Resource name fields are optional. You can enter multiple Environment URLs by separating them with a comma.

11. Configure import schedule:

    1.  Open the Copilot scheduled job.

    2.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive.

        **Note:** verify to execute the Discovery-scheduled job first.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

12. Select **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

