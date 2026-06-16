---
title: DevOps Change Velocity release notes
description: Version history for the DevOps Change Velocity application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-change-velocity.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 33
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Change Velocity release notes

Version history for the DevOps Change Velocity application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.0.0 - June 2026**
    -   Changed:
        -   Jira authentication with 3LO
            -   Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.
        -   Bitbucket Cloud basic authentication using API token with scopes
            -   Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.
-   **Version 6.3.0 - March 2026**
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
        -   Health scan enhancements
            -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
            -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in GitHub, GitLab, Azure DevOps, and Jenkins using the DevOps webhook configuration analysis health check.
            -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
            -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
            -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting View all findings in the Health scan findings widget.
-   **Version 6.1.0 - August 2025**
    -   New:
        -   Import based evidence collection framework
            -   Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub and Azure DevOps \(ADO\) orchestration tools.
    -   Changed:
        -   Support for MID Server cluster
            -   Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.
        -   Improved UX for DevOps Change health scans
            -   Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.
        -   Pipeline association for GitHub Actions
            -   When onboarding GitHub Actions pipelines \(workflows\) through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.
        -   Tool connection check status
            -   If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.
        -   New roles for vulnerability integration
            -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
            -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
        -   Support for multiple test summaries in single Azure DevOps pipeline step
            -   When a step in an Azure DevOps pipeline has multiple test summaries, the pipeline may get stuck waiting indefinitely. This update ensures that such wait states are resolved efficiently.
        -   GitHub pipeline rename
            -   Previously, renaming a GitHub workflow caused event processing to be ignored.Now, DevOps Change Velocity stores the context of individual GitHub workflow runs and updates pipeline names prior to event processing.
        -   Improvements to Agile 2.0 Story-Release syncing 
            -   Previously, unmapped or changed releases in Agile 2.0 Stories did not have outdated mappings removed, leading to inaccurate story lists for each release. With this update, only correct Story-to-Release mappings will be kept.
-   **Version 6.0.0 - May 2025**
    -   New:
        -   Bitbucket cloud tool integration with ServiceNow
            -   Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity, enabling ServiceNow to connect, discover, import, and process real-time repository events.
    -   Changed
        -   Additional scans for DevOps Health Scan Content pack
            -   Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with catching configuration issues like plugin and version incompatibilities or pipelines that chronically fail have been added.
        -   Bitbucket Server and Data Center tool integration with ServiceNow
            -   Improved support for Bitbucket Server and Data Center by enabling Pull Request functionality.
        -   Secure token for Rally Integration User
            -   Rally integration now supports a more secure integration user token, instead of basic auth for integration user, and is now consistent with the remaining planning tool integrations.
