---
title: DevOps Change Velocity properties
description: Use these properties to configure settings in the DevOps Change Velocity application.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps Change Velocity properties

Use these properties to configure settings in the DevOps Change Velocity application.

Role required: sn\_devops.admin

You can view the properties from the DevOps Change workspace by navigating to **System configuration** &gt; **Properties**.

To view the properties from the Classic UI, navigate to **All** &gt; **DevOps** &gt; **Administration** &gt; **Properties**.

<table id="table_l4c_ndl_xgb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default

</th><th>

Name

</th></tr></thead><tbody><tr><td>

Maximum retries for errored inbound events

</td><td>

Maximum number of retries for errored inbound events.

</td><td>

3

</td><td>

\[sn\_devops.max\_retry\_count\_inbound\_event\]

</td></tr><tr><td>

Tool capabilities

</td><td>

The tool capabilities supported, entered as comma-separated values.

</td><td>

code,plan,orchestration,artifact,test

</td><td>

\[sn\_devops.tool\_capabilities\]

</td></tr><tr><td>

DevOps change request approval text

</td><td>

The DevOps change request approval text to be used for change management customizations.

</td><td>

Approved

</td><td>

\[sn\_devops.change\_request.approved\_approval\]

</td></tr><tr><td>

DevOps change request - Apply attributes on change creation

</td><td>

If enabled, change attributes are applied when a change is created. If there are any data policies applied on the change attributes, they are enforced when the change is created. If this property is not enabled, change attributes are applied after the change is created, which may cause change creation failure if any data policies are present on the change attributes.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.change\_request.apply\_attributes\_on\_creation\]

</td></tr><tr><td>

Duration of DevOps system health report \(in days\)

</td><td>

Defaults to the last 7 days, to show system health metrics like inbound events.

</td><td>

7

</td><td>

\[sn\_devops.health\_duration\_report\]

</td></tr><tr><td>

Enable automatic association of repos to apps on pipeline execution

</td><td>

If enabled, automatically associates repositories to apps and enables track when a pipeline identifies commits of a repository that is not yet associated. Also associates pipelines that are not yet associated to the corresponding app when the repository is already assigned to the app.

</td><td>

Yes \(enabled\)

</td><td>

\[sn\_devops.enable\_automatic\_associations\]

</td></tr><tr><td>

Maximum number of pages to process at a time for an import request

</td><td>

The maximum number of pages that must be processed at a time for an import request.

</td><td>

10

</td><td>

\[sn\_devops.import.max.pages.processing.per\_import\]

</td></tr><tr><td>

DevOps change request reusability decision subflow

</td><td>

The subflow that can be called to check if a previously created change can be reused, instead of creating a new one.

</td><td>

sn\_devops.change\_request\_reusability\_subflow

</td><td>

\[sn\_devops.change\_request\_reusability\_decision\]

</td></tr><tr><td>

GitHub URL

</td><td>

For GitHub, this field is used to get the API URL \(for REST calls\).

</td><td>

https://github.com

</td><td>

\[sn\_devops.github.url\]

</td></tr><tr><td>

DevOps change request cancel state

</td><td>

DevOps change request cancel state to be used for change management customizations.

</td><td>

4 \(Canceled\)

</td><td>

\[sn\_devops.change\_request.cancel\_state\]

</td></tr><tr><td>

Maximum orchestration tool executions while importing

</td><td>

Maximum orchestration tool executions while importing Jenkins freestyle jobs.

</td><td>

1000

</td><td>

\[sn\_devops.import.orchestration\_tool.executions.maximum\]

</td></tr><tr><td>

To save payloads as attachments on the Import Request Page record, set the "Value" field to "true". Anything else is considered as false.

</td><td>

If true, the fetched JSON payload is saved as an attachment in the Import Request page.To save payloads as attachments on the Import Request Page record, set the **Value** field to true. Anything else is considered false.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.import.save.payloads.as.attachments\]

