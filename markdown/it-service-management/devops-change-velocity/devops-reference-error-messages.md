---
title: Common errors in DevOps Change Velocity
description: Identify the root cause of errors that occur in DevOps Change Velocity, and see the corresponding steps that might resolve them.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# Common errors in DevOps Change Velocity

Identify the root cause of errors that occur in DevOps Change Velocity, and see the corresponding steps that might resolve them.

## Tool connection

This table lists the steps required to resolve the errors that might occur when you select the **Submit** or **Connect** button after entering the tool details in the tool connection process:

<table id="table_scf_prj_v5b"><thead><tr><th>

Message

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Tool cannot be created because the tool name has not been entered. Enter the tool name, and try again.

</td><td>

Re-enter the tool name.

</td></tr><tr><td>

Tool cannot be created because the tool integration has not been selected. Select the correct tool integration value, and try again.

</td><td>

Select the correct tool integration value.

</td></tr><tr><td>

Tool cannot be created because the tool URL is invalid or incorrect. Re-enter the tool URL, and try again.

</td><td>

Re-enter the tool URL.

</td></tr><tr><td>

Tool cannot be created because the platform version cannot be determined. Create the glide.buildtag.last sys property, and try again.

</td><td>

1.  Navigate to **DevOps &gt; Administration &gt; Properties**.
2.  Verify if the **glide.buildtag.last sys** property exists.
3.  If not, create the **glide.buildtag.last sys** property.

</td></tr><tr><td>

Tool cannot be created because the associated CreateDevOps tool connection is invalid. Create a valid connection alias, and try again.

</td><td>

1.  Navigate to **All &gt; Connections &amp; Credentials &gt; Connection &amp; Credential Aliases** and open the **CreateDevOpsTool** record.
2.  In the Connections related list, create a record and enter a name for the connection.
3.  On the Connection form, select the **Credential** field lookup list, and then select **New** to create an admin credential.
4.  Select **Basic Auth Credentials** and enter a name.
5.  Enter admin username and password \(required to access the tools in your DevOps environment\).

A user with connection\_admin role can configure an HTTP connection.

6.  On the Connection form, enter **https://&lt;instance name&gt;.service-now.com/** for the Connection URL.

</td></tr><tr><td>

Tool cannot be created because the CreateDevOpsTool alias credentials are incorrect. Update the credential record, and try again.

</td><td>

1.  Select the **credential record** link in the message. If you are connecting to the tool from the workspace UI, right-click on the credentials record link, and select **Open in a new tab**.
2.  In the credentials record page, enter the correct credentials in the **Username** and **Password** fields.
3.  Save the changes, and retry connecting to the tool.

</td></tr><tr><td>

Tool cannot be created because the connection URL of the CreateDevOpsTool alias is incorrect. Use the following URL: https://&lt;instancename&gt;.service-now.com,and try again.

</td><td>

1.  Navigate to **All &gt; Connections &amp; Credentials &gt; Connection &amp; Credential Aliases** and open the **CreateDevOpsTool** record.
2.  On the Connection form, enter **https://&lt;instance name&gt;.service-now.com/** for the Connection URL.

</td></tr><tr><td>

To create a connection alias, you need the connection\_admin role. Contact your system administrator.

</td><td>

This error occurs if the connection alias field is empty for a tool record. To create the tool connection, you need a connection alias. Only a user having the**connection\_admin** role can create a connection alias. You must reach out to a user having this role, like an administrator, and get the connection alias created.

</td></tr><tr><td>

Tool cannot be created because the &lt;toolname&gt; tool name already exists. Enter a different name, and try again.

</td><td>

Use a different name for the tool.

</td></tr><tr><td>

Tool cannot be created because the &lt;toolname&gt; does not have a valid MID server configuration. Configure a valid MID server, and try again.

</td><td>

1.  If you are using the workspace, check if the mid server is running and reachable.
2.  If you are using the catalog and record producer, check if the mid server is running and reachable with application as DevOps and Capability as REST.

</td></tr><tr><td>

Tool cannot be created because there are no connection and credentials aliases available for DevOps Data Model scope. Create a new connection and credential alias, and try again.

</td><td>

This error occurs for OAuth authentication.

 1.  Navigate to **All &gt; Connections &amp; Credentials &gt; Connection &amp; Credential Aliases**.
2.  Create a new alias with the application as **DevOps Data Model**.

</td></tr><tr><td>

Tool cannot be created due to a technical issue while creating the credential record.

</td><td>

1.  Navigate to **All &gt; Process Automation &gt; Flow Designer &gt; Executions**.
2.  Check for the latest execution of the sn\_devops.devops\_create\_credentials subflow to know the details of the error.

</td></tr><tr><td>

Tool cannot be created because credential and domain combination for an active record already exists.

</td><td>

This error occurs for OAuth authentication.

 1.  Use a different credential.
