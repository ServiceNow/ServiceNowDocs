---
title: Create a script in Microsoft Endpoint Configuration Manager
description: Create a script in the Microsoft Endpoint Configuration Manager to configure the display of the processes metrics on the Investigation tab of the Incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/create-mecm-script.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a script in Microsoft Endpoint Configuration Manager

Create a script in the Microsoft Endpoint Configuration Manager to configure the display of the processes metrics on the **Investigation** tab of the Incident record.

## Before you begin

The Microsoft Endpoint Configuration Manager server must be logged in using the Microsoft Remote Desktop.

Role required: admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  On the Microsoft Endpoint Configuration Manager, select **Software Library**.

3.  On the Software Library section, select **Scripts** and click **Create Script**.

    Alternatively, you can also right-click **Scripts** and select **Create Script**.\[Omitted image "select-create-script.png"\] Alt text: Select create script option

4.  Specify **Script name**.

5.  Add the script on the script field \(block\).

    \[Omitted image "add-script-block.png"\] Alt text: Add script block

6.  Click **Next**.

7.  Click **Next &amp; Close**.

    A script record is created with **Approval State** as **Waiting for Approval**.

8.  Select the script record.

9.  Select the **Approve/Deny** option and then click **Approve** to approve the script.

    Alternatively, you can also right-click on the created script record and select the **Approve/Deny** option and then click **Approve**.\[Omitted image "approve-script-record.png"\] Alt text: Approve script record

10. Get the script GUID.

    1.  Open power shell console using **Connect via Windows PowerShell ISE**.

        \[Omitted image "connect-window-power-shell.png"\] Alt text: Connect via Windows Powershell ISE

    2.  Get the script GUID by running the command `Get-CMScript -ScriptName 'GetProcess' | Select ScriptGuid`.

        \[Omitted image "script-guid-command.png"\] Alt text: Run command for script GUID


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.md)