</td></tr><tr><td>

DevOps non-admin software quality summary flag

</td><td>

Enable to view and monitor SonarQube scans configured on your GitHub Actions, Jenkins, or Azure DevOps pipelines as a non-admin SonarQube user.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.non\_admin\_software\_quality\_summary\_flag\]

</td></tr><tr><td>

Default test type

</td><td>

Default test type from orchestration pipelines.

</td><td>

JUnit

</td><td>

\[sn\_devops.default\_test\_type\]

</td></tr><tr><td>

Coding tool branches per page

</td><td>

Number of coding tool branches per page.

</td><td>

19

</td><td>

\[sn\_devops.import.coding\_tool.branches.per\_page\]

</td></tr><tr><td>

Planning tool issues per page

</td><td>

Number of planning tool issues displayed per page.

</td><td>

100

</td><td>

\[sn\_devops.import.planning\_tool.issues.per\_page\]

</td></tr><tr><td>

sn\_devops role to be automatically added to active DevOps users

</td><td>

The sn\_devops role entered in the value field is automatically added to users who are active DevOps users \(for example, making a commit\). If a role that is not in the sn\_devops scope is provided, it is not added.

 Leave empty if no role should be automatically provided.

</td><td>

sn\_devops.viewer

</td><td>

\[sn\_devops.discovered.user.auto.assign.role\]

</td></tr><tr><td>

Software quality categories shown by default in the Pipeline UI view

</td><td>

The software quality categories shown by default in the Pipeline UI view, entered as comma-separated values.

</td><td>

coverage,lines\_of\_code,bugs,code\_smells,duplications,vulnerabilities

</td><td>

\[sn\_devops.sq\_ui\_category\_preferences\]

</td></tr><tr><td>

Errors or exceptions \(comma separated\) for which errorred inbound events are set to Retry

</td><td>

Errors or exceptions for which the errored inbound events are set to Retry. Entered as comma-separated values.

</td><td>

TimeOutException,FlowObjectAPIException

</td><td>

\[sn\_devops.inbound\_events\_retry\_error\_list\]

</td></tr><tr><td>

DevOps log level

</td><td>

The DevOps log level. Select the appropriate level from the following:

-   Error
-   Warning
-   Information
-   Debug
-   Trace

</td><td>

Warning

</td><td>

sn\_devops.devops\_log\_level

</td></tr><tr><td>

Categorize DevOps change requests on **DevOps Change** field

</td><td>

.Select this option to categorize change requests with category field set to DevOps as a DevOps change.

Clear to disable.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.custom\_change\_categorization\]

</td></tr><tr><td>

Orchestration tool executions per page

</td><td>

Number of orchestration tool executions per page.

</td><td>

50

</td><td>

\[sn\_devops.import.orchestration\_tool.executions.per\_page\]

</td></tr><tr><td>

Enable import polling

</td><td>

Option to enable polling of import requests. Clear to disable polling.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.enable\_import\_polling\]

</td></tr><tr><td>

GitHub API version path

</td><td>

The GitHub API version path.

</td><td>

/api/v3

</td><td>

\[sn\_devops.github.api\_version\_path\]

</td></tr><tr><td>

Tool permission check timeout per record \(in milliseconds\)

</td><td>

During the tool connection process, the system performs permission validations in the foreground, and restricts the tool connection page. For every permission validation, a REST API call is made to external tools to evaluate the availability of the permission. The REST API response time may vary based on your network settings. To avoid delays, you can specify how long the system should wait to get a response from an external tool before marking the permission as an error through this property.

</td><td>

10000

</td><td>

\[sn\_devops.permission\_check\_timeout\]

</td></tr><tr><td>

DevOps change request reusability model subflow

</td><td>

The DevOps change request reusability model subflow.

</td><td>

sn\_devops.devops\_reused\_model\_change\_request

</td><td>

\[sn\_devops.devops\_reused\_model\_change\_request\]

</td></tr><tr><td>