2.  Check if the existing credential is used by any active connection.

</td></tr><tr><td>

Tool cannot be created due to a technical issue while creating the connection record.

</td><td>

1.  Navigate to **All &gt; Process Automation &gt; Flow Designer &gt; Executions**.
2.  Check for the latest execution of **sn\_devops.create\_connection\_for\_tool** action to know the details of the error.

</td></tr><tr><td>

Tool cannot be created because of the following reasons: -   The validate subflow is not configured, and
-   An integration capability record with the same subflow name does not exist for the associated tool integration.

Configure the subflow, and create the integration capability record with the Validate action and a subflow name for the tool integration, and try again.

</td><td>

This error occurs only for custom tool integrations.

 1.  Navigate to **All &gt; Process Automation &gt; Flow Designer**.
2.  In the Flow Designer page, select the **Subflows** tab.
3.  Open the **DevOps Demo Validate Subflow** record from the list.
4.  From the Actions section, open the **DevOps Demo Validate Action** record by selecting the Open action in Action Designer \(![Open action in Action Designer icon](../image/openactionfdicon.png)\) icon.
5.  Select **More Actions menu &gt; Copy Action**.![Copy action dialog box](../image/validate-action-copy-dialog.png)
6.  Enter a new name for the action and select the application as **DevOps Integrations**, and select **Copy**.
7.  In the copied action, select **Inputs &gt; REST step**.
8.  In the Request Details section, enter resource path of your custom tool in the **Resource Path** field.![Validate action screen](../image/validate-action-copy.png)
9.  Enter the API version of your custom tool in the **Query Parameters** field.
10. Save the changes.
11. Publish the action by selecting **Publish**.
12. Navigate back to the **DevOps Demo Validate Subflow** record.
13. Select **More Actions menu &gt; Copy Subflow**.
14. Enter a new name for the subflow and select the application as **DevOps Integrations**, and select **Copy**.
15. In the copied subflow, delete the **DevOps Demo Validate Action** action and add the action you created in step 11.![Add new action record](../image/validate-add-action.png)
    1.  In the **Action** field, select the action you created in step 11.
    2.  In the **aliasGR** field, select the Connection &amp; Credential Alias record from the **Data &gt; Lookup records** section.
    3.  In the **apiversion** field, select the api version from the **Data &gt; Subflow Inputs** section.
    4.  Save the changes.
16. Publish the subflow by selecting **Publish**.
17. Navigate to **DevOps &gt; Integrations &gt; Integration Capabilities** and create a record with the **Validate** action.

For more information, see [Create a DevOps tool integration](../task/set-up-dev-ops-integrations.md).

![Integration Capabilities related tab](../image/validate-associate-subflow.png)

18. Associate the subflow you created in step 16 with the integration capability record.

</td></tr><tr><td>

Tool cannot be created due to a connectivity issue. Check the &lt;validate\_subflow\_name&gt; subflow for more details, and try again.

</td><td>

1.  Navigate to **All &gt; Process Automation &gt; Flow Designer &gt; Executions**.
2.  Check for the latest execution of &lt;validate\_subflow\_name&gt; subflow to know the details of the error.

</td></tr><tr><td>

Tool authorization credentials are invalid. Enter valid credentials, and try again.

</td><td>

Re-enter the correct username/password for the tool.

</td></tr><tr><td>

Tool cannot be created because there is no response received from the server. Enter a valid tool URL or Check if server is up and running, and try again.

</td><td>

1.  Re-enter the tool URL.
2.  Check the mid server.

</td></tr><tr><td>

The connection URL is incorrect, check theURL and try again.

</td><td>

Re-enter the tool URL.

</td></tr><tr><td>

Tool cannot be connected because the GitHub app slug name is incorrect. Enter the correct GitHub app slug name and try again.

</td><td>

You can find the GitHub app slug name on the settings page of your GitHub app. The GitHub app slug name is the URL-friendly name of your GitHub app. For example, if you have created a GitHub app with the name **Test App**, the corresponding URL-friendly GitHub app slug name will be **test-app**. In your GitHub url - "https://github.com/settings/apps/test-app", "test-app" is the GitHub app slug name. For more information, see [GitHub documentation](https://docs.github.com/en/rest/apps/apps?apiVersion=2022-11-28#get-an-app).

</td></tr><tr><td>

Password value is too long and could be truncated after encryption. Please either reduce password length or increase field size.

</td><td>

From 18th January 2023, Jira has extended the length of API tokens for Atlassian accounts. You must increase the maximum password value to more than 255 in the discovery\_credentials table to accommodate the extended character length. For more information, see the [KB1269878](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1269878) kb article and [Atlassian documentation](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/).

</td></tr><tr><td>

Unexpected behaviour from remote host: Circular redirect to 'https://bitbucket.org/account/signin/?next=%2F...%2Frest%2Fapi%2F1.0%2Fusers'.

</td><td>

This error might occur if you try to connect to a BitBucket Cloud instance. BitBucket Cloud is not supported. You must use a BitBucket Server instance to connect to ServiceNow DevOps. Connect to your BitBucket instance via an MID server. A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md)