-   **Version 5.1.0 - February 2025**
    -   New:
        -   Support for proactive health scans
            -   Detect anomalies and issues in your DevOps Change Velocity instance by using a suite of proactive checks. These checks can help you identify problems that are not obvious in the product UI but can easily be detected through table scans. They are either Scheduled or On-Demand in nature, based on the type of check.
        -   Harness tool integration with ServiceNow
            -   Integrate the Harness orchestration tool with DevOps Change Velocity. This integration enables you to connect, discover, import, process real-time events, and integrate CI/CD with change in ServiceNow for Harness pipelines.
    -   Changed:
        -   Simplified onboarding of orchestration tools that are not supported in the base system
            -   The simplified generic framework provides you an easy-to-use solution to integrate custom orchestration tools with ServiceNow DevOps Change Velocity, requiring minimal knowledge of the platform. It reduces the complexity of integration by lowering the amount of custom coding needed and by simplifying the overall process for both customers and partners. By streamlining the onboarding of new orchestration tools, the framework enables faster adoption, smoother scaling, and easier onboarding of additional teams. This enables you to experience fewer integration challenges, speeding up the user adoption process and reducing friction during the transition. This generic framework supports the integration of any orchestration tool not natively supported by ServiceNow in the base system.
        -   Custom fields for planning tool integration
            -   Bring in additional custom fields for work items and thereby experience enhanced configurability of planning tools supported in the base system by DevOps Change Velocity.
        -   Enhanced lead time calculation
            -   Lead time calculation now considers Artifacts/Packages registered as part of Pipeline Execution and is calculated based on commits associated with it.
        -   Improved in-product guidance for effective self-service adoption
            -   Improved user experience by adding documentation or navigation to external documentation at various places in workspace.
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
    -   New:
        -   Improved journey to full change automation using models
            -   In-product guidance to leverage DevOps change models and easily create DevOps changes without disruption of your change process in the DevOps Change Workspace.
            -   Fast-track your change process by using a new DevOps Simplified change model, which doesn't contain the Assess state. Change approval for this model is based on the DevOps Simplified Model Change policy.
            -   Approval policy is manual by default for the corresponding DevOps and DevOps Simplified change models.
            -   The new Change DevOps Update execution state flow in the DevOps model is now used to send a callback to the third-party orchestration tool.
        -   DevOps data for Change traceability in Service Operations Workspace \(SOW\)
            -   Add and edit DevOps data in a manually created change request in Service Operations Workspace for a unified change request experience in both DevOps Change Workspace and Service Operations Workspace.
            -   View the DevOps summary card in the Overview tab of the SOW Workspace for all the change states \(New, Assess, Authorize, Schedule, Implement, Review and Close\). You can add or edit data on the DevOps summary card for DevOps change requests created manually.
        -   Note: This feature is only available for the Xanadu release.
    -   Awareness of DevOps change to Change managers in SOW Admin center for\` configuration
        -   ServiceNow admins can now see a navigation link to the DevOps Change Workspace if it is installed, and the Get App link which enables them to install DevOps Change Velocity \(DCV\) if not already installed \(only applicable for ITSM Pro or if DCV is available for installing\).
        -   Note: This feature is only available for the Xanadu release.
    -   -   Awareness of DevOps change in Adoption Blueprints
    -   A new adoption blueprint, "Modernize your change management process", is now available in Admin Center Adoption Blueprints that gives ServiceNow admins a walk through on how they can adopt the required capabilities to allow their change process to dynamically scale without compromising stability and governance.
-   Note: This feature is only available for the Xanadu release.
    -   Awareness of DevOps change to ServiceNow admins in the Change management setup
        -   The new Change Management configuration in SOW Admin Center highlights features that could be used by Change Admins and Managers to modernize their change management journey such as change models, risk and success scores, approval policies and DevOps, which thereby serves as a one stop shop for customers looking for guidance on how to modernize change.
        -   Note: This feature is only available for the Xanadu release.
    -   Changed:
        -   DevOps Change Request Manual Approval Flow trigger change
            -   The DevOps Change Request Manual Approval flow wont trigger for DevOps change requests whose model is a base system DevOps change model \(DevOpsorDevOpssimplified\) to avoid conflicts and errors.
        -   Support reruns with GitHub Actions
            -   Rerunning of failed jobs in GitHub Actions workflows is now supported with creating change requests.
            -   Reruns of any failed stage before or after or at the time of change creation is supported.
        -   Support API\_KEY for Jira Server: The API\_KEY authentication method is now available for Jira Server, aligning it with the existing support already available for Jira Cloud.
        -   Persist branch details in pipeline execution to determine commits from artifacts and packages
            -   A new column is now added to the pipeline execution table to reference the branch table and enable filtering by branch to ensure right commits get associated to a change when users work on multiple versions of an artifact simultaneously.
            -   Enhanced the commit calculation logic for Artifact version to filter by branch.
            -   The commit association logic for packages has been changed to show all the commits that are being deployed as part of a package, including the commits from previous artifact versions that have not been deployed, but only on the same branch
        -   Removed:
            -   To make the Change - DevOps Implement flow of the DevOps model more suitable for DevOps changes, change tasks are no longer automatically created.
            -   The DevOps Change Request Minimal Automation Approval Flow and DevOps Change Request Advanced Automation Approval flows won't trigger for DevOps change requests whose model is a base system DevOps change model \(DevOpsorDevOpssimplified\) to avoid conflicts and errors.
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
-   DevOps Workspace improvements
    -   The Tools module now has three list groups - All, Status, and Capability.
    -   Test Results and Software Quality functionalities are now available in the List module for easy navigation.
    -   You can create your own lists in the "My Lists" section.
    -   System health, Integrations and Advanced \(earlier called as Troubleshooting\) are now available in the Admin module.
-   DevOps Insights improvements
    -   Use the Insights dashboard in the DevOps Workspace as part of the Next Experience, with newer and relevant indicators/widgets such as Deployment success rate and Failed Deployments along with safeguards and better filtering.
    -   DevOps Standard Insights on platform has been deprecated for all new DevOps users.
    -   Platform \(record producer\) users are now redirected to the workspace to create tools or apps. Release/legacy users can still directly go to the platform URL to create tools or apps in the platform through the "Create New \(legacy\)" and "Create App \(legacy\)" options.
-   **Version 3.1.0 - February 2024**
    -   New:
        -   GitLab integration with Docker Container
            -   Integration of GitLab with ServiceNow DevOps has been simplified using Docker Container which is published to DockerHub. This supports ServiceNow DevOps CHG creation, SonarQube integration with GitLab pipelines, and registering artifacts and package creation with ServiceNow DevOps.
        -   GitHub Issues integration
            -   GitHub now supports the Plan capability with GitHub Issues integration in addition to the code and orchestration capabilities. GitHub Issues of the repository can also be discovered and linked with the GitHub commits and persisted in the ServiceNow DevOps CHG, which can be used for policy decisions of ServiceNow DevOps CHG acceleration.
        -   Supported various unit test types for GitHub Actions
            -   Automatically publish test results of various unit test tool reports like NUnit, pytest, jest, JUnit, XUnit without any custom API calls to publish to the ServiceNow DevOps CHG.
        -   Improved error logging and handling with ServiceNow DevOps extensions
            -   ServiceNow DevOps extensions published for GitHub Custom Actions, Jenkins plugins, ADO extensions now have improved error logging and handling for easier troubleshooting.
        -   Guided change automation experience
            -   Better in-product guidance is now provided on the various ways to leverage DevOps changes and how to easily adopt DevOps changes without complete disruption of your change process. A stepper guides you to automate DevOps change creation. You can check the connection status of a tool while selecting a pipeline on the stepper and you are also alerted before proceeding to the next step. Two new state transition flows: Change - DevOps - New and Change - DevOps Schedule, for DevOps change model are introduced to move and track changes through these states. The DevOpsChangeRelationshipHelper script has been introduced to retrieve data associated with a change request based on the specified relation type.
        -   Changed error handling for DevOps change request flows
            -   You can view errors corresponding to a change request in the worknotes of the change request and in the console logs of the pipeline tool when a business rule or data policy causes an issue while updating a change in the DevOps Change Request Manual Approval, DevOps Change Request Minimal Automation Approval, or DevOps Change Request Advanced Automation Approval flows.
        -   Handling of Azure DevOps and GitHub API rate limiting
            -   When Azure DevOps or GitHub API rate limits are exceeded, DevOps Change Velocity will defer processing of new events until GitHub throttling has subsided to handle large volumes of data.
        -   Support pagination in Discover import requests for pipelines, repos, plans for Azure DevOps and GitHub
            -   Data is now retrieved from 3rd party tools in batches \(paginated way\). This will help you to scale by onboarding many teams having large volumes of data.
        -   Removal of Connection Admin and Flow Designer roles for DevOps Admin &amp; Tool Owner
            -   Visibility and editing capabilities of DevOps Admins and Tool Owners has been limited by removing the Flow Designer and Connection Admin roles for these users.
        -   Changes to artifacts and packages
            -   The overall experience with adoption, implementation, and error handling for artifacts and packages has been improved.
        -   GitLab notification processing improvements
            -   Scalability has been improved with seamless handling of GitLab events.
        -   SonarQube Integration changes
            -   SonarQube overall quality gate status for the scan summary is now supported and SonarQube integration with GitLab pipelines is also supported using ServiceNow DevOps Gitlab Docker Container.
-   **Version 3.0.0 - November 2023**
    -   New:
        -   Minimal Automated DevOps Change Approval.
        -   Studio support to DevOps Change Velocity.
    -   Changed:
        -   Renamed existing DevOps change flows appropriately.
-   **Version 2.0.0 - August 2023**
    -   New:
        -   Security framework
            -   A new integration framework and data model has been added specifically for application security tools. It is an extensible framework that also allows you to create custom integrations with any application security tools.
        -   Veracode support
            -   Connect Veracode that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results. This helps you determine how vulnerable your code is. Veracode scans that are configured on GitHub Actions, Jenkins, and Azure DevOps pipelines are supported in the base system. You can view the security scan results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance or in the Pipeline UI. You can use security results in defining change policies and conditions for change automation.
        -   Multimodal support
            -   Multimodal change is a new change management feature that allows better flexibility in defining change models or processes to reflect modern development practices. DevOps supports this new feature using which you can create change models with states and rules that determine the transitions between the states to deliver "fit for purpose" change models with a suite of succinct flows and flow actions built in Flow designer. With DevOps change models, change teams can now selectively transition to a wide range of models that are fully optimized for their specific use cases.
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

    -   Changes:
        -   Azure DevOps organization support
            -   Connect a tool to Azure DevOps directly at the organizational level. Projects within the organization are discovered automatically. You can configure webhooks for multiple projects at once and easily update credentials at the organization level. This removes the need to connect a tool per ADO project.
        -   Group access for tools and applications
            -   Control access to tools and applications by adding user groups to the Maintained by field. Users belonging to the groups added can access only that tool or app, and can edit them only if their roles allow it. A new role, DevOps tool owner, has been introduced. Users with this role can only connect tools and will not have access to additional DevOps admin capabilities like system properties.
        -   Automatically retrieve pipeline steps when associating to an app
            -   While associating a pipeline with an app, the pipeline steps are also retrieved during import. No longer a requirement to run a pipeline once for the steps to be mapped in ServiceNow DevOps.
        -   Changed error messaging
            -   Improved error messages are displayed in Inbound events and Import requests to help find the root cause of a problem for real-time notifications. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   Credentials expiry notification
            -   Admins and tool owners will be notified when tool credentials expire or are about to expire. They will be alerted through email, universal task, notification bell icon and a message on the tool record. This prevents any loss of data.
        -   Last event received
            -   Alert DevOps admins when events were being last received to caution them about any possible issue that might occur with their tool connection. The Last event received field in the tool record will help in easily troubleshooting any connection issues. You can set the number of days to display warning or critical alerts in the Last event received field in the tool record when events were not being received.
        -   Logging change status while pipeline is pending decision to resume execution:
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
    -   Changed:
        -   Improved error handling and guardrails
        -   Improved error messages to help find the root cause of a problem while onboarding \(connection, discover, configure, or import\) a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   DevOps Change Workspace changes
            -   Streamlined initial system setup for ServiceNow admins, which includes status of setup, improved identification of scope needed to complete, ability to set new passwords for account used for configurating credential alias, extra validation, and more.
            -   App Owner role expansion, which includes the ability to modify pipeline steps to assign application services or to set up change automation. App owners can also click Discover for tools to associate any new objects needed for their DevOps application. Changed tool administration which includes the ability to easily update credentials for every tool and check permissions for the given credentials.
        -   Rally integration: Connect to the Broadcom Rally planning tool to import Rally planning objects such as epics, stories, bugs, and tasks into DevOps data as work items. The Rally integration supports discovery of work items, configuring webhooks to send real-time data, and importing of historical data. Rally work items can be associated with commits used for change request acceleration.
        -   GitHub OAuth JWT Authentication: Secure authentication of GitHub tool connection is now supported using OAuth JWT \(Json Web Tokens\). OAuth-JWT authentication using private key generated in GitHub is now supported.
        -   Get and update DevOps Change Request details: Get and update change request details associated with a Jenkins pipeline by running the snDevOpsGetChangeNumber and snDevOpsUpdateChangeInfo scripts respectively in the Jenkins pipeline.
        -   DevOps Accelerate Metrics: Now also shown in Digital Portfolio Management workspace by business application.
    -   Fixed:
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
-   **Version \(1.36.0\) - November 2022**

    Changes:

    -   Updated error messaging
        -   Improved error messages to help find the root cause of a problem while connecting to a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them. A new permission check when connecting a tool shows permissions available from the credentials instead of the required permissions.
    -   You can now specify a particular MID Server directly on the DevOps Change workspace page while connecting to a tool.
    -   Pull Request \(PR\) pipeline executions support GitHub/Jenkins
        -   Track and support Pull Request pipeline executions for the Jenkins orchestration tool and PRs created in the GitHub coding tool. Integrate PR data like Pull Request ID, Commits, Origin branch, Destination branch, Raised by, Approver, Comments, PR raised time, PR approved time, and PR merged/closed time from the GitHub coding tool to the DevOps CHG created for the corresponding pipeline execution in the Jenkins orchestration tool. In addition, attach the PR-related data to the DevOps CHG to review who authorized, validated, verified, and approved the PR merge process.
    -   Import historical data for DevOps tools and CHG traceability - Gitlab
        -   Import historical data for Code and Orchestration capabilities by fetching data through the app-onboarding self-service catalog and periodic polling.
        -   The import framework helps to onboard teams by importing DevOps data into the instance without having to edit the pipeline or configure webhooks. The imported data provides insights into root causes for complete change traceability of Commits, Branches, Tags, and Pipelines \(both CI and CD\) from Gitlab.
    -   SonarQube - Support new code metrics
        -   Integrate New Code metrics provided by SonarQube scan results apart from the Overall code scan results, based on the New Code configuration in SonarQube. The following new code metrics are integrated in this release: New Vulnerabilities, New Maintainability Rating, New Reliability Rating, New Security Rating, New Bugs, New Code Smells, New Technical Debt, and New Lines of Code. This is supported for the Jenkins, Azure DevOps, and GitHub Actions orchestration tools.
    -   Split.io Feature Flag tool Integration with ServiceNow
        -   This integration extends ServiceNow to manage the CHG approval process for feature flags and segments of Split.io. ServiceNow DevOps can now manage updates to feature flags.
        -   Split.io feature flag tool integration support enables discovery of workspaces, environments, segments, and feature flags. You can set CHG request fields to enable Split.io for CHG control. Upon approval/rejection of a CHG request, the callback URL in split.io for the split or segment is invoked to resume implementation of the update to the split and segment
    -   The DevOps insights dashboard can now filter by Business Application
    -   For the Jenkins integration, The minimum supported Jenkins version is 2.289.1
    Fixed:

    -   Artifacts with the same name but different versions are considered duplicates \(even though they belong to different repositories\).
    -   Two pipeline executions were created for an ADO release pipeline when the ADO project name has spaces and special characters.
    -   DevOps - Change tickets have links to the pipeline home instead of a specific execution.
    -   Azure DevOps
    -   Commits and work items are not getting linked to artifacts for pipelines that have Publish artifacts in the first step or job.
    -   Azure DevOps - Imported commit details show the incorrect number of files changed
    -   Work items, test summaries, and commits are not attached to change in ServiceNow when the Release pipeline checks in before the build pipeline.
    -   Incorrect message in inbound event processing details when test type mapping is missing.
    -   After historical import of pipeline executions that are canceled, pipeline status shows as in-progress in the pipeline UI
    -   Jenkins Orchestration events randomly go into an error state.
-   **Version 1.35.3 - September 2022**
    -   New
        -   Improved error messages to help you find the root cause of a problem while connecting to a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   You can now specify a particular MID Server directly on the DevOps Change workspace page while connecting to a tool.
-   **Version 1.35.0 - August 2022**

    GitHub Actions Integration:

    -   GitHub is a coding tool that is now updated to support the GitHub Actions orchestration capability in ServiceNow DevOps. You use the ServiceNow DevOps custom actions \(published to the GitHub Actions marketplace\) to integrate GitHub Actions pipelines and GitHub Environments.
    -   To update the data model, GitHub Actions Integration requires that GitHub is connected, configured, and that pipelines are discovered. GitHub Actions workflow run are paused and resumed using custom actions.
    The following custom actions are published to the GitHub repository:

    1.  ServiceNow DevOps Change
    2.  ServiceNow DevOps Test Report
    3.  ServiceNow DevOps Sonar
    4.  ServiceNow DevOps Register Artifact
    5.  ServiceNow DevOps Register Package
    Historical import and polling for ADO Artifacts:

    -   Import historical data for ADO artifacts by using the app-onboarding self-service catalog and periodic polling to fetch the data. The import framework helps onboard teams by fetching DevOps data into the instance without having to edit the pipeline or configure webhooks. The imported data provides insights into the root causes for complete change traceability, which helps to identify the root causes and areas of improvement
    Out-of-the-box change approval policy Risk Inputs and Reject Reasons:

    -   The base-system DevOps default change approval policy improves the change automation and approval policy. Policy conditions run against collected DevOps data to auto-reject, auto-approve, or defer for manual approval. The data could be metrics on commits, code coverage, test results, sonar scan results, risk inputs, and so on. The change approval policy is configurable. To help users quickly take corrective actions, rejection reasons are captured in the CHG work notes.
    Jenkins snippet generator:

    -   The Jenkins plugin for ServiceNow DevOps can generate DevOps scripted pipeline steps. This helps developers to adopt ServiceNow DevOps features quickly and to modify pipelines easily.
    Workspace DevOps Onboarding:

    -   Onboarding \(connecting to\) a tool is challenging because it involves several disconnected steps and can involve multiple personas. Workspace guides you through the onboarding process to enable Change automation outcomes. The workspace drives self-service. With this release, you can easily onboard the Azure DevOps, Jira, GitHub, and Jenkins tools.
    DevOps Insights Module in Workspace:

    Flow Metrics that show the value of work being delivered.

    Cycle Times,Throughput Distribution, Planned to Deploy Flow Time, and Work In Progress amounts.

    New change acceleration metrics that focus on the path to automation.

    Automated versus manual changes, Change policy decisions applied, ROI.

    Updated filtering capabilities include Service, Configuration Item, Products, and by-Date.

    Drill into data collected with a new tabbing design to keep you in the workspace.

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