Time elapsed \(in minutes\)

</td><td>

The time elapsed in minutes. The retry job checks for errored inbound events from the time/value specified.

</td><td>

1440 \(7 days\)

</td><td>

\[sn\_devops.inbound\_events\_error\_retry\_mins\_ago\]

</td></tr><tr><td>

Cancel the change request when the associated stage in the pipeline fails or is canceled

</td><td>

When this property is enabled and the orchestration task mapped to a certain step in your DevOps pipeline fails or is canceled, the change request associated with that step is also canceled. A change request can be canceled only if it has not already been rejected or is not in the implement or review state at the time of cancellation.

</td><td>

False \(disabled\)

</td><td>

\[sn\_devops.cancel\_change\_on\_pipeline\_cancel\]

</td></tr><tr><td>

Cascade delete threshold \(recommended foreground limit 1000\)

</td><td>

Cascade delete threshold.

</td><td>

1000

</td><td>

\[sn\_devops.cascade\_delete\_threshold\]

</td></tr><tr><td>

Maximum retries per page while importing

</td><td>

Maximum retries allowed per page while importing data from tools.

</td><td>

3

</td><td>

\[sn\_devops.import.max.retries.per\_page\]

</td></tr><tr><td>

DevOps change request post implement state

</td><td>

DevOps change request post implement state to be used for change management customizations.

</td><td>

0 \(Review\)

</td><td>

\[sn\_devops.change\_request.post\_implement\_state\]

</td></tr><tr><td>

DevOps change request implement state

</td><td>

DevOps change request implement state to be used for change management customizations.

</td><td>

-1 \(Implement\)

</td><td>

\[sn\_devops.change\_request.implement\_state\]

</td></tr><tr><td>

Default committer score

</td><td>

The default committer score.

</td><td>

50

</td><td>

\[sn\_devops.committer.score.default\]

</td></tr><tr><td>

Enable to track GitLab pull \(merge\) requests. If not enabled, then pull \(merge\) requests and related events will be ignored.

</td><td>

When this property is enabled, GitLab pull \(merge\) requests are tracked in DevOps Change Velocity. If disabled, then all merge request events are ignored.

</td><td>

Yes \(enabled\)

</td><td>

sn\_devops.track.gitlab.pullrequests

</td></tr><tr><td>

Default throttle reset time in minutes from current time

</td><td>

If a tool doesn't support a throttle reset time, the throttle reset time will be considered as the current time plus the value given for this property.

</td><td>

15 minutes

</td><td>

\[sn\_devops.throttle.reset.time.default\]

</td></tr><tr><td>

Enable to track Azure DevOps Code Pull-Requests. If this is enabled then azure pull request web-hooks will be auto-configured when tool or project is configured.

</td><td>

When this property is enabled, the Azure DevOps pull request web-hooks are auto-configured whenever a tool or project is configured.

</td><td>

Yes \(enabled\)

</td><td>

sn\_devops.track.azure.pullrequests

</td></tr><tr><td>

Multiply factor for committer score

</td><td>

The multiplication factor to be used for committer score.

</td><td>

1

</td><td>

\[sn\_devops.committer.score.multiply.factor\]

</td></tr><tr><td>

Auto archive \(in months\)

</td><td>

The duration after which the table data is to be auto-archived.

</td><td>

9

</td><td>

\[sn\_devops.table\_auto\_archive\_duration\]

</td></tr><tr><td>

Deprecated - Enable debug flag \(Use new property DevOps log level\)

</td><td>

DevOps Debug Logger.

**Note:** This property is deprecated, use the **sn\_devops.devops\_log\_level** \(DevOps log level\) property instead.

</td><td>

Yes \(enabled\)

</td><td>

\[sn\_devops.enable\_debug\]

</td></tr><tr><td>

Maximum processing time per page while importing \(in seconds\)

</td><td>

Maximum processing time in seconds, that should be allowed per page while importing data from tools.

</td><td>

