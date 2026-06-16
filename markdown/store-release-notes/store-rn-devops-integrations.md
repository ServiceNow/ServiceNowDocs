---
title: DevOps Integrations release notes
description: Version history for the DevOps Integrations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-integrations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 38
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Integrations release notes

Version history for the DevOps Integrations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.0.0 - June 2026**
    -   Changed:
        -   Jira authentication with 3LO
            -   Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.
        -   Bitbucket Cloud basic authentication using API token with scopes
            -   Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.
-   **Version 6.3.1 - March 2026**
    -   Changed:
        -   Enhanced JFrog integration with DevOps Change Velocity
            -   Gather JFrog evidence seamlessly and create change records automatically using the improved integration with DevOps Change Velocity.
        -   Bearer authentication in JFrog
            -   Connect to JFrog using the more secure bearer token authentication to comply with updated security policies.
        -   HTTP proxy for Docker
            -   Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment.
        -   Auto close without Change Management - State Model \[Legacy\] plugin
            -   Change requests can now be auto-closed without requiring installation of the Change Management - State Model \[Legacy\] plugin.
-   **Version 6.2.0 - December 2025**
    -   New:
        -   Import-based evidence collection for GitLab and Jenkins
            -   Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitLab and Jenkins orchestration tools.
    -   Changed:
        -   Prod Deploy commit logic for other step types
            -   Update the Controls whether other Step types should follow the same logic as Prod Deploy to determine commits for a Change \[sn\_devops.commit\_rel\_change\_step\_type\] property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.
        -   Override start and end time of a change request
            -   Set the sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time and sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time properties as false to consider the change request start and end time instead of the pipeline’s when the autoCloseChange parameter is enabled in a pipeline.
        -   Node version of DevOps extension
            -   The node version of the ServiceNow DevOps extension has been upgraded to version 20.x in Azure DevOps.
        -   Improved pipeline governance in GitLab
            -   View change request details like status, sys\_id, priority, and so on in the GitLab console when a change request is created in GitLab using Docker image.
-   **Version 6.1.0 - August 2025**
    -   New:
        -   Import based evidence collection framework
        -   Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub and Azure DevOps \(ADO\) orchestration tools.
-   **Version 6.0.1 - May 2025**
    -   New:
        -   Bitbucket cloud tool integration with ServiceNow
            -   Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity, enabling ServiceNow to connect, discover, import, and process real-time repository events.
        -   DevOps Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities
            -   An intuitive DevOps Workspace UI to integrate a new custom tool across capabilities with basic know how of ServiceNow has been added. It offers easy navigation to the ServiceNow AI Platform for defining transformer or adapter rules or integrate the ability to do so within the workspace wherever applicable and embeds necessary documentation links and tooltips to bolster self-service.
    -   Changed:
        -   Additional scans for DevOps Health Scan Content pack
            -   Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with catching configuration issues like plugin and version incompatibilities or pipelines that chronically fail have been added.
        -   Bitbucket Server and Data Center tool integration with ServiceNow
            -   Improved support for Bitbucket Server and Data Center by enabling Pull Request functionality.
        -   Secure token for Rally Integration User
            -   Rally integration now supports a more secure integration user token, instead of basic auth for integration user, and is now consistent with the remaining planning tool integrations.
-   **Version 5.1.0 - February 2025**
    -   New:
        -   Harness tool integration with ServiceNow
            -   Integrate the Harness orchestration tool with DevOps Change Velocity. This integration enables you to connect, discover, import, process real-time events, and integrate CI/CD with change in ServiceNow for Harness pipelines.
    -   Changed:
        -   Simplified onboarding of orchestration tools that are not supported in the base system
            -   The simplified generic framework provides you an easy-to-use solution to integrate custom orchestration tools with ServiceNow DevOps Change Velocity, requiring minimal knowledge of the platform. It reduces the complexity of integration by lowering the amount of custom coding needed and by simplifying the overall process for both customers and partners. By streamlining the onboarding of new orchestration tools, the framework enables faster adoption, smoother scaling, and easier onboarding of additional teams. This enables you to experience fewer integration challenges, speeding up the user adoption process and reducing friction during the transition. This generic framework supports the integration of any orchestration tool not natively supported by ServiceNow in the base system.
        -   Custom fields for planning tool integration
            -   Bring in additional custom fields for work items and thereby experience enhanced configurability of planning tools supported in the base system by DevOps Change Velocity.
        -   Enhanced lead time calculation
            -   Lead time calculation now considers Artifacts/Packages registered as part of Pipeline Execution and is calculated based on commits associated with it.
-   **Version 5.0.0 - November 2024**
    -   New:
        -   OAuth 2.0 authentication for Azure DevOps \(ADO\)
            -   Use OAuth 2.0 authentication to connect your Azure DevOps tool with DevOps Change Velocity ensuring a more secure authentication method.
        -   OAuth 2.0 authentication for Jira Cloud
            -   Use OAuth 2.0 authentication to connect your Jira Cloud tool with DevOps Change Velocity ensuring a more secure authentication method.
    -   Changed:
        -   Generalized Docker container solution to support any orchestration tool
            -   Use the generalized and extensible Docker container solution to integrate any orchestration tool with DevOps Change Velocity for invoking pipeline actions like change request creation and collecting relevant DevOps data without having to rely on tool-specific plugins or extensions.
        -   Simplified onboarding of Planning tools that are not supported in the base system
            -   Integrate planning tools that are not supported in the base system by using transformer rules. GitLab Issues is now available as one of the planning tools and is built leveraging this new approach, so you can discover plans, import work items, and configure webhooks for work items \(issues\) in GitLab.
        -   Improved manual DevOps change creation experience by enabling the association of work items directly
            -   Add work items data in a manually created DevOps change request in  Service Operations Workspace  for  ITSM.
