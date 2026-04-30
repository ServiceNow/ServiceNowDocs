---
title: Create multiple instances for the Microsoft Defender Mitigation Control Integration
description: You can configure multiple instances for the Microsoft Defender Mitigation Control Integration.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Install Microsoft integrations, Policies for Exploit Protection \(EDR\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Create multiple instances for the Microsoft Defender Mitigation Control Integration

You can configure multiple instances for the Microsoft Defender Mitigation Control Integration.

## Before you begin

Roles required:

-   SPC Admin Group and SPC Analyst Group for configuration of new integration instances in the workspace
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

1.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations**.

2.  Select **New**.

    The New Defender instance modal is displayed.

3.  Enter a name for your new instance and select **Create instance**.

    The SPC API Integrations page is displayed with the instance provided with the application and your new instance.

4.  Select the link for your new instance.

5.  Fill out the fields in the SCCM credentials configuration modal for your new instance.

<table id="table_rzb_crm_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Field is populated automatically with the instance name.

</td></tr><tr><td>

Connection

</td><td>

Create a new connection.1.  Select **Create Connection and Alias** at the top of the modal.
2.  In the Connection and Credential Aliases form, fill out the mandatory fields.

    -   **Name** - Unique name
    -   **Type** - Connection and Credential
    -   **Connection type** - Basic
**Note:** Do not select **Submit** at this time.

3.  Right-click anywhere in the gray header and select **Save**.

The page refreshes and related links and tabs are displayed at the bottom of the page after you save it.

4.  With the Connections tab selected, select **New** at the right of the tab.

The Connection form is displayed. Fill out the fields.

    -   **Name** - Unique name
    -   Credential - Select the search icon. Locate the Windows credentials and select the link. On the Windows Credentials form, fill out the fields.
        -   **Name** - Unique name
        -   Username - User name for the credentials. This is the user name that will be referenced for the Username field in the SCCM credentials configuration modal after you save it on this page.
        -   Password - Password for the credentials. This is the password that will be referenced for the password field in the SCCM credentials configuration modal after you save it on this page.
    -   Host - This is the Host for the SCCM server that will be referenced in the Host field in the SCCM credentials configuration modal after you save it on this page.
5.  Select the **Use MID Server** check box. Select Specific MID Server for **MID Selection** and select one from the MID Server list.
6.  Right-click anywhere in the gray header and select **Save**. These are the credentials you enter on the Connection form described above in step d.


</td></tr><tr><td>

Host

</td><td>

This is the Host for the SCCM server referenced from the Host field after you save it on the Connection page as described above.

</td></tr><tr><td>

User name

</td><td>

This is the user name referenced from the Username field after you save it on the Connection page as described above.

</td></tr><tr><td>

Password

</td><td>

This is the password referenced from the Password field after you save it on the Connection page as described above.

</td></tr><tr><td>

MID Server

</td><td>

This is the MID Server referenced from the MID Server fields after you save it on the Connection page as described above.

</td></tr><tr><td>

Validation status

</td><td>

Field populated after validation attempt. If the connection successful, the integration instance state is **Valid**.

</td></tr><tr><td>

SG connector connection

</td><td>

Select one Connection and Credential Aliases option from the list for the Service Graph Connector for Microsoft SCCM. You set this connection up during the Guided Setup steps for Microsoft SCCM SGC.

</td></tr><tr><td>

Validation detail

</td><td>

Details about the validation attempt.

</td></tr></tbody>
</table>6.  Navigate to **Connectors and use cases setup** &gt; **SPC API Integrations**.

7.  Select the link for your new instance.

8.  In the SCCM credentials configuration modal, select the connection from the list that you created in step 5 for the Connection field.

    Note that the fields listed below are auto-populated based on the information you entered for your new connection.

    | | |
    |---|---|
    |Host|This is the Host for the SCCM server referenced from the Host field after you save it on the Connection page as described above.|
    |User name|This is the user name referenced from the Username field after you save it on the Connection page as described above.|
    |Password|This is the password referenced from the Password field after you save it on the Connection page as described above.|
    |MID Server|This is the MID Server referenced from the MID Server fields after you save it on the Connection page as described above.|
    |Validation status|Field populated after validation attempt. If the connection successful, the integration instance state is **Valid**.|
    |SG connector connection|Select one Connection and Credential Aliases option from the list.|
    |Validation detail|Details about the validation attempt.|

9.  Select **Save and Test Credentials**.

    A `Valid` response for a successful connection is required to proceed to the next step.

10. Select **Next**.

    The PowerShell script is created as described in [Install and configure the Service Graph Connector for Microsoft SCCM and the Microsoft Defender Mitigation Control Integration](spc-install-config-sccm-defender.md). Follow the steps in that topic to approve the scripts for your new instances.