300

</td><td>

\[sn\_devops.import.max.processing.time.seconds.per\_page\]

</td></tr><tr><td>

Supported webhook capabilities

</td><td>

Webhook capabilities supported by DevOps Change Velocity.

</td><td>

code,plan,orchestration,artifact, test

</td><td>

\[sn\_devops.supported\_webhook\_capabilities\]

</td></tr><tr><td>

DevOps change request closed state

</td><td>

DevOps change request closed state to be used for change management customizations.

</td><td>

3

</td><td>

\[sn\_devops.change\_request.closed\_state\]

</td></tr><tr><td>

Bulk flow timeout \(in milliseconds\)

</td><td>

Bulk flow timeout in milliseconds.

</td><td>

60000

</td><td>

\[sn\_devops.bulk\_flow\_timeout\]

</td></tr><tr><td>

GitHub/Bitbucket coding tool commits per page

</td><td>

Number of coding tool commits per page for GitHub and Bitbucket.

</td><td>

100

</td><td>

\[sn\_devops.import.coding\_tool.commits.per\_page\]

</td></tr><tr><td>

Folder depth

</td><td>

Retrieves only those orchestration tasks and pipelines which are in folders whose nesting level is less than or equal to the number specified here. Folder Depth is the level of nesting done on folders in Jenkins, which contains the orchestration task and pipelines that you want to discover. For example, if you want to discover orchestration tasks and pipelines for a folder structure that is nested 2 times in your Jenkins environment, you must enter 2 as the value for this property.

</td><td>

3

</td><td>

\[sn\_devops.discover.jenkins.folder.depth\]

</td></tr><tr><td>

DevOps change request handler subflow

</td><td>

If you are using a custom subflow instead of the Default Change Handler subflow in Flow Designer \(which is used to populate the change request fields with default values\), then you must update this property value to the new subflow. You can copy the Default Change Handler subflow in Flow Designer and update it according to your organization's needs. For information on the Default Change Handler subflow, see [Customizing DevOps flows](using-dev-ops-model-change-flow.md).For information on copying a subflow, see [Copy a subflow](https://www.servicenow.com/docs/access?context=copy-subflow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td><td>

sn\_devops.default\_change\_handler\_subflow

</td><td>

\[sn\_devops.change\_request\_handler\_subflow\]

</td></tr><tr><td>

Coding tool repositories per page

</td><td>

The number of repositories that must be displayed per page when you import repositories after connecting to a tool. The total number of repositories imported is not dependent on this property, but the number of repositories that must be displayed per page from the total number of repositories imported can be specified using this property. For example, if your tool contains 1000 repositories and you specify 100 as the property value, 1000 repositories will be imported of which 100 will be displayed per page in the Import Requests page.

 When you discover repositories, the number of repositories that must be retrieved per API call in the backend is also dependent on this property value. For a large number of repositories, set a relatively smaller value in this property so that lesser number of repositories are retrieved per call and the system does not time out.

</td><td>

100

</td><td>

\[sn\_devops.import.coding\_tool.repos.per\_page\]

</td></tr><tr><td>

GitHub API URL

</td><td>

GitHub API URL.

</td><td>

https://api.github.com

</td><td>

\[sn\_devops.github.api\_url\]

</td></tr><tr><td>

ITBM Agile planning tool issues import max limit

</td><td>

Strategic Portfolio Management \(SPM\) Agile planning tool issues import max limit.

</td><td>

1000

</td><td>

\[sn\_devops.import.planning\_tool.itbm.issues.max.limit\]

</td></tr><tr><td>

Assign a universal task and notify to update tool credentials when expired

</td><td>

Admins and tool owners will be notified \(through universal task, email, banner, and field message\) on expiry of tool credentials after the credentials have expired. As an admin or tool owner, you can update your tool credentials and connect the tool to prevent any further loss of data. For information on updating tool credentials, see [Update third-party tool credentials in DevOps Change Velocity](../task/update-third-party-tool-credentials-in-devops-change-velocity.md).

