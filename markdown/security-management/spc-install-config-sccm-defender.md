---
title: Install and configure the Service Graph Connector for Microsoft SCCM and the Microsoft Defender Mitigation Control Integration
description: The Service Graph Connector for SCCM and the Microsoft Defender Mitigation Control Integration require separate configuration steps.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Policies for Exploit Protection \(EDR\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Install and configure the Service Graph Connector for Microsoft SCCM and the Microsoft Defender Mitigation Control Integration

The Service Graph Connector for SCCM and the Microsoft Defender Mitigation Control Integration require separate configuration steps.

## Before you begin

You must install, activate, and configure the Service Graph Connector for SCCM to import asset details. You configure the Microsoft Defender Mitigation Control Integration, that also uses SCCM, to gather additional data about mitigation controls configured on the assets to that are monitored by the Service Graph Connector for SCCM.

Roles required:

-   admin for installation and activation of plugins
-   SPC Admin Group and SPC Analyst Group for configuration of integrations in the workspace
-   Microsoft SCCM credentials that include the Script Authors role. The Script Authors role provides required permissions to create a script that is required to import mitigation information on the SCCM server.

    **Note:** This role must be created and assigned with the following permissions:

    |Category|Permission|State|
    |--------|----------|-----|
    |Collection|Run Script|No|
    |Site|Read|Yes|
    |SMS Scripts|Create|Yes|
    |SMS Scripts|Read|Yes|
    |SMS Scripts|Delete|Yes|
    |SMS Scripts|Modify|Yes|

-   Microsoft SCCM credentials that include the Script Approvers role. The script created to import mitigation information requires approval in your Microsoft SCCM console by user with the Script Approvers role.

    **Note:** This role must be created and assigned with the following permissions:

    |Category|Permission|State|
    |--------|----------|-----|
    |Collection|Run Script|No|
    |Site|Read|Yes|
    |SMS Scripts|Read|Yes|
    |SMS Scripts|Approve|Yes|
    |SMS Scripts|Modify|Yes|


## Procedure

1.  To install and configure the Service Graph Connector for Microsoft SCCM integration, follow these steps:

    **Note:** If you have installed the Service Graph Connector for Microsoft SCCM integration, proceed to step 2 to configure the Microsoft Defender Mitigation Control Integration.

    1.  Navigate to **Connectors and use cases setup** &gt; **Service graph connectors tab**.

    2.  Locate the Service Graph Connector for Microsoft SCCM integration.

    3.  Select the link that takes you to the app listing for the application in the ServiceNow® Store.

    4.  Follow the prompts to install the application.

    5.  Download the installation guide from the Supporting Links and Docs section on the app listing before you exit to help you with configuration and activation.

    6.  Navigate to **Setup** in your instance.

    7.  Follow the prompts in the guided setup and refer to the documentation to configure and activate the SGC.

2.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations** to configure the Microsoft Defender Mitigation Control Integration.

    This tab lists the mitigation controls sources \(CrowdStrike, F5 Big Ip, and Defender\), and the tab is displayed in the workspace only if you have installed the Mitigation Controls Monitoring application.

    On the source cards, you can view the status of the mitigation source \(`Active` or `Inactive`\).

    Note the Active column in Sources displays, `Active`. This indicates the source \(Service Graph Connector for Microsoft SCCM\) is active to retrieve asset data, but you must configure the Microsoft Defender Mitigation Control Integration that fetches additional data about defender configurations on these assets using SCCM before you can monitor mitigation controls.

3.  Select **Next**.

    The SCCM Configuration page is displayed with one Microsoft SCCM Mitigation Control instance link.

4.  Select the instance link that is provided in the Name column.

5.  Fill out the fields for the SCCM credentials configuration Microsoft SCCM Mitigation Control Integration modal.

    |Field|Description|
    |-----|-----------|
    |Name|Field is populated automatically with the instance name.|
    |Connection|Field populated automatically with connection information.|
    |Host|Host name for the SCCM server inside the connection information provided in the previous field.|
    |User name|User name to access the SCCM server.|
    |Password|Password to access the SCCM server.|
    |MID Server|Select a ServiceNow-managed MID Server from the list.|
    |Validation status|Field populated after validation attempt. If the connection successful, the integration instance state is **Valid**.|
    |SG connector connection|Select one Connection and Credential Aliases option from the list for the Service Graph Connector for Microsoft SCCM. You set this connection up during the Guided Setup steps for Microsoft SCCM SGC.|
    |Validation detail|Details about the validation attempt.|

6.  Select **Save and Test Credentials**.

    A `Valid` response for a successful connection is required to proceed to the next step.

7.  Select **Next**.

    A PowerShell script is created automatically to retrieve mitigation details. A modal is displayed with the option to Validate script approval.

8.  To approve the script, log in to your Microsoft SCCM console with the Script Approver role.

    A PowerShell script has been generated in your SCCM Configuration manager to retrieve mitigation details. You must log in with the appropriate credentials with a user role that has the script approver permission in order to approve the script. After it is approved, you can validate it in your ServiceNow AI Platform instance.

9.  In your console, locate the **\[Servicenow Secops\]: Get System Mitigations** script and approve it.

    **Note:** In your SCCM configuration manager, the Script section is located under the software library. Locate: \[Servicenow Secops\]: Get System Mitigations script to approve it.

    This script remains in the **Waiting for approval** state until you approve it.

    You can validate the script in your ServiceNow AI Platform instance without approving it as described above, but the error message, `Script is not approved is displayed`.

10. To validate the approval, return to your ServiceNow AI Platform instance and in the Approve PowerShell script modal select **Validate script approval**.

11. Select **Done**.

    The configuration page should look like the screen in the following image.![SPC API Integrations page after successful configuration of Microsoft SCCM](../image/spc-api-integration-sccm.png)