-   **Version 4.1.0 - August 2024**
    -   Improved DevOps Integrations to support the following DevOps Change Velocity features:
        -   Changed:
            -   Improved journey to full change automation using models.
            -   Support reruns with GitHub Action.
            -   Support API\_KEY for Jira Server.
            -   Persist branch details in pipeline execution to determine commits from artifacts and packages.
        -   Removed:
            -   To make the Change - DevOps Implement flow of the DevOps model more suitable for DevOps changes, change tasks are no longer automatically created.
            -   The DevOps Change Request Minimal Automation Approval Flow and DevOps Change Request Advanced Automation Approval flows won't trigger for DevOps change requests whose model is a base system DevOps change model \(DevOpsorDevOpssimplified\) to avoid conflicts and errors.
        -   Note: For detailed information on the features, see the DevOps Change Velocity Release Notes.
-   **Version 4.0.0 - May 2024**
    -   New:
        -   Custom orchestration tool integration support
            -   Integrate DevOps Change Velocity with any orchestration tool that is not supported inthe base system.
        -   Improved onboarding error handling and guardrails
            -   View improved error messages which helps you find the root cause of a problem whileonboarding \(connection, discover, configure, or import\) a tool.
        -   Change request creation with errors in DevOps data retrieval
            -   Enable change request creation even if there is an error in retrieving the DevOps datain a pipeline.
        -   GitLab merge request / pull request support
            -   Manage GitLab pipelines pull requests for GitLab coding source from ServiceNow DevOps.
        -   JFrog Artifactory support for GitHub Actions, Azure DevOps, and GitLab
            -   Import the artifact data published to JFrog Artifactory for GitHub Actions, Azure DevOps, and GitLab pipeline executions.
        -   Multiple ServiceNow DevOps configurations in the same Jenkins instance
            -   Configure multiple ServiceNow DevOps connections in one Jenkins Server.
    -   Changed:
    -   -   Jira Cloud support
    -   Onboard Jira Cloud to DevOps Change Velocity in addition to Jira On-premises.
-   GitLab Docker Container improvements
    -   Retrieve and update change request details associated with a GitLab pipeline and publish unit test results. Automatically updating the close code, based on the overall pipeline execution status for simple GitLab pipelines is also supported.
-   **Version 3.1.0 - February 2024**
    -   New:
        -   GitHub Issues integration
            -   GitHub now supports the Plan capability with GitHub Issues integration in addition to the code and orchestration capabilities. GitHub Issues of the repository can also be discovered and linked with the GitHub commits and persisted in the ServiceNow DevOps CHG, which can be used for policy decisions of ServiceNow DevOps CHG acceleration.
        -   Supported various unit test types for GitHub Actions
            -   Automatically publish test results of various unit test tool reports like NUnit, pytest, jest, JUnit, XUnit without any custom API calls to publish to the ServiceNow DevOps CHG.
        -   Guided change automation experience
            -   Better in-product guidance is now provided on the various ways to leverage DevOps changes and how to easily adopt DevOps changes without complete disruption of your change process. A stepper guides you to automate DevOps change creation. You can check the connection status of a tool while selecting a pipeline on the stepper and you are also alerted before proceeding to the next step. Two new state transition flows: Change - DevOps - New and Change - DevOps Schedule, for DevOps change model are introduced to move and track changes through these states. The DevOpsChangeRelationshipHelper script has been introduced to retrieve data associated with a change request based on the specified relation type.
        -   Handling of Azure DevOps and GitHub API rate limiting
            -   When Azure DevOps or GitHub API rate limits are exceeded, DevOps Change Velocity will defer processing of new events until GitHub throttling has subsided to handle large volumes of data.
        -   Support pagination in Discover import requests for pipelines, repos, plans for Azure DevOps and GitHub
            -   Data is now retrieved from 3rd party tools in batches \(paginated way\). This will help you to scale by onboarding many teams having large volumes of data.
            -   Removal of Connection Admin and Flow Designer roles for DevOps Admin &amp; Tool Owner
                -   Visibility and editing capabilities of DevOps Admins and Tool Owners has been limited by removing the Flow Designer and Connection Admin roles for these users.
        -   Changes to artifacts and packages
            -   The overall experience with adoption, implementation, and error handling for artifacts and packages has been improved. The artifact and package registration API, for both Jenkins and ADO, now provides clear messaging in the response regarding the status. Users can see if the artifact version is already present, staged, or created and can also see the reason in case of a rejection. A clear message is available on the console along with a link to navigate to the artifact page. The DevOpsDPRHelper API now takes pipeline executions as an input to get data on vulnerabilities, test results, and code coverage. The troubleshooting experience has been improved by the addition of a description column that explains why an artifact version or package is pending. A new List module comprising of Artifact, Package, and Pending Packages lists has been created to improve ease of access to this information in the DevOps Change Workspace.
        -   GitLab notification processing improvements
            -   Scalability has been improved with seamless handling of GitLab events. Pre-filtering has been introduced on the inbound events to reduce the number of flow events and API calls. Support for rate limit throttling has been enabled for both Discover and Import flows along with webhook events. GitLab sub flows such as GitLab CI Notification has been re-designed to reduce interference in tracking the waiting state which has optimized the number of REST calls made to retrieve project information.
        -   SonarQube Integration Changes
            -   SonarQube overall quality gate status for the scan summary is now supported and SonarQube integration with GitLab pipelines is also supported using ServiceNow DevOps Gitlab Docker Container.
        -   Removed: Github spoke dependency has been removed.
