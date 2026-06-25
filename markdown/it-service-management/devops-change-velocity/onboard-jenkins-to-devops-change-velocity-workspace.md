---
title: Onboard Jenkins to DevOps Change Velocity — Workspace
description: Connect to your Jenkins instance using the DevOps Change Workspace playbook to discover pipelines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/onboard-jenkins-to-devops-change-velocity-workspace.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Jenkins to DevOps Change Velocity — Workspace

Connect to your Jenkins instance using the DevOps Change Workspace playbook to discover pipelines.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/setting-up-devops-change-velocity.md) topic.

Install and enable the **ServiceNow DevOps** plugin for Jenkins. If you've already installed it, update to the latest version. For instructions, see [Configure Jenkins plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-jenkins-plugin.md).

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the playbook to onboard Jenkins.

    You can connect a tool from an application if you also know which specific pipelines should be associated and tracked under that application to streamline the setup. This will allow you to easily associate and import data from Jenkins as well.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d44292e127">

Option

</th><th align="left" id="d44292e130">

Steps

</th></tr></thead><tbody><tr><td id="d44292e136">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to Jenkins as an orchestration tool, you'd select Jenkins under the **Orchestration** category.


</td></tr><tr><td id="d44292e166">

**Applications module**

</td><td>

1.  Select **Applications** \(\[Omitted image "applications-icon.png"\] Alt text: Applications icon.\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to Jenkins as an orchestration tool, you'd select Jenkins under the **Orchestration** category.


</td></tr><tr><td id="d44292e221">

**Tools module**

</td><td>

1.  Select **Tools** \(\[Omitted image "tools-icon-wkspc.png"\] Alt text: Tools icon.\) from the primary navigation.
2.  From the Capability list, select the appropriate category. For example, if you want to connect to Jenkins as an orchestration tool, select the **Orchestration** category.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Jenkins**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like pipelines while connecting to the tool, you must connect your tool from the Application module.

2.  In the **Tool name** field, enter a name for the tool.

    \[Omitted image "jenkins-workspace-connect-1.png"\] Alt text: Connect to the Jenkins tool screen

3.  On the **Jenkins instance details** playbook activity:

    1.  Enter the URL of your Jenkins instance.

    2.  Enter the login credentials \(password or access token or API token\) of the Jenkins instance.

        To generate API token, see [Connect to Jenkins using API token authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/authenticate-jenkins-using-api-token.md).

    3.  If your Jenkins instance is attached to a MID Server, select the MID Server option and enter its details.

        A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_MIDServerSelector.md)

4.  Select **Connect**.

    \[Omitted image "jenkins-workspace-connect-2.png"\] Alt text: Connect to the Jenkins tool - Enter instance details screen

5.  Permission checks are run on the credentials that you entered.

    Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see Jenkins permissions in [Permissions required for DevOps tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/tool-req-permission.md).

    You can choose to continue with the tool connection even if you don't have all the required permissions.

    \[Omitted image "jenkins-workspace-connect-3.png"\] Alt text: Connect to Jenkins tool - Permission checks screen

6.  Select **Next**.

7.  Specify the access for the tool.

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
    \[Omitted image "jenkins-workspace-connect-5.png"\] Alt text: Specify tool access

8.  Install the ServiceNow DevOps plugin for Jenkins.

    For more information on the extension, see [Configure Jenkins plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-jenkins-plugin.md).

    \[Omitted image "jenkins-workspace-connect-11.png"\] Alt text: Install Jenkins plugin.

9.  Select **Configure** to automatically set up **ServiceNow DevOps Configuration** in your Jenkins instance.

    **Important:**

    -   You must first install and enable the **ServiceNow DevOps** plugin for Jenkins. If you've already installed it, update to the latest version. For instructions, see [Configure Jenkins plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-jenkins-plugin.md).

    -   To configure webhooks automatically, Jenkins admin access is required.
    -   If you choose to automatically configure this tool, then the existing set up for **ServiceNow DevOps Configuration** in Jenkins will be over-written.
    -   You can add a total of ten ServiceNow configurations.
    \[Omitted image "jenkins-workspace-connect-8.png"\] Alt text: Configure webhooks automatically.

    \[Omitted image "jenkins-plugin.png"\] Alt text: Automatically sets up ServiceNow DevOps configuration in Jenkins

    To configure webhooks manually in Jenkins, see [Configure webhooks manually for Jenkins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-jenkins-plugin.md).

    You can also choose to enable nightly polling to retrieve data for any tracked pipelines by selecting the **Enable Polling** property option in the **Administration** module. See [DevOps Change Velocity properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-administration.md).

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then pipelines available in your instance are discovered. You can track and import historical data from them.
10. Select the pipelines that you want to track from **Select pipelines** playbook activity.

    For each selected pipeline, all steps are imported for the last successful execution.

    \[Omitted image "jenkins-workspace-connect-4.png"\] Alt text: Select pipelines to track.

11. In the Assign services to pipeline steps activity, specify **Step type** and **Service** for each pipeline step.

    \[Omitted image "jenkins-workspace-connect-6.png"\] Alt text: Assign services to pipelines in Jenkins.

    Completing this step as part of tool onboarding enables the DevOps Insights dashboards to show more meaningful data immediately.

12. If you want to import pipeline data, select the date range and select **Submit**.

13. From the **Summary** page, select **View tool record**to review the details of the connected Jenkins tool.

    \[Omitted image "jenkins-workspace-connect-7.png"\] Alt text: Summary page.

    **Note:** If your tool credential has changed, you must update the credentials in your ServiceNow instance. For more information, see [Update third-party tool credentials in DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/update-third-party-tool-credentials-in-devops-change-velocity.md).


## Result

You’ve successfully onboarded your Jenkins tool to DevOps Change Velocity.

**Parent Topic:**[Jenkins integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/jenkins-integration-dev-ops.md)

**Related topics**  


[Configure webhooks from the tool record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-webhooks-from-the-tool-record.md)