</td><td>

Yes \(enabled\)

</td><td>

\[sn\_devops.credential\_expiration.notify\_on\_expiration\]

</td></tr><tr><td>

Number of days before tool credential expiry to assign a universal task and notify \(if applicable\)

</td><td>

Set the number of days before tool credentials expiry to send notifications \(through universal task, email, banner, and field message\) to admins for GitHub tools created with basic authentication. To stop sending proactive notifications, select 0 as the value for this property. For information on updating tool credentials, see [Update third-party tool credentials in DevOps Change Velocity](../task/update-third-party-tool-credentials-in-devops-change-velocity.md).

</td><td>

3

</td><td>

\[sn\_devops.credential\_expiration.notify\_before\_days\]

</td></tr><tr><td>

Number of days to display warning alerts when events were not being received

</td><td>

Set the number of days to display warning alerts in the **Last event received** field in the tool record when events were not being received. This only applies for tools which sends data to ServiceNow. The **Last event received** field in the tool record header and inside the tool record will be highlighted in yellow for warning alerts when the events were not being received.

</td><td>

2

</td><td>

\[sn\_devops.last\_event\_received.warning\]

</td></tr><tr><td>

Number of days to display critical alerts when events were not being received

</td><td>

Set the number of days to display critical alerts in the Last event received field in the tool record when events were not being received. This only applies for tools which sends data to ServiceNow. The **Last event received** field in the tool record header and inside the tool record will be highlighted in red for critical alerts when the events were not being received.

</td><td>

7

</td><td>

\[sn\_devops.last\_event\_received.critical\]

</td></tr><tr><td>

Enable whether Azure DevOps Run Commits must be determined from the last successful pipeline build

</td><td>

If enabled, DevOps Change will pick up the last commits, upto a maximum of 2000, created after the last successful pipeline build from Azure DevOps as part of Run Commits.

 If disabled, only the last 200 commits will be considered for Run Commits.

</td><td>

No

</td><td>

\[sn\_devops.enable\_ado\_bulk\_run\_commits\]

</td></tr><tr><td>

Enable whether GitHub Run Commits must be determined from the last successful workflow run

</td><td>

If enabled, DevOps Change will pick up the first 2000 commits after the last successful workflow run in GitHub as part of Run Commits.

**Note:** Skipped commits are not considered.

 If disabled, only the last commit will be picked up for Run Commits.

</td><td>

No

</td><td>

\[sn\_devops.enable\_github\_run\_commits\]

</td></tr><tr><td>

This property decides whether to create a Generic Connection on configure operation for Azure DevOps

</td><td>

The step to enter the integration user name and password is required to configure webhooks when this property is enabled.

</td><td>

No

</td><td>

\[sn\_devops.enable\_ado\_generic\_connection\]

</td></tr><tr><td>

Maximum limit for the number of pipelines that can be discovered for an Azure DevOps project

</td><td>

Set the maximum number of pipelines that can be discovered in an import request for an ADO project. If your project has more than 15000 pipelines, then you can try setting this property value to that number and see if the pipelines get discovered. If not, you can reduce the value to a lower number and try to discover.

</td><td>

15000

</td><td>

\[sn\_devops.discover.max.pipelines.ado\]

</td></tr><tr><td>

Update DevOps Change Request States Automatically when Change Receipt is Enabled

</td><td>

Updates the DevOps change request states automatically when change receipt is enabled. If you want to stop the automatic transition of the change request states even when change receipt is turned on, you must disable this property.

</td><td>

Selected \(enabled\)

</td><td>

\[sn\_devops.enable\_change\_receipt\_state\_transition\]

</td></tr><tr><td>

Switch to this user after token based authentication is successful

</td><td>

If the devops.system user is not available in your ServiceNow instance, use this property to set any other user that has the sn\_devops.integration role, which is needed to complete the token authentication.

</td><td>