-   **Version 3.0.0 - November 2023**
    -   New:
        -   Automatic updation of close code based on overall pipeline execution status
            -   The Change created from a pipeline is now automatically closed and updated with the closure notes, actual start/end time based on the overall pipeline completion status. This is controlled by a configuration flag which can be passed in as the attribute in the CHG creation step or via the configuration in the pipeline level in DevOps Change Velocity.
        -   Tool connection and configuration status
            -   For Jenkins, GitHub, and Azure DevOps, the connection and configuration status indicators are updated. You can also easily test the tool connections. Overall Status of the tool is now updated as Connected, Disconnected, Needs Attention, based on the status of Connection Status, Tool Credentials, Permissions Check, Webhook Configuration Status.
        -   GitHub Organization Support
            -   GitHub Organization is now supported with GitHub tool connected via basic auth or GitHub App using Authorization Code, with membership privileges updated accordingly in GitHub tool. And GitHub App using JWT supports one organization per tool, but with multiple tool connections, multiple organizations can be supported.
        -   Supported various unit test types for Azure DevOps \(ADO\)
            -   Automatically publish test results of various test tools reports like NUnit, pytest, jest, JUnit, XUnit without any custom API calls to publish to the DevOps CHG.
        -   Pull Request \(PR\) / Merge Request support for Azure DevOps \(ADO\)
            -   ADO pull request pipeline executions are now tracked in DevOps Change Velocity and the following metadata is published to the CHG, Pull request ID, Commits, Origin branch, Destination branch, Raised by, Approver, Comments, PR raised time, PR approved time, PR merged/closed time.
        -   Handling of GitHub API rate limiting
            -   When GitHub API rate limits are exceeded, DevOps Change Velocity will defer processing of new events until GitHub throttling has subsided. This will increase overall performance for large volumes of data.
        -   Checkmarx support
            -   Connect Checkmarx that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results. This helps you determine how vulnerable your code is. Checkmarx scans that are configured on GitHub Actions, Jenkins, and Azure DevOps pipelines are supported in the base system. You can view the security scan results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance or in the Pipeline UI. You can use security results in defining change policies and conditions for change automation. Both Checkmarx One and Checkmarx SAST are supported.
        -   Multimodel support&gt; &gt;changes
            -   Migrate all your existing pipelines to use models by using the DevOps Pipeline Migration to Change Models catalog. In addition, you can pass the change models by name from your orchestration tool pipelines.
-   **Version 2.0.0 - August 2023**

    New:

    -   New:
        -   Security framework
            -   A new integration framework and data model has been added specifically for application security tools. It is an extensible framework that also allows you to create custom integrations with any application security tools.
        -   Veracode support
            -   Connect Veracode that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results. This helps you determine how vulnerable your code is. Veracode scans that are configured on GitHub Actions, Jenkins, and Azure DevOps pipelines are supported in the base system. You can view the security scan results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance or in the Pipeline UI. You can use security results in defining change policies and conditions for change automation.
        -   Multimodal support
            -   Multimodal change is a new change management feature that allows better flexibility in defining change models or processes to reflect modern development practices. DevOps supports this new feature using which you can create change models with states and rules that determine the transitions between the states to deliver "fit for purpose" change models with a suite of succinct flows and flow actions built in Flow designer. With DevOps change models, change teams can now selectively transition to a wide range of models that are fully optimized for their specific use cases
        -   Secure token authentication for Integration user
            -   Azure DevOps, Jenkins, and GitHub Actions now support token-based authentication for the integration user. Jenkins supports both basic auth and token authentication to make it compatible with DevOps Config.
        -   Run commits for GitHub Actions and Azure DevOps
            -   Increase traceability by capturing the full list of run commits for a change in GitHub Actions and Azure DevOps.
        -   Workspace changes for onboarding and insights
            -   This includes validating the installation of ServiceNow DevOps extension in Azure DevOps before configuring webhooks, automatically importing pipeline steps when going through change automation setup, info icons for DevOps Insights widgets, and better visuals for flow and accelerate metric score widgets for DevOps Insights.
        -   Logging CHG state transitions within orchestration tool and Policy Condition details
            -   Change information such as Change Number, State, Assignment Group, Approvers, Planned Start/End date is displayed in the console logs of Azure DevOps pipelines and GitHub Action workflows, while the pipeline or workflow is pending change approval. The ServiceNow DevOps application is polled at regular intervals and if there is any difference in the change information, it is logged directly in the console logs, thereby minimizing the hops to ServiceNow instance. The details of the Policy Condition, which failed, are also logged in the console of the orchestration tool.
        -   Get and update DevOps Change Request details
            -   Get and update change request details associated with an Azure DevOps pipeline and GitHub Action workflow, by using the ServiceNow DevOps extension from Azure DevOps and GitHub Action marketplace. These extensions or custom actions can be used to get the change, update the change, and close the change as required, by passing in the needed attributes.
        -   GitHub Action Deployment Gates
            -   ServiceNow DevOps Change Velocity now supports GitHub Action Deployment Gates for its environments. By integrating this feature with ServiceNow DevOps, developers can enforce quality gates on every deployment environment in GitHub Actions and get the change details from within the Deployment Protection Rule console logs of GitHub Actions along with the progress of the change states as approved or rejected.
        -   Configure webhooks manually
            -   You can now choose to configure webhooks manually rather than configuring it automatically from ServiceNow DevOps Change Velocity. You can use this feature to access the token and sysid. Using this information, the tool admin within your organization can configure the webhooks manually. It is accessible only for DevOps Admin and Tool owner roles.
        -   ServiceNow DevOps connection and credential
            -   The initial setup of ServiceNow DevOps Change Velocity by ServiceNow Admins has been simplified. The task of setting up the integration user with basic auth credentials is not required anymore. CreateDevOpsTool alias setup has been removed.
        -   Optimal handling of ServiceNow DevOps events to improve performance
            -   ServiceNow DevOps will filter out ignorable events before they trigger a Flow execution. This will improve the performance of event handling and flow designer execution bandwidth for significant events, thereby improving the overall response time. This also allows DevOps admins to add tool webhooks with a broader scope without impacting system performance.
    -   Major fixes.
