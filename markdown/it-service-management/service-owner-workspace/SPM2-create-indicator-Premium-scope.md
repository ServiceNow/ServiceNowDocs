---
title: Create indicators in Service Portfolio Management Premium
description: Create custom indicators for your Service Portfolio Management Premium jobs in the correct scope.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Create indicators in Service Portfolio Management Premium

Create custom indicators for your Service Portfolio Management Premium jobs in the correct scope.

## Before you begin

Role required: pa\_admin

## About this task

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Set up Service Owner Workspace](../image/SOWSetupBanner2.png "Navigate")

</td></tr></tbody>
</table>You must have the Reporting file type delegated developer access to change the scope from Global to Service Portfolio Management Premium when creating custom indicators for the application. Administrators grant the Reporting file type delegated developer access. For information regarding obtaining delegated developer access, refer to [Create indicators in Service Portfolio Management Premium](SPM2-create-indicator-Premium-scope.md).

When you create an indicator and associate it with a job in an application, both the indicator and the job must be in the same scope. Jobs and indicators available in the Service Portfolio Management Premium base system are in the correct Service Portfolio Management Premium scope. However, when you create a custom indicator, by default it is created in the Global scope. To associate a custom indicator with a Service Portfolio Management Premium job, you need to first change the scope from Global to Service Portfolio Management Premium.

![Create automatic indicators](../image/SOW_createdautomatedindicators.gif)

## Procedure

1.  Click the Settings ![Settings icon](../../../common/image/Banner_GearIcon.png) icon in the banner.

2.  In **System Settings**, click **Developer**.

3.  In **Application**, find and select Service Portfolio Management Premium.

4.  Navigate to **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** and click **New** to create an indicator in the Service Portfolio Management Premium scope.

    For details on how to create an automated indicator, refer to [Create an automated indicator](https://www.servicenow.com/docs/access?context=t_CreateAnAutomatedIndicator&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).


