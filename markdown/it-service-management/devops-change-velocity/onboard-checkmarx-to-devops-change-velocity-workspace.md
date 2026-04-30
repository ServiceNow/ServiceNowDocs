---
title: Onboard Checkmarx to DevOps Change Velocity - Workspace
description: Connect to your Checkmarx instance using the DevOps Change Workspace playbook.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Checkmarx, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Checkmarx to DevOps Change Velocity - Workspace

Connect to your Checkmarx instance using the DevOps Change Workspace playbook.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## About this task

Checkmarx has two types of tools - Checkmarx SAST and Checkmarx One.

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Checkmarx.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d157325e81">

Option

</th><th align="left" id="d157325e84">

Steps

</th></tr></thead><tbody><tr><td id="d157325e90">

**Homepage**

</td><td>

1.  Select the **Connect tools** widget
2.  On the  Connect to a tool  modal, select **Checkmarx One** or **Checkmarx SAST** from the **Security** category.


</td></tr><tr><td id="d157325e120">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\).
2.  Select an existing application, or create one. To create an application, see [Create an application - Classic](app-create-all.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select **Checkmarx One** or **Checkmarx SAST** from the **Security** category.


</td></tr><tr><td id="d157325e172">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\).
2.  From the Capability list, select **Security**.
3.  Select **Connect a tool**.
4.  On the  **Connect to a tool ** modal, select **Checkmarx One** or **Checkmarx SAST**.


</td></tr></tbody>
</table>2.  Enter a name to identify your tool and select **Next**. ![Connect to Checkmarx tool in playbook](../image/checkmarx-sast-pl01.png)

3.  On the instance details playbook activity section, enter the following credentials based on whether you are connecting to Checkmarx One or Checkmarx SAST.

<table id="choicetable_e1f_tgd_xyb"><thead><tr><th align="left" id="d157325e243">

Tool

</th><th align="left" id="d157325e246">

Steps

</th></tr></thead><tbody><tr><td id="d157325e252">

**Checkmarx SAST**

</td><td>

1.  In the **Server URL** field, enter the server URL of the Checkmarx SAST instance. ![Enter Checkmarx SAST instance details playbook activity](../image/checkmarx-sast-pl02.png)
2.  In the **API id** field, enter the API ID of your Checkmarx SAST instance.
3.  In the **API key** field, enter the API key of your Checkmarx SAST instance.


</td></tr><tr><td id="d157325e287">

**Checkmarx One**

</td><td>

1.  In the **CheckmarxOne Access Control Base URL** field, enter the Checkmarx One Access Control Base URL of your Checkmarx One instance. ![Enter Checkmarx One instance details playbook activity](../image/checkmarx-one-pl01.png)
2.  In the **CheckmarxOne API Base URL** field, enter the API base URL of your Checkmarx One instance.
3.  In the **Tenant** field, enter the name of the tenant of your Checkmarx SAST instance.
4.  In the **Client Id** field, enter the client ID of your Checkmarx SAST instance.
5.  In the **Client Secret** field, enter the client secret of your Checkmarx SAST instance.


</td></tr></tbody>
</table>    Ensure that your Checkmarx SAST user has a role that has permissions to read **Project** and **Scan Results** to get summary details. For more information, see [Checkmarx documentation](https://checkmarx.atlassian.net/wiki/spaces/KC/pages/1178009601/CxSAST+CxOSA+Roles+and+Permissions+v9.0.0+and+up). Ensure that your Checkmarx One user has the **create-scan** and **manage-project** roles to access Scan summary details. For more information, see [Checkmarx documentation](https://checkmarx.com/resource/documents/en/34965-68603-managing-roles.html).

4.  Select **Connect** and review the details of the successfully connected Checkmarx instance.

5.  Specify the access for the tool.

    1.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field.

        The tasks these users in the groups can perform depends on the role assigned to them.

        -   DevOps Tool Owner role: Can view and edit the tool.
        -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
        -   DevOps Administrator role: Can edit all tools.
        -   Other DevOps roles: Can view the tool.
        **Note:** If you don't select a group and skip this step, all users with the DevOps Tool Owner role will be able to edit the tool.

    2.  If you choose to control access to the tool, the **All App Owners can view and associate tool objects to applications** option becomes available for selection.

        This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

    3.  Select **Assign**.
    ![Specify tool access playbook activity](../image/checkmarx-sast-pl03.png)

6.  If this isn’t the first instance of the security tool you’re onboarding, select the orchestration tool to associate with your security tool instance from the Associate orchestration tool instances playbook activity.

    This activity isn’t displayed if this is the first security tool instance you’re onboarding.

    **Note:** This playbook activity is required only if you’re onboarding more than one security tool instances. When multiple security tool instances are onboarded in ServiceNow, you must associate only one of the security tool instances to the same orchestration tool or pipeline record.

    ![Associate orchestration tool instance playbook activity](../image/checkmarx-sast-pl04.png)

7.  From the Add custom action to pipelines playbook activity section, copy the required custom action code and add it as a step in your pipeline.

    -   If only one security instance is onboarded in ServiceNow, the pipelines will be automatically associated with Checkmarx when the pipeline is run.
    -   If this is the first security tool instance you’re onboarding, the custom action codes for the orchestration tool that you’ve onboarded in ServiceNow will be available to copy.
        -   If you are using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always.
        -   You can configure Checkmarx scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity. If you’re using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always. If you’re using Jenkins, and your pipeline already has a Checkmarx One security scan \(checkmarxASTScanner\) step, you don’t have to add the custom action code in your pipeline. For Checkmarx SAST, the custom action code must be added in your pipeline even if it has the security scan step \(checkmarxASTScanner\).
    -   If this is the not the first security tool instance you’re onboarding, the respective custom action codes for orchestration tools that you’ve selected in step 6 will be available to copy. If you’re using Jenkins, and your pipeline already has a Checkmarx One security scan \(checkmarxASTScanner\) step, you don’t have to add the custom action code in your pipeline.
    -   If you want to configure Checkmarx for the GitLab tool, you can either use the generic Docker container image to add the Checkmarx security step or perform the steps specified in the [Integrate security tools with GitLab](configure-security-tool-for-gitlab.md) topic.
    -   For Harness pipelines, you can configure Checkmarx scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using generic Docker container image](../concept/servicenow-custom-actions-for-gitlab.md)
    -   Alternatively, you can associate pipeline with security tool instance by adding security tool ID to the custom action code. This will override any previously associated security tool instance.
    ![Add custom actions to pipeline playbook activity Checkmarx SAST](../image/checkmarx-one-pl05.png)

8.  Mark the activity as complete.

9.  From the **Summary** page, select **View tool record** to review the details of the connected instance.

    ![Playbook summary page](../image/checkmarx-06.png)


## What to do next

[Configure Checkmarx scans on your pipeline](../concept/configure-checkmarx-scans-on-your-pipeline.md)

**Parent Topic:**[Checkmarx integration with DevOps Change Velocity](../concept/checkmarx-integration-with-devops-change-velocity.md)

