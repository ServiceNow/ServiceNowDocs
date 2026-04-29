---
title: Onboard Veracode to DevOps Change Velocity - Workspace
description: Connect to your Veracode instance using the DevOps Change Workspace playbook.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Veracode to DevOps Change Velocity - Workspace

Connect to your Veracode instance using the DevOps Change Workspace playbook.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Veracode.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d279406e93">

Option

</th><th align="left" id="d279406e96">

Steps

</th></tr></thead><tbody><tr><td id="d279406e102">

**Homepage**

</td><td>

1.  Select the **Connect tools** widget
2.  On the  Connect to a tool  modal, select Veracode from the **Security** category.


</td></tr><tr><td id="d279406e129">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\).
2.  Select an existing application, or create one. To create an application, see [Create an application - Classic](app-create-all.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Veracode from the **Security** category.


</td></tr><tr><td id="d279406e178">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\).
2.  From the Capability list, select **Security**.
3.  Select **Connect a tool**.
4.  On the  **Connect to a tool ** modal, select **Veracode**.


</td></tr></tbody>
</table>2.  Enter a name to identify your tool and select **Next**.![Connect to Veracode tool in playbook](../image/veracode-playbook-07.png)

3.  On the Enter Veracode instance details playbook activity section, enter the following credentials:

    1.  In the **API id** field, enter the API ID of your Veracode instance.
    2.  In the **API key** field, enter the API key of your Veracode instance.
    **Note:** Ensure that your Veracode credentials have the following API roles.

    -   Upload and Scan
    -   Results
    For more information, see [https://docs.veracode.com/r/c\_API\_roles\_details](https://docs.veracode.com/r/c_API_roles_details).

4.  Select **Connect** and review the details of the successfully connected Veracode instance.

    ![Playbook activity to enter Veracode instance details](../image/veracode-playbook-02.png)

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
    ![Playbook activity to specify access level](../image/veracode-playbook-03.png)

6.  If this isn’t the first instance of the security tool you’re onboarding, select the orchestration tool to associate with your security tool instance from the Associate orchestration tool instances playbook activity.

    This activity isn’t displayed if this is the first security tool instance you’re onboarding.

    **Note:** This playbook activity is required only if you’re onboarding more than one security tool instances. When multiple security tool instances are onboarded in ServiceNow, you must associate only one of the security tool instances to the same orchestration tool or pipeline record.

    ![Playbook activity to associate orchestration tool instances to a security tool](../image/veracode-playbook-4.png)

7.  From the Add custom action to pipelines playbook activity section, copy the required custom action code and add it as a step in your pipeline.

    -   If only one security instance is onboarded in ServiceNow, the pipelines will be automatically associated with Veracode when the pipeline is run.
    -   If this is the first security tool instance you’re onboarding, the custom action codes for the orchestration tool that you’ve onboarded in ServiceNow will be available to copy.
        -   If you are using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always.
        -   If you’re using Jenkins, and your pipeline already has a Veracode security scan step, you don’t have to add the custom action code in your pipeline. Ensure that your Veracode security scan step has **waitForScan: true**. This is required for the system to retrieve the scan information.
    -   If this is the not the first security tool instance you’re onboarding, the respective custom action codes for orchestration tools that you’ve selected in step 6 will be available to copy. If you’re using Jenkins, and your pipeline already has a Veracode security scan step, you don’t have to add the custom action code in your pipeline. Ensure that your Veracode security scan step has **waitForScan: true**. This is mandatory for the system to retrieve the scan information.
    -   If you want to configure Veracode for the GitLab tool, you can either use the generic Docker container image to add the Veracode security step or perform the steps specified in the [Integrate security tools with GitLab](configure-security-tool-for-gitlab.md) topic.
    -   For Harness pipelines, you can configure Veracode scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using a generic Docker container image](../concept/servicenow-custom-actions-for-gitlab.md).
    -   Alternatively, you can associate pipeline with security tool instance by adding security tool ID to the custom action code. This will override any previously associated security tool instance.
    ![Playbook activity to copy custom action code](../image/veracode-playbook-05.png)

    For information on configuring the Veracode scans on your pipeline, see [Configure Veracode scans on your pipeline](configure-veracode-scans-on-your-pipeline.md)

8.  Mark the activity as complete.

9.  From the **Summary** page, select **View tool record** to review the details of the connected instance.

    ![Summary page in playbook](../image/veracode-playbook-06.png)


## What to do next

[Configure Veracode scans on your pipeline](configure-veracode-scans-on-your-pipeline.md)

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