-   **Version 1.38.0 - May 2023**

    Changes:

    -   Azure DevOps organization support
        -   Connect a tool to Azure DevOps directly at the organizational level. Projects within the organization are discovered automatically. You can configure webhooks for multiple projects at once and easily update credentials at the organization level. This removes the need to connect a tool per ADO project.
    -   Group access for tools and applications
        -   Control access to tools and applications by adding user groups to the Maintained by field. Users belonging to the groups added can access only that tool or app, and can edit them only if their roles allow it. A new role, DevOps tool owner, has been introduced. Users with this role can only connect tools and will not have access to additional DevOps admin capabilities like system properties.
    -   Automatically retrieve pipeline steps when associating to an app
        -   While associating a pipeline with an app, the pipeline steps are also retrieved during import. No longer a requirement to run a pipeline once for the steps to be mapped in ServiceNow DevOps.
    -   Updated error messaging
        -   Improved error messages are displayed in Inbound events and Import requests to help find the root cause of a problem for real-time notifications. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
    -   Credentials expiry notification
        -   Admins and tool owners will be notified when tool credentials expire or are about to expire. They will be alerted through email, universal task, notification bell icon and a message on the tool record. This prevents any loss of data.
    -   Last event received
        -   Alert DevOps admins when events were being last received to caution them about any possible issue that might occur with their tool connection. The Last event received field in the tool record will help in easily troubleshooting any connection issues. You can set the number of days to display warning or critical alerts in the Last event received field in the tool record when events were not being received.
    -   Logging change status while pipeline is pending decision to resume execution
        -   Change information such as, Change Number, State, Assignment Group, Approvers, Planned Start/End date is displayed in the console logs of Jenkins and GitHub Actions, while the pipeline/workflow is pending for change approval. The ServiceNow DevOps application is polled at regular intervals and if there is any difference in the change information, it is logged directly in the console logs, thereby minimizing the hops to ServiceNow instance.
    Fixed:

    -   GitHub: The Discover action fails if an already discovered repository is deleted in GitHub.
    -   User with the "sn\_devops.viewer" role from DevOps Change is able to see the DevOps Config workspace link.
    -   SonarQube/SonarCloud: In a change request, the non-admin software quality summary record is overriden by next record instead of creating a new summary record.
    -   Change creation fails if data policies are present on change attributes.
    -   Unable to edit default view of the Change Request related list when DevOps Change Velocity is installed.
    -   Azure DevOps: When step type is not prod deploy, the Workitem and Commits related lists for change display incorrect entries.
    -   Jira: Duplicate workitems are created if an issue is updated immediately after creation.
    -   User with DevOps Viewer role cannot access KPI analytics for all Insights widgets in workspace.
    -   If a commit is processed in DevOps, deleted in DevOps and then re-commited from GitHub then committer details for the commit are not persisted.
    -   Incorrect \# of tests displayed in Application activity last 30 days widget.
-   **Version 1.37.0 - February 2023**
    -   Changed
        -   Improved error handling and guardrails: Improved error messages to help find the root cause of a problem while onboarding \(connection, discover, configure, or import\) a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   DevOps Change Workspace changes:
            -   Streamlined initial system setup for ServiceNow admins, which includes status of setup, improved identification of scope needed to complete, ability to set new passwords for account used for configurating credential alias, extra validation, and more.
            -   App Owner role expansion, which includes the ability to modify pipeline steps to assign application services or to set up change automation. App owners can also click Discover for tools to associate any new objects needed for their DevOps application. Updated tool administration which includes the ability to easily update credentials for every tool and check permissions for the given credentials.
        -   Rally integration: Connect to the Broadcom Rally planning tool to import Rally planning objects such as epics, stories, bugs, and tasks into DevOps data as work items. The Rally integration supports discovery of work items, configuring webhooks to send real-time data, and importing of historical data. Rally work items can be associated with commits used for change request acceleration.
        -   GitHub OAuth JWT authentication: Secure authentication of GitHub tool connection is now supported using OAuth JWT \(Json Web Tokens\). OAuth-JWT authentication using private key generated in GitHub is now supported.
        -   Get and update DevOps Change Request details: Get and update change request details associated with a Jenkins pipeline by running the snDevOpsGetChangeNumber and snDevOpsUpdateChangeInfo scripts respectively in the Jenkins pipeline.
        -   DevOps Accelerate Metrics: Now also shown in Digital Portfolio Management workspace by business application.
    -   Fixed
        -   DevOps Insights 1.36 application adds ACLs, which hides the Business Service and Business Application CIs in the CMDB.
        -   DevOps Subscription isn't adding the users with assigned role via an assignment group to the Participant table.
        -   Owner field is not getting populated when app is created via app onboarding.
        -   Jenkins Discover fails with large number of pipelines/jobs.
        -   When pipeline name is same across tools \(eg Gitlab, Jenkins\), pipeline executions of one tool is mapped to another tool.
        -   Branch details are missing for commit due to race condition when both tag and branch events get processed simultaneously.
        -   The 'Do you wish to configure?' checkbox is missing on service portal during App on-boarding.
        -   GitHub bulk commit processing persists more commits than required.
        -   For an Azure DevOps \(ADO\) pipeline with only one stage and change receipt enabled, the CR gets created with Actual Start date greater than Actual End date.
        -   Gitlab Discover populates only first 100 \(value defined in the import.coding\_tool.repos.per\_page property\) repos, pipelines.
        -   CI class name 'Package' created from DevOps package conflicts with CMDB CI OS package.
