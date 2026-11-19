---
title: Prepare SSRS for metadata collection
description: Configure SQL Server Reporting Services \(SSRS\) authentication and permissions to enable the metadata collector to harvest data sources, reports, and policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/preparing-to-run-sql-server-reporting-services-collector.html
release: brazil
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 2
keywords: [SSRS collector, SQL Server Reporting Services, metadata collector, authentication, permissions]
breadcrumb: [SQL Server Reporting Services \(SSRS\) metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare SSRS for metadata collection

Configure SQL Server Reporting Services \(SSRS\) authentication and permissions to enable the metadata collector to harvest data sources, reports, and policies.

## Before you begin

You must have administrator access to SQL Server Management Studio and your SSRS instance.

Role required: admin

## About this task

Before running the SSRS metadata collector, configure authentication and set up appropriate permissions. You can use the [Browser role](https://learn.microsoft.com/en-us/sql/reporting-services/security/role-definitions-predefined-roles?view=sql-server-ver16) for basic harvesting, or create a custom role to harvest data sources and policies.

## Procedure

1.  Create a custom role with permissions to harvest data sources and policies.

    You need to set up a custom role only if you want to harvest data sources and policies. Otherwise, you can skip this step and use the Browser role.

    1.  Open SQL Server Management Studio as an Administrator.

    2.  In the Object Explorer, select **Connect** &gt; **Reporting Services**.

    3.  Connect to your SSRS instance.

    4.  In the Object Explorer, navigate to **Security** &gt; **Roles**.

    5.  Right-click Roles and select **New Role**.

    6.  In the Name field, enter a role name.

        For example, enter `Content Viewer`.

    7.  Select the following tasks:

        -   View reports
        -   View resources
        -   View folders
        -   View data sources \(allows harvesting of data sources\)
        -   View models
        -   Consume reports
        -   Set security for individual items \(allows harvesting of policies, optional\)
    8.  Save the role.

    For complete details on creating roles, see the Microsoft documentation at [Role Definitions - Create, Delete, or Modify](https://learn.microsoft.com/en-us/sql/reporting-services/security/role-definitions-create-delete-or-modify?view=sql-server-ver16) and [Role Definitions - Predefined Roles](https://learn.microsoft.com/en-us/sql/reporting-services/security/role-definitions-predefined-roles?view=sql-server-ver16).

2.  Configure authentication for the collector.

    The collector harvests from SSRS using Basic or NTLM authentication.

    1.  If you are using basic authentication with a local machine user and your SSRS instance does not have basic authentication configured, configure basic authentication on your SSRS environment.

        For details, see the Microsoft documentation at [Configure Basic Authentication on the Report Server](https://learn.microsoft.com/en-us/sql/reporting-services/security/configure-basic-authentication-on-the-report-server?view=sql-server-ver16).

    2.  Create a domain user \(recommended\) or a local machine user that the collector will use for authentication and harvesting of SSRS objects.

    3.  Grant the user access to the report server and apply the [Browser role](https://learn.microsoft.com/en-us/sql/reporting-services/security/role-definitions-predefined-roles?view=sql-server-ver16) or apply the custom role with permissions to harvest data sources and policies.

        For details, see the Microsoft documentation at [Grant User Access to a Report Server](https://learn.microsoft.com/en-us/sql/reporting-services/security/grant-user-access-to-a-report-server?view=sql-server-ver16).

    4.  If required by your SSRS instance, set permissions at the folder level.

        1.  Navigate to the root folder or set of folders that you want to harvest resources from.
        2.  Select **Manage Folder** from the menu.
        3.  Select the user you set up for running the collector.

## Result

SSRS is configured with the required authentication and permissions. You can now run the SSRS metadata collector.

**Parent Topic:**[SQL Server Reporting Services \(SSRS\) metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sql-server-reporting-services-collector.md)