</td></tr><tr><td>

Mismatch in tool URL: Tool URL entered in ServiceNow: https://&lt;URL of the Jenkins instance you entered&gt; Tool URL entered in Jenkins: https://&lt;Jenkins location URL entered in Jenkins&gt; In Jenkins, under Manage Jenkins &gt; System, check that your configured Jenkins URL is the same as the Tool URL entered here. See the troubleshooting tool on-boarding errors.

</td><td>

This error occurs when the Jenkins URL entered in DevOps is different from the Jenkins URL entered in your Jenkins instance.

 From your Jenkins instance, navigate to **Manage Jenkins** &gt; **System** &gt; **Jenkins Location**. The **Jenkins URL** entered here must match the **URL of the Jenkins instance** entered in DevOps.

</td></tr></tbody>
</table>## Tool permissions

This section lists the steps required to resolve tool permission errors when you create a DevOps tool using workspace playbooks. Tool permission check guidelines are displayed in a pop-up when you connect to a tool from the workspace.

-   **Action**

    If any permission is missing, perform the following steps:

    -   Update the permissions for the provided credentials in the external DevOps tool. Select **Refresh** in the pop-up to perform the checks again.
    -   Close the pop-up, use different credentials, and select **Connect** again. The permission check pop-up appears with results of the newly entered credentials.
    -   Review the impact column, and if the impact does not affect your use-case, select **Continue** anyway.
    If all permission checks are successful:

    -   Select **Continue** to progress to the next step in the playbook.
    -   If errors show up in the result, try again by selecting **Refresh**.
    -   If the error persists, update the [Tool permission check timeout per record \(in milliseconds\)](devops-reference-error-messages.md#toolchecktimeoutproperty) property and try again.
-   **Tool permission check timeout property**

    During the tool connection process, the system performs permission validations in the foreground, and restricts the tool connection page. For every permission validation, a REST API call is made to external tools to evaluate the availability of the permission. The REST API response time may vary based on your network settings. To avoid delays, you can specify how long the system should wait to get a response from an external tool before marking the permission as an error. You can specify this time using the **Tool permission check timeout per record \(in milliseconds\)** property **\(sn\_devops.permission\_check\_timeout\)**. If you find that some of the permission checks are resulting in an error, try increasing the timeout value, and select **Refresh** in the Permissions pop-up.


## Tool notification

This table lists the steps required to resolve errors that might occur in scenarios such as retrieving commit details, pipeline execution details, pull request details, test summaries:

<table id="table_xns_nzc_2xb"><thead><tr><th>

Reason

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Authorization credentials are either invalid or do not have the minimum required permissions.

</td><td>

-   Verify if your third-party tool credentials have the required scopes. If you are using the workspace UI, you can navigate to the tool record, and select **More actions \(![More actions icon](../../itsm-workspace/image/more-actions-icon.png)\) &gt; Check credential permissions** to know about the required permissions.
-   Verify if you have entered the correct username/password for your third-party tool. If you are using the workspace UI, and you want to update your tool credentials, then navigate to the tool record, and select **More actions \(![More actions icon](../../itsm-workspace/image/more-actions-icon.png)\) &gt; Check credential permissions**. For more information on updating credentials, see [Update third-party tool credentials in DevOps Change Velocity](../task/update-third-party-tool-credentials-in-devops-change-velocity.md).

</td></tr><tr><td>

There is no response from the server. Check the server connection status, and try again.

</td><td>

-   Verify that the DevOps tool server is reachable and responsive.
-   If MID server is configured, verify if the server is up and running.

</td></tr><tr><td>

Unable to process the request.

</td><td>

Verify if the maximum number of instances associated with a webhook has exceeded. If you encountered this error for GitHub, verify if you have associated more than 20 instances to a webhook.

</td></tr><tr><td>

Authorization credentials do not have the minimum required permissions.

</td><td>

Verify if your third-party tool credentials have the required scopes. If you are using the workspace UI, you can navigate to the tool record, and select **More actions \(![More actions icon](../../itsm-workspace/image/more-actions-icon.png)\) &gt; Check credential permissions** to know about the required permissions.

</td></tr><tr><td>

MID server configuration is invalid. Configure a valid MID server, and try again.

</td><td>

Check if the mid server is running and reachable.

</td></tr><tr><td>

The connection URL is invalid. Enter a valid URL, and try again.

</td><td>

1.  Navigate to **All &gt; Connections &amp; Credentials &gt; Connection &amp; Credential Aliases** and open the required connection &amp; credential record.
2.  From the Connections related list, open the related **Connection** form.
3.  On the **Connection** form, verify if the connection URL of the third-party tool is correct.

</td></tr><tr><td>

The rate limit has been exceeded. Retry after \{0\}.

</td><td>

Rate limit is the number of API calls an app or user can make within a given time period. Rate limiting is a technique to limit network traffic to help prevent users from exhausting system resources. If the max rate limit allowed in your third-party tool has exceeded, you might encounter this error.

</td></tr><tr><td>

Your credentials does not have the required scopes.

</td><td>

Verify if your third-party tool credentials have the required scopes. If you are using the workspace UI, you can navigate to the tool record, and select **More actions \(![More actions icon](../../itsm-workspace/image/more-actions-icon.png)\) &gt; Check credential permissions** to know about the required permissions.

</td></tr></tbody>
</table>## Change request

This table lists the steps required to resolve errors that might occur during change request creation:

<table id="table_bwy_lhx_dyb"><thead><tr><th>

Error

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Change request cannot be created because the type compatibility flag is disabled. Enable the type compatibility flag in system properties or configure the change model in the step record in ServiceNow or enter the appropriate change model sys id in the pipeline.

</td><td>

-   Navigate to **All &gt; System Properties**, and enable the **com.snc.change\_management.change\_model.type\_compatibility** property, or
-   Add the change model in the Step form or change attributes of the pipeline.

</td></tr><tr><td>

Change request cannot be created because either the change type or change model is not configured for the pipeline.

</td><td>

Add the change model or type in the Step form or change attributes of the pipeline.

</td></tr></tbody>
</table>## General errors

This table lists steps required to resolve few general errors that might occur while working with the DevOps Change Velocity application.

<table id="table_hrq_pvx_vgb"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Import request not progressing

</td><td>

If an import request remains in the Requested state for too long while performing an import for a tool \(such as Jenkins, Jira, or GitHub \), delete the import request and try again.

 **Note:** Delete the existing request to retry importing the same range.

</td></tr><tr><td>

Tool connection fails

</td><td>

Remove the trailing slash \(‘/’\) in the **Connection URL** field on the HTTP Connection form.

</td></tr><tr><td>

No change request is created for a Jenkins job under change control

</td><td>

Verify that:-   The tool integration in your instance is set up properly.
-   The task has been synced in your instance.
-   Tasks and app steps have been configured in your instance.

 Change request creation is not supported if the task is under change control:

-   Is not part of a pipeline \(is a standalone task, for example\).
-   Is the first in the pipeline.
-   Is within the pipeline, but the user manually triggers, or does SCM checkout directly on the task under change control \(thus not triggering the pipeline from the beginning\).

</td></tr><tr><td>

Jenkins does not block the job under change control \(does not wait for change request approval\)

</td><td>

Verify that the Jenkins location is configured:

 Navigate to **Jenkins** &gt; **Manage Jenkins** &gt; **Configure System** and provide the hostname for the **Jenkins URL** field in the Jenkins Location section.

 **Note:** To avoid caching issues, click **Save** even if the **Jenkins URL** field already contains a value when you first open the form.

</td></tr><tr><td>

Events occurring in the payload log with state Not Connected

</td><td>

If any of the following changes for a connection made manually \(using manual configuration mode\), the connection is automatically disconnected.

-   Alias associated with the tool
-   Type of tool
-   New active HTTP connection for the same domain added to the alias
-   Existing HTTP connection for the same domain activated
-   Connection URL of the HTTP connection
-   Credentials of the HTTP connection
-   Use MID Server setting in the HTTP connection

 Enter manual configuration mode and reconnect.

</td></tr><tr><td>

Retry Inbound events that fail or error out due to REST API TimeoutException/FlowObjectAPIException

</td><td>

Update the **Retry Errored Inbound Events** scheduled job to retry processing inbound events that are in **Error** state.

-   Update the errors or exceptions list to specify exceptions that you want to retry event processing for.
-   Modify the default **Maximum Retry** count.

For more information, see [Retry errored inbound events](../task/config-retry-schedule-job-inbound.md)

</td></tr><tr><td>

Pipeline execution in ServiceNow DevOps does not move forward and waits indefinitely as the SonarQube scans do not take place due to the absence of SonarQube tool.

 The software quality inbound event displays the following error message in the processing details field. "Check if the respective SonarQube tool is created successfully. If not, create the SonarQube tool and retry the inbound event."

</td><td>

For all SonarQube steps in code quality scans, the user must create SonarQube tool in the ServiceNow DevOps instance.

 For more information, see [SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md)

</td></tr><tr><td>

Pipeline UI displays broken links between stages.

</td><td>

Navigate to **Task Executions** and ensure that the Upstream executions column has the appropriate upstream link references.

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Change Velocity reference](devops-change-velocity-reference.md)

