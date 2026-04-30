---
title: Create Windows credentials for SCCM deployments
description: Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create Windows credentials for SCCM deployments

Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.

## Before you begin

Role required: sn\_client\_sf\_dist.csd\_admin or admin

## About this task

Client software distribution requires Windows credentials that have administrative rights on the SCCM server.

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Credentials**.

2.  Click **New**.

3.  In the list of credential types, select **Windows Credentials**.

4.  Provide a user name and password with administrative rights on the SCCM server.

    **Important:** Ensure the following:

    -   This user must have the Application Administrator role on the SCCM server.
    -   Use the credentials to log into the SCCM Server and connect via Windows PowerShell from the System Center Configuration Manager console at least once to set the path variable for that credential.
5.  Fill in the other fields on the form, as appropriate.

    For details, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

6.  Click **Submit**.


**Parent Topic:**[Configuring SCCM](../concept/configuring-sccm.md)