-   **Version 1.35.3 - September 2022**
    -   New
        -   Improved error messages to help you find the root cause of a problem while connecting to a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   You can now specify a particular MID Server directly on the DevOps Change workspace page while connecting to a tool.
-   **Version 1.35.0 - August 2022**

    GitHub Actions Integration:

    -   GitHub is a coding tool that is now updated to support the GitHub Actions orchestration capability in ServiceNow DevOps. You use the ServiceNow DevOps custom actions \(published to the GitHub Actions marketplace\) to integrate GitHub Actions pipelines and GitHub Environments.
    -   To update the data model, GitHub Actions Integration requires that GitHub is connected, configured, and that pipelines are discovered. GitHub Actions workflows are paused and resumed using custom actions
    The following custom actions are published to the GitHub repository:

    1.  ServiceNow DevOps Change
    2.  ServiceNow DevOps Test Report
    3.  ServiceNow DevOps Sonar
    4.  ServiceNow DevOps Register Artifact
    5.  ServiceNow DevOps Register Package
    Historical import and polling for Azure DevOps Artifacts:

    -   Import historical data for ADO artifacts by using the app-onboarding self-service catalog and periodic polling to fetch the data. The import framework helps onboard teams by fetching DevOps data into the instance without having to edit the pipeline or configure webhooks. The imported data provides insights into the root causes for complete change traceability, which helps to identify the root causes and areas of improvement.
    Out-of-the-box change approval policy Risk Inputs and Reject Reasons:

    -   The base-system DevOps default change approval policy improves the change automation and approval policy. Policy conditions run against collected DevOps data to auto-reject, auto-approve, or defer for manual approval. The data could be metrics on commits, code coverage, test results, sonar scan results, risk inputs, and so on. The change approval policy is configurable. To help users quickly take corrective actions, rejection reasons are captured in the CHG work notes.
    Jenkins snippet generator:

    -   The Jenkins plugin for ServiceNow DevOps can generate DevOps scripted pipeline steps. This helps developers to adopt ServiceNow DevOps features quickly and to modify pipelines easily.
-   **Version 1.34.1 - May 2022**
    -   Changed
        -   Out of the box change approval policy: Out of the box \(OOTB\) DevOps default change approval policy is implemented to update the change automation and approval policy. With which, the policy conditions are applied on the DevOps data collected to either auto-reject or auto-approve or defer for manual approval. The DevOps data could be metrics on commits, code coverage, test results, sonar scan results, etc. The change approval policy is configurable.
        -   Import historical data for DevOps tools - Azure DevOps: Import historical data for all capabilities \(Code, Plan, and Orchestration\) by using the app-onboarding self-service catalog and periodic polling to fetch data. The import framework helps onboard teams by fetching DevOps data into the instance without having to edit the pipeline or configure webhooks. The imported data provides insights into the root causes for complete change traceability. Starting with version 1.34, you can import the data and configure a polling mechanism for Azure DevOps.
        -   jFrog - Jenkins artifactory integration: Integrate Jenkins and jFrog Artifactory in ServiceNow DevOps and use this data for traceability and linking CI/CD pipelines in ServiceNow. Associate the build pipelines \(CI\) with the artifacts built and published to jFrog, and associate the deploy pipelines \(CD\) with the packages downloaded from jFrog repositories to deploy. Linking these CI/CD pipelines with the artifacts and associating those with the change creates the link from commit to artifacts built and deployed for change traceability.
    -   Fixed
        -   GitLab integration: Very large GitLab build numbers are saved as extreme big numbers in build\_number column of Task Execution table
        -   Security bug
-   **Version 1.33.1 - February 2022**
    -   Changed
        -   Change traceability
            -   Change traceability is a non-invasive way to utilize DevOps data to accelerate manual changes. This allows for quicker time to value on the path to full change automation. With this release, you can associate either artifact versions, build numbers or a release version to a manually created change request that will pull in DevOps data such as work items, commits and tests.
            -   The implementation does not require pipeline modifications to include ServiceNow DevOps change tasks. Thus, with the associated DevOps data, you have complete visibility of what was deployed to production to accelerate your manual changes.
        -   Support Import and Polling for JIRA, GitHub and Jenkins
            -   The import via app-onboarding self-service catalog and periodical Polling to fetch data for all capabilities \(Code, Plan and Orchestration\) will help you to onboard teams easily by quickly getting DevOps data into ServiceNow without having to edit the pipeline or configure webhooks. The imported data will provide you the insights into the root causes for complete change traceability. This release will cover the importing framework for JIRA, GitHub and Jenkins and configurable polling mechanism.
            -   The following app spoke dependencies are added to support the feature
                -   Jenkins V2 Spoke – 1.1.2
                -   Jira Spoke – 3.1.1
                -   GitHub Spoke – 2.2.2
        -   System Health Dashboard &amp; Notifications
            -   The system health dashboard provides a way to monitor or troubleshoot the data that is coming in from your connected DevOps tools to ServiceNow DevOps. This is a way for DevOps admins to have better visibility into the inbound events processing data received from various tools which have been configured in DevOps. There’s also an easy way to check the latest status of the tool connectivity.
            -   Email notifications can be sent to a group that will provide weekly information on key stats such as pipeline executions, change requests, and inbound event data. This allows DevOps admins to be proactively notified if there are any possible changes to the overall help of their DevOps system.
    -   Fixed
        -   Azure DevOps
            -   If multiple commits are processed at the same millisecond, duplicate repositories are created
            -   ADO tool created saves credentials in clear text
        -   GitLab notifications are stuck in waiting and error state when midserver is intermittently up and down
        -   Pipeline UI is not loading for pipelines having large number of pipeline executions
        -   DevOps relationship rules are executed for change requests with non-DevOps category
        -   Artifact registration fails for Free style job after upgrade to 1.32
        -   Security bug
