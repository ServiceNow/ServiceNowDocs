---
title: Configure the Application Administrator role on the SCCM server
description: To deploy software using ServiceNow Client Software Distribution \(CSD\), ensure that an SCCM administrative user has the correct permissions to deploy software and that PowerShell is properly configured.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Configure the Application Administrator role on the SCCM server

To deploy software using ServiceNow® Client Software Distribution \(CSD\), ensure that an SCCM administrative user has the correct permissions to deploy software and that PowerShell is properly configured.

## Before you begin

SCCM role required: Application Administrator

## About this task

These instructions are for Microsoft 2012 R2 Server.

## Procedure

1.  In the System Center Configuration Manager console, navigate to **Administration** &gt; **Security** &gt; **Administrative Users**.

2.  Right-click the user to whom you want to grant the Application Administrator role.

3.  Select **Properties** from the drop-down menu.

4.  In the Properties dialog box, select the **Security Roles** tab.

5.  Ensure that the user has the Application Administrator role.

6.  If the user does not already have this role, click **Add**, select this role from the list, and click **OK**.

7.  Log into SCCM as the user with the Application Administrator role.

8.  Open the menu from the upper left corner of the console and select **Connect via Windows PowerShell**.

9.  Ensure that the user can access the CM console.

    This action establishes the environment path to PowerShell for the logged in Application Administrator user.


**Parent Topic:**[Configuring SCCM](../concept/configuring-sccm.md)

