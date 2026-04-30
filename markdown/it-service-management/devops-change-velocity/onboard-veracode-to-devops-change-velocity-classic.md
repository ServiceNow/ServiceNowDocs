---
title: Onboard Veracode to DevOps Change Velocity - Classic
description: Connect to your Veracode instance to retrieve scan results.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Veracode to DevOps Change Velocity - Classic

Connect to your Veracode instance to retrieve scan results.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  In the Create DevOps tool form, enter the tool details:

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Veracode integration.|
    |Tool integration|Select Veracode.|
    |Tool username/ API ID|API ID of your Veracode instance.|
    |Tool password/ Access token / API Key|API key of your Veracode instance.|

    **Note:** You must have the Results and Upload and scan API roles for your Veracode credentials. For more information, see [https://docs.veracode.com/r/c\_API\_roles\_details](https://docs.veracode.com/r/c_API_roles_details)

3.  Click **Submit** to connect to your Veracode instance.

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

[Configure Veracode scans on your pipeline](configure-veracode-scans-on-your-pipeline.md)

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