-   **Version 1.32.0 - November 2021**
    -   New
        -   Jenkins Support for parallel stages: ServiceNow DevOps will now track stages that run in parallel/nested in Jenkins pipelines. The parallel stages will be rendered accurately in the Pipeline User Interface, and automated Change Requests will only get created once parallel stages preceding it are complete.
        -   Azure DevOps: Bulk Processing feature enabled for ADO tool's Orchestration Capability to optimize the processing of events.
        -   Table Archiving Policies
            -   Archive Rules added to auto archive data which is older than 9 months \(configurable, can be configured for all archive rules using one property\).
            -   Destroy Rules are added which will purge the archived data older than 3 years.
            -   Above Archive and Destroy Rules are applied to tables consisting of data – PipelineExecution, StepExecution, TaskExecution and all related tables.
    -   Fixed
        -   Agile Development 2.0: When user with scrum\_product\_owner and scrum\_story\_creator roles creates a user story, the corresponding work item is not created in DevOps.
        -   Jenkins: Multibranch pipelines with BitBucket configuration has task execution value as empty Pipeline executions are created even though Track is NOT enabled for multibranch pipeline and nested pipeline After recreating Jenkins tool, inbound events are created even though pipelines are not discovered or tracked.
        -   Azure DevOps: For custom project \(not Agile project\): When ADO work item is deleted, inbound event errors with error code 400 thereby not updating corresponding DevOps workitem’s state to Deleted.
        -   Change Receipt flag for a pipeline step record is not updated when app-onboarding payload is posted
-   **Version 1.31.0 - October 2021**
    -   New
        -   Support for parallel stages in Azure DevOps
            -   ServiceNow DevOps will now track stages that run in parallel in Azure DevOps Release pipelines. The parallel stages will be rendered accurately in the Pipeline User Interface, and automated Change Requests will only get created once parallel stages preceding it are complete.
            -   Note: Support for parallel stages is limited to Azure DevOps Release pipelines; Build pipelines will continue to be tracked and rendered in serial in ServiceNow DevOps.
        -   Return Change Request Number in Jenkins
            -   When a Jenkins job or pipeline is configured for Change Control, this feature will cause the Change Number for the newly-created change to be output to the build log file. This information helps the pipeline owner understand why their pipeline is paused and allows them to follow up on the change status if desired. The log output is informational only, and the existing changeInfo is recommended for programmatically retrieving details and status information for a pending DevOps Change Request.
        -   Support for Azure DevOps legacy URLs
            -   ServiceNow DevOps now supports use of the legacy \(visualstudio.com\) URL in Azure DevOps projects. The legacy URL may now be used interchangeably with the new \(azure.com\) URL.
-   **Version 1.30.0 - September 2021**
    -   New
        -   Restart stages for Azure DevOps: Support pipeline and stage/step restarts that enables you to trace the information correctly as the pipeline run is the same
        -   GitLab OAuth: Support OAuth as it is more secure than basic auth to prevent malicious actions and unwarranted visibility
    -   Fixed
        -   Jenkins plug-in for ServiceNow DevOps
            -   Security vulnerabilities related to Jenkins plugin dependencies. \(Note: Starting with DevOps 1.30, the minimum base version of Jenkins server must be 2.204.6 to fix the vulnerabilities\)
            -   Notification stuck in waiting state for multibranch pipelines that have a branch name with special characters \(for example, scratch/dev!@@&amp;mybranch\)
        -   Azure DevOps
            -   Build pipeline: Artifact versions are not displayed in Change Request related list when both package and change are created in same stage.
            -   The **Committed at** field is changed when tag is created to a historic commit
            -   Release pipeline executions create package with same name on each run
            -   Performance issues on DevOps pipeline execution, test summary and callback tables.
            -   Intermittently, duplicate work items are created in DevOps when work item is created from Agile 2.0 ServiceNow plugin.
            -   Test results not seen in deploy pipeline when generated from multiple build pipelines.
    -   Changed: Starting with DevOps 1.30, the minimum base version of Jenkins server must be 2.204.6 to fix the vulnerabilities.