devops.system

</td><td>

\[sn\_devops.token\_auth.user\]

</td></tr><tr><td>

Maximum limit for the number of times the discover action that exceeds the rate limit will be retried.

</td><td>

Determines the maximum number of times the discover action will be automatically retried after it reaches the rate limit. For example, if the rate interval in Azure DevOps is 5 mins, and you enter a value of 4 here, then after every 5min, the discover action will be retried for 4 times.

</td><td>

10

</td><td>

\[sn\_devops.max\_retry\_count\_discover\]

</td></tr><tr><td>

Enable change request creation even with errors in DevOps data retrieval

</td><td>

If enabled, when an error occurs in retrieving DevOps data like work items, commits, test summaries, security summaries, etc, the corresponding change request is still created. The data that can be retrieved will still be associated with the change request. For the data that cannot be retrieved, the reason for the error will be notified to the user in the third-party console, and the same information will also be added in the **Change Comments** field in the Step Execution record and the change **Worknotes**.

</td><td>

No \(disabled\)

</td><td>

\[sn\_devops.enable\_change\_creation\_with\_partial\_data\]

</td></tr><tr><td>

Enable state transition from New to Assess when DevOps Change Request Manual Approval Flow is active

</td><td>

If enabled, updates the change request state from New to Assess directly when the DevOps Change Request Manual Approval Flow is active. If you want to stop the automatic transition of the change request state to Assess when the DevOps Change Request Manual Approval Flow is active, you must disable this property.

</td><td>

Yes \(enabled\)

</td><td>

\[sn\_devops.enable\_change\_request\_state\_transition\]

</td></tr><tr><td>

Change request callback timeout \(in minutes\)

</td><td>

Set the timeout value in minutes until which the system will try to process a change when an inbound event goes into the waiting state during a pipeline run. After that the pipeline will be aborted. The reason for the error is displayed in your third-party tool's console logs. When a pipeline is cancelled because of callback timeout, the same information is added in the callback record of the corresponding step execution.

</td><td>

120 minutes

</td><td>

\[sn\_devops.change\_request\_callback\_timeout\]

</td></tr><tr><td>

Default Bitbucket branch used for import request

</td><td>

Specify the default Bitbucket branch name that must be used to create an import request.

</td><td>

master

</td><td>

\[sn\_devops.bitbucket\_default\_branch\]

</td></tr><tr><td>

Close code value for a change request completed successfully when the autoCloseChange parameter is enabled.

</td><td>

Enter the close code value for a change request completed successfully when the autoCloseChange parameter is enabled.

</td><td>

successful

</td><td>

sn\_devops.change\_request.auto\_close\_successful\_code

</td></tr><tr><td>

Close code value for a change request completed with issues when the autoCloseChange parameter is enabled.

</td><td>

Enter the close code value for a change request completed with issues when the autoCloseChange parameter is enabled.

</td><td>

successful\_issues

</td><td>

sn\_devops.change\_request.auto\_close\_partial\_successful\_code

</td></tr><tr><td>

Close code value for a change request completed unsuccessfully when the autoCloseChange parameter is enabled.

</td><td>

Enter the close code value for a change request completed unsuccessfully when the autoCloseChange parameter is enabled.

</td><td>

unsuccessful

</td><td>

sn\_devops.change\_request.auto\_close\_failure\_code

</td></tr><tr><td>

Import based evidence collection for orchestration capability

</td><td>

This property modifies how pipeline events are processed. When switched on, the setting reduces instance overhead by skipping step-level processing in the pipeline. The skipped step-level events will be ignored with the processing details, "IGNORED: This event is ignored because the 'Import based evidence collection for orchestration capability' property is enabled". Conversely, switching off reverts to the standard mode, where all inbound events undergo processing.

</td><td>

False \(disabled\)

</td><td>

sn\_devops.import\_based\_evidence\_collection

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Change Velocity reference](../reference/devops-change-velocity-reference.md)

