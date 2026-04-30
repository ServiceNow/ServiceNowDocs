---
title: Configure Jenkins plugin
description: Configure Jenkins to send real time notifications for your pipeline executions to DevOps Change Velocity.Configure webhooks in Jenkins to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure Jenkins plugin

Configure Jenkins to send real time notifications for your pipeline executions to DevOps Change Velocity.

## Before you begin

Role required: Jenkins admin

## Procedure

1.  Install the **ServiceNow DevOps** plugin from the Jenkins Marketplace by navigating to **Manage Jenkins &gt; System configuration &gt; Plugins** in your Jenkins instance.

2.  Search for **ServiceNow DevOps Plugin** and select it, and then select **Install**.


**Parent Topic:**[Jenkins integration with DevOps Change Velocity](../concept/jenkins-integration-dev-ops.md)

**Related topics**  


[Configure webhooks manually for Jenkins](configure-jenkins-plugin.md#)

## Configure webhooks manually for Jenkins

Configure webhooks in Jenkins to send sync notifications to the DevOps Change Velocity application.

### Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity, Jenkins admin

### About this task

You can add a total of ten ServiceNow DevOps configurations. For example, you can configure Jenkins connections for your Development, Testing, Production instances, and so on.

If you are an upgrading customer, you must download and install the latest Jenkins plugin to enable multiple ServiceNow configurations. After installation, your existing configuration will be retained and made the default configuration.

In the ServiceNow DevOps Configuration section in Jenkins, the values in the **Name** field and the combination of the **Instance URL** and **Orchestration Tool ID** fields must be unique.

If you choose to automatically configure a tool from ServiceNow, then the existing set up for ServiceNow DevOps Configuration will be over-written in Jenkins.

If DevOps Config is installed, you will only be able to configure Jenkins manually.

### Procedure

1.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    ![Configure webhooks automatically.](../image/jenkins-workspace-connect-8.png)

2.  Select **Copy** in the appropriate field to copy the value to your clipboard.

    The field label changes to **Copied**, but you can copy multiple times.

    ![Configure webhooks manually.](../image/jenkins-workspace-connect-9.png)

3.  In Jenkins, navigate to **Manage Jenkins** &gt; **System configuration** &gt; **Manage Plugins** &gt; **Configure System**.

4.  In the ServiceNow DevOps Configuration section, select **Add**.

    **Note:** You can add multiple connections by selecting **Add** for each new configuration.

5.  Configure the plugin by filling in the fields.

    When enabled, Jenkins starts sending events to DevOps as inbound events.

    **Note:** Values are case-sensitive.

    ![Fields to be configured in Jenkins.](../image/jenkins-plugin.png)

<table id="table_b1g_c3x_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Select this option to make the connection active. By default this option is selected when you select **Add** for a new connection.**Note:** All the connections that have Active enabled, will send webhook notifications for your pipeline execution,however for the change step only the connection specified will be considered.

</td></tr><tr><td>

Default

</td><td>

Select this option to make the connection the default one when the connection name is not passed in an existing step on a pipeline. **Note:** Not selecting this option when only one connection is available will result in error.

</td></tr><tr><td>

Name

</td><td>

Unique name of the connection. **Note:** The name value is auto-generated when you auto configure a connection from ServiceNow.

</td></tr><tr><td>

Instance URL

</td><td>

Enter your ServiceNow instance URL you copied in step 2. For example, `https://<your-instance>.service-now.com`.

</td></tr><tr><td>

Orchestration Tool ID

</td><td>

The sys\_id of the orchestration tool you copied in step 2.

 Alternatively, you can copy this value from the webhook URL \(*toolid* value\), or obtain it directly using the `Copy sys_id` command on the Orchestration Tool record.

 **Note:** The combination of the Instance URL and Orchestration Tool ID values must be unique for each connection.

</td></tr><tr><td>

Artifact Tool ID

</td><td>

The sys\_id of the artifact tool.

</td></tr><tr><td>

Credentials

</td><td>

Select the basic authentication credentials that you want to use for connecting to Jenkins.

 1.  To add credentials, select **Add**.
2.  In the **Username** field, enter your DevOps Integration User details. By default, it is devops.integration.user.
3.  In the **Password** field, enter your DevOps Integration User password.


</td></tr><tr><td>

Secret Credentials

</td><td>

Select the secret token that you copied in step 2. Alternatively, you can perform the following steps to obtain the secret token from the tool record.

 1.  Copy the secret token for your Jenkins tool in DevOps Change.
    -   Workspace: Navigate to the tool record, select **Configure** and copy the secret token.
    -   Classic UI: Navigate to the tool record and select **Copy token**.
2.  To add tokens, select **Add**.
3.  From the **Kind** list, select **Secret text**.
4.  In the **Secret** field, enter the secret token generated while creating the Jenkins tool connection in DevOps.
5.  In the **ID** field, enter a name for the token.


</td></tr><tr><td>

Log Level

</td><td>

The level of log messages you want to store in Jenkins logs/ ServiceNow log recorder.Select from one of the following options:

-   inherit
-   off
-   severe
-   warning
-   info
-   config
-   fine
-   finer
-   finest
-   all
 For more information on Log levels and log recorders, see [Jenkins log levels and Log Recorders](../reference/devops-jenkins-log-recorders.md)

</td></tr><tr><td>

Force Tracking Check

</td><td>

Select the check box to make a REST \(POST\) API call to Jenkins for each pipeline execution to determine whether the pipeline is tracked or not.

 Clear the check box to store details in the **snPipelineInfo.json** file and stop making API calls for every pipeline execution.

 **Note:** When a pipeline is tracked, all active Jenkins configurations will receive job notifications.

</td></tr><tr><td>

Pull Request Pipeline Tracking Check

</td><td>

Select the check box to enable tracking for pull request pipelines.

 **Note:** When a pipeline is tracked, all active Jenkins configurations will receive job notifications.

</td></tr></tbody>
</table>6.  Select **Test Connection**.

    Verify that the connection successful message displays.

    -   If you've added basic authentication credentials, on successful connection, you will see the message: `Connection using 'Credentials' is successful`.
    -   If you've added the secret token, on successful connection, you will see the message: `Connection using 'Secret Credentials' is successful`.
7.  Select **Apply** to apply the changes and select **Save**.