-   **Version 1.29.0 - August 2021**
    -   Feature changes:
        -   Jenkins plug-in for ServiceNow DevOps
            -   Plugin from Jenkins Marketplace: Easy onboarding by directly installing from the Jenkins Marketplace. Mainly to remove ALL friction for dev teams to be able to self-onboard and use the solution
            -   Improved log levels: Logger is key to diagnose or debug a problem. However, turning on excessive logging can rapidly flood your system and terminate the servers. Dev teams will now have the ability to set the log levels as desired to trace out the exact root cause of a problem
            -   Reducing Excessive pipeline info call: To reduce the number of calls from Jenkins to ServiceNow to know whether a pipeline is being tracked or not every time a Jenkins build is triggered, a new flag “Force Tracking Check” has been introduced in Jenkins configuration. When this is disabled, a file with the pipeline tracking and testing info is created which will be used to determine to know what pipelines are tracked on ServiceNow to send notifications. Whenever a pipeline tracking flag or test info is updated on ServiceNow application by user, ServiceNow will make a POST REST API call to Jenkins to update the pipeline tracking file
        -   Change request on Categorization: When a Change Request is automatically created, it has Category=DevOps. The category values you have today denotes a type of change, like Hardware, Software, Network, etc. whereas “DevOps” value is more like the source of change. There could be instances where a change is sourced by DevOps and is of type Hardware or Software. In addition, already the Category list could be used for a different purpose and use values like, e.g. non-Production, etc. DevOps team will now have the ability to uniquely identify that a change record is a “DevOps Change Record”.
        -   Improved performance of Inbound Event processing throughput
    -   Fixes:
        -   ADO Pipeline and task executions are appearing when tracking specific pipeline at tool level, but track is not enabled for pipeline
        -   Change request auto approve and reject comments are not set in the sysapproval\_approver table record
    -   Jenkins plug-in for ServiceNow DevOps: 1.29
-   **Version 1.28.0 - July 2021**
    -   New:
        -   Inbound events erroring with certain exception types will be automatically retried by a scheduled job. The exception types, retry count and age of errored inbound events to process are configurable in DevOps properties
        -   Jenkins Integration Improved security, you can now use API key to create to Jenkins tool in ServiceNow DevOps The change request rejected/cancelled reason is sent back to the respective Jenkins pipeline so that you will know why the change was rejected/cancelled.
    -   Fixed:
        -   Code push and tag push events fail for an empty commit that does not have any file changes
        -   GitHub: Error 404 - Import is not working at Repo level - When tool url has trailing '/' Artifact is not linked to task execution when pipeline name contains the branch name
        -   GitHub Enterprise - Unable to configure a repository due to incorrect webHookResourcePath Layout of pipeline UI page is broken in IE11 Jenkins Multibranch pipeline events stuck in Waiting state when branch name has '/' and has Junit tests Multibranch pipeline with a space doesn't work
        -   Azure DevOps:
            -   DevOps plan import request for Azure DevOps fails with big backlog \(for example, &gt;2000 workitems\)
            -   Notification Inbound fails for a release that include an Azure Artifact
            -   When the credentials change/expire after the tool is created, state of import requests for Discover action are success instead of error In a single pipeline execution, the revert commit is persisted prior to the original commit thereby not removing the revert commit from the Run Commits
        -   Jenkins plug-in for ServiceNow DevOps: 1.28
-   **Version 1.27.0 - June 2021**
    -   Changed:
        -   Software quality framework: Updated data model specifically for code quality and security tools​. An extensible framework that allows anyone to create custom integrations to any Code Quality and Security tools.
        -   SonarQube support: OOTB support for Azure DevOps and Jenkins. Whenever there is a scan triggered from the pipeline, the scan results are captured in ServiceNow DevOps that is needed to determine change risk
        -   Allow change fields to be set via the API. This overrides any step configurations previously set. The current functionality stays intact with the only difference being that fields can now be set from the API.
        -   Jenkins plug-in for ServiceNow DevOps: 1.27
    -   Fixed:
        -   Race condition causing incorrect DevOps Inbound Event waiting reason and incomplete pipeline executions
        -   DevOps change creation fails with legacy change management plugin
        -   When GitHub pusher email is empty, Committer &amp; Committer Email are not populated in DevOps
        -   For BitBucket, DevOps tag updates are not processed
-   **Version 1.26.1 - May 2021**
    -   Changed:
        -   Dynamically create connection aliases \(under a parent alias\) which avoids the need for a System Admin to create connection aliases separately when creating the DevOps tool. This feature uses the platform "Child Aliases" feature and is available from Paris. DevOps application ships with parent aliases and corresponding configuration templates \(Basic Auth, API Key and OAuth - Authorization Code\) which can then be used to create connection and credential under the created child alias.
    -   Fixed:
        -   Pipeline UI is broken when all task executions are skipped
        -   Test tool integration expects the toolID in the query parameters to be an orchestration tool id DevOps tag updates are not processed
        -   There is no default handling for unsupported azure states like SucceededWithIssues Filter the commit api to fetch only commits for Jenkins
        -   Branch info not getting updated for commits on code merge
    -   Plugin and extensions compatibility:
        -   Jenkins plug-in for ServiceNow DevOps \(1.24.0\) https://marketplace.visualstudio.com/items?itemName=ServiceNow.vss-services-servicenow-devops Version: 1.24.0
-   **Version 1.25.1 - April 2021**
    -   Changed:
        -   Azure DevOps: Onboarding ADO tool made easy by enabling the customers to choose only specific pipelines to track
        -   You may now set archive/purge conditions for the Inbound Events table to handle high volumes of DevOps data
    -   Fixed:
        -   Azure DevOps: When job names under different stages are the same, artifact/package is not linked to task execution
        -   Azure DevOps: For a release gate with manual only trigger on a stage, release pipeline creates two pipeline execution records
        -   Artifact generation includes commits from different branch for failed executions in Multibranch pipeline
        -   DevOps flow designer scripts should execute as ‘User who initiates session’ instead of ‘System User’
