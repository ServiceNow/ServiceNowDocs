---
title: Onboard Checkmarx to DevOps Change Velocity - Classic
description: Connect to your Checkmarx instance to retrieve scan results.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Checkmarx, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Checkmarx to DevOps Change Velocity - Classic

Connect to your Checkmarx instance to retrieve scan results.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  In the Create DevOps tool form, enter the tool details based on whether you are onboarding Checkmarx SAST or Checkmarx One.

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Checkmarx integration.|
    |Tool integration|Checkmarx SAST.|
    |Server URL|Base URL of your Checkmarx One intance.|
    |Tool username/ API ID|API ID of your Checkmarx instance.|
    |Tool password/ Access token / API Key|API key of your Checkmarx instance.|
    |MID server|MID server associated with the Checkmarx One instance.|

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Checkmarx integration.|
    |Tool integration|Checkmarx One.|
    |CheckmarxOne Access Control Base URL|Access Control Base URL of your Checkmarx One instance.|
    |CheckmarxOne API Base URL.|API Base URL of your Checkmarx One instance.|
    |Tenant|Name of your Checkmarx One tenant account.|
    |Client Id|Name you used to store your Checkmarx Client ID in your repository.|
    |Client Secret|Name you used to store your Checkmarx Secret in your repository.|

    Ensure that your Checkmarx SAST user has a role that has permissions to read **Project** and **Scan Results** to get summary details. For more information, see [Checkmarx documentation](https://checkmarx.atlassian.net/wiki/spaces/KC/pages/1178009601/CxSAST+CxOSA+Roles+and+Permissions+v9.0.0+and+up). Ensure that your Checkmarx One user has the **create-scan** and **manage-project** roles to access Scan summary details. For more information, see [Checkmarx documentation](https://checkmarx.com/resource/documents/en/34965-68603-managing-roles.html).

3.  Click **Submit** to connect to your Checkmarx instance.

4.  On successful tool creation, you're taken to the tool record page.
5.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.


## What to do next

[Configure Checkmarx scans on your pipeline](../concept/configure-checkmarx-scans-on-your-pipeline.md)

**Parent Topic:**[Checkmarx integration with DevOps Change Velocity](../concept/checkmarx-integration-with-devops-change-velocity.md)

