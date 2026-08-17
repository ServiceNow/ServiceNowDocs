---
title: Create an AI connection for Copilot Studio \(v3.0.0\)
description: Create an AI connection for Copilot Studio in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.0.0\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connection-for-copilot-v3-0-0.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Copilot Studio \(v3.0.0\)

Create an AI connection for Copilot Studio in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.0.0\).

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

If you don't want to create a System administrator role, you can create a Copilot Studio dataverse custom role. For custom role creation, see [Create a Copilot Studio Dataverse custom role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-a-copilot-studio-dataverse-custom-role.md).

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

3.  Select the Microsoft Copilot check box.

4.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

5.  Select **Continue**.

6.  Setup page appears.

7.  Enter the details on Configure and Test Copilot connection:

    1.  Enter the **Connection name**.

    2.  Enter the **Environment URLs** \(example: https://org55f16a5d.crm.dynamics.com\).

        **Note:** You can obtain the Environment URL from Settings &gt; Session details &gt; Instance URL in your environment.

    3.  Enter the **OAuth client ID**.

    4.  Enter the **OAuth Client Secret**.

    5.  Enter the **Tenant ID**.

    6.  Select **Create and test connection**.

    7.  Select **Continue**.

8.  Configure Copilot import schedule:

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped base system inactive.

        **Note:** Ensure to execute the Discovery-scheduled job first.

    2.  Set the run frequency.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    3.  To run frequency by demand, select Execute now to run.

    4.  Select **Continue**.

9.  Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