-   **Version 1.24.0 - March 2021**
    -   Changed:
        -   Change request pipeline API changes: Set additional change request attributes when creating the change request from Jenkins and Azure DevOps pipelinesSet flag from pipeline so ServiceNow DevOps will not close the change request
        -   GitLab and Azure DevOps repository tags are now supported in ServiceNow DevOps
        -   Can now process bulk commits from GitLab
        -   'version' is now an optional field in the plan payload
    -   Fixed:
        -   Pipeline UI renders a blank page for pipeline that creates artifact version in the same stage as change
        -   In a change request, user with only DevOps Viewer Role is able to see all commits in the system instead of commits included in the artifact
        -   Change request is not created when commits have empty committer
        -   Change request is not created if upstream stage is 'skipped'
        -   For Azure DevOps and GitLab, reverted commits in a merge commit show in a change request's commits related list
-   **Version 1.22.0 - January 2021**
    -   Feature changes:
        -   Automatically importing and categorizing GitLab JUnit tests during the pipeline execution is now supported.
    -   Fixes:
        -   Large commits are now supported with Azure DevOps.
        -   Jenkins pipeline under DevOps change resumes automatically after restart of Jenkins server.
        -   Two pipeline execution records are created if change control is enabled on the first stage of a freestyle pipeline.
        -   Inbound event generates error when processing workitem for ADO tool with a project that has a space in the name.
        -   When multiple ADO pipelines \(all with tests\) are run in parallel, inbound events get stuck in waiting state with exceptions.
        -   App Onboarding payload is not stored in the encrypted field. Inbound Stage completion notifications from Azure DevOps are not processed correctly resulting in a timeout.
        -   Azure release gates reattempt use cases are failing with change receipt changes.
        -   Jenkins global tool configuration username/password are stored as plain texts in config.xml.
        -   Jenkins pipeline fails if pipeline has not been discovered.
-   **Version 1.22.0 - January 2021**
    -   New: Multiple work items for a commit are now supported and will be linked to the commit in ServiceNow DevOps. In addition:
        -   The work item syntax in the commit message can be customized to reflect your organization's processes.
        -   Selecting the work items through the Azure DevOps user interface when committing is now supported.
-   **Version 1.21.0 - December 2020**
    -   New:
        -   You can now delete many DevOps objects such as Tools, Repositories, and Pipelines. See product documentation for full list and restrictions.
        -   You can now obtain the change number created in a pipeline for further interaction with the change request from the pipeline.
    -   Removed:
        -   The Configuration Item field on a tool has been removed.
        -   Under Use Mid Server selection, the two fields \(Mid Server Application, Mid Server Capability\) have been removed.
-   **Version 1.20.1 - January 2021**

    For the following fixes, install the Jenkins plugin for ServiceNow DevOps \(1.20.2\).

    -   Fixed:
        -   Security fix
        -   If Pipeline has not been discovered, the Jenkins plugin behavior can fail
        -   When Jenkins is restarted, deployments are resumed without change approval
-   **Version 1.20.0 - November 2020**
    -   New:
        -   Change registration: Pipeline steps can now be configured to create change receipts, which includes all of the pipeline data, but does not require approval to proceed forward in the pipeline.
        -   Test tool improvements: JUnit and Selenium tests can now be auto-categorized and additional test types can be configured for auto-categorization.
        -   Jenkins skipped stages: When stages are skipped, due to branch conditions, the Pipeline UI will not display them.
-   **Version 1.19.1 - October 2020**
    -   New:
        -   DevOps Pipeline Steps are now autocreated as the Jenkins pipeline runs. You no longer need to manually create the Pipeline Steps in ServiceNow or configure the notifications in Jenkins. Change is still configured manually on the desired steps in Jenkins and in ServiceNow DevOps.
        -   DevOps has increased the data resiliency by adding retries to most tool communication from the ServiceNow flows. You can modify the retry configuration to match your needs.
-   **Version 1.18.1 - December 2020**
    -   Fixed: This release is a fix release. It fixes a compatibility issue with the change feature.
-   **Version 1.18.0 - September 2020**
    -   New:
        -   Azure DevOps release pipeline support
            -   Includes support for the ServiceNow DevOps Release Gate extension or using the Invoke Rest API call as a pre-deployment Gate.
    -   Upgrade impacts and troubleshooting:
        -   If you already have an ADO tool connection, you will have to update the ADO Release URL in the Connection &amp; Credential Alias.
-   **Version 1.17.0 - August 2020**
    -   New: New lighter touch Azure DevOps integration removes the need to add start and end job notifications to ADO pipelines. Pipeline modifications are now only needed for pipeline artifact and change.
    -   Fixed:
        -   Added support for batch commits in GitLab notifications.
        -   Corrected handling of Azure DevOps connection attempts made with invalid URL or credentials.
        -   Corrected the pipeline execution start/end time issue in Azure DevOps.
-   **Version 1.16.0 - July 2020**
    -   New:
        -   GitLab Coding Tool integration
            -   Discover repositories that are owned, a member of, or through keyword search
            -   Manual configuration of webhooks
        -   GitLab Orchestration Tool integration
            -   Support for Basic Pipeline Types
            -   Manual configuration of webhooks
-   **Version 1.14.0 - May 2020**

    -   New: Support for historical Import of ADO Work Items.
    -   Fixed: Corrected issue for freestyle jobs under folders in Jenkins where upstream execution is not set for child jobs.
    **Note:** This version of the app can only be installed on instances running New York or later.


