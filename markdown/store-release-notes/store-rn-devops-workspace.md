---
title: DevOps Workspace release notes
description: Version history for the ITSM DevOps Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Workspace release notes

Version history for the ITSM DevOps Workspace application on the ServiceNow Store.

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
-   **Version 6.0.0 - May 2025**
    -   New:
        -   Bitbucket cloud tool integration with ServiceNow.
        -   Integrate the Bitbucket Cloud coding tool with DevOps Change Velocity, enabling ServiceNow to connect, discover, import, and process real-time repository events.
        -   DevOps Workspace UI for simplified creation of custom tool integration with planning, coding and orchestration capabilities
        -   An intuitive DevOps Workspace UI to integrate a new custom tool across capabilities with basic know how of ServiceNow has been added. It offers easy navigation to the ServiceNow AI Platform for defining transformer or adapter rules or integrate the ability to do so within the workspace wherever applicable and embeds necessary documentation links and tooltips to bolster self-service.
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
        -   Enhanced manual DevOps change creation experience by enabling the association of work items directly
            -   Add work items data in a manually created DevOps change request in Service Operations Workspace for ITSM.
-   **Version 4.1.0 - August 2024**
    -   Improved the DevOps Change Workspace to support the following DevOps Change Velocity features:
        -   Changed:
            -   Enhanced journey to full change automation using models.
            -   Support reruns with GitHub Action.
            -   Support API\_KEY for Jira Server.
            -   Persist branch details in pipeline execution to determine commits from artifacts and packages.
        -   Removed:
            -   To make the Change - DevOps Implement flow of the DevOps model more suitable for DevOps changes, change tasks are no longer automatically created.
            -   The DevOps Change Request Minimal Automation Approval Flow and DevOps Change Request Advanced Automation Approval flows won't trigger for DevOps change requests whose model is a base system DevOps change model \(DevOpsorDevOpssimplified\) to avoid conflicts and errors.
            -   Note: For detailed information on the features, see the DevOps Change Velocity Release Notes.
-   **Version 4.0.0 - May 2024**
    -   Changed:
        -   Improved the DevOps Change Workspace to support the following DevOps Change Velocity features:
            -   Re-designed the Tools Module for better user-experience
            -   Support for custom orchestration tool integration
            -   Improved onboarding error handling and guardrails
            -   Allow change request creation even with errors in DevOps data retrieval
            -   GitLab merge request / pull request support
            -   JFrog Artifactory support for GitHub Actions, Azure DevOps, and GitLab
            -   Jira Cloud support
            -   Support multiple ServiceNow DevOps Configurations in the same Jenkins instance
            -   GitLab Docker Container improvements
-   **Version 3.1.0 - February 2024**
    -   New:
        -   GitHub Issues integration
            -   GitHub now supports the Plan capability with GitHub Issues integration in addition to the code and orchestration capabilities. GitHub Issues of the repository can also be discovered and linked with the GitHub commits and persisted in the ServiceNow DevOps CHG, which can be used for policy decisions of ServiceNow DevOps CHG acceleration.
            -   Supported various unit test types for GitHub Actions
                -   Automatically publish test results of various unit test tool reports like NUnit, pytest, jest, JUnit, XUnit without any custom API calls to publish to the ServiceNow DevOps CHG.
            -   Guided change automation experience
                -   Better in-product guidance is now provided on the various ways to leverage DevOps changes and how to easily adopt DevOps changes without complete disruption of your change process. A stepper guides you to automate DevOps change creation. You can check the connection status of a tool while selecting a pipeline on the stepper and you are also alerted before proceeding to the next step. Two new state transition flows: Change - DevOps - New and Change - DevOps Schedule, for DevOps change model are introduced to move and track changes through these states. The DevOpsChangeRelationshipHelper script has been introduced to retrieve data associated with a change request based on the specified relation type.
            -   Removal of Connection Admin and Flow Designer Role for DevOps Admin &amp; Tool Owner
                -   Visibility and editing capabilities of DevOps Admins and Tool Owners has been limited regarding connections and credentials by removing the Flow Designer and Connection Admin roles for these users.
            -   Changes to artifacts and packages:
                -   The overall experience with adoption, implementation, and error handling for artifacts and packages has been improved. The artifact and package registration API, for both Jenkins and ADO, now provides clear messaging in the response regarding the status. Users can see if the artifact version is already present, staged, or created and can also see the reason in case of a rejection. A clear message is available on the console along with a link to navigate to the artifact page. The DevOpsDPRHelper API now takes pipeline executions as an input to get data on vulnerabilities, test results, and code coverage. The troubleshooting experience has been improved by the addition of a description column that explains why an artifact version or package is pending. A new List module comprising of Artifact, Package, and Pending Packages lists has been created to improve ease of access to this information in the DevOps Change Workspace.
-   **Version 3.0.0 - November 2023**
    -   New:
        -   DevOps Homepage updates
            -   The DevOps Homepage is updated with a new getting started guide, enabling you to automatically create DevOps changes that follow your current change process. A new DevOps system property enables state transitions. Once a DevOps change request is created, the getting started guide is replaced with a steady state, which gives an overview of all your tools, applications, and change control enabled pipelines. The new metric section for tools makes it easy to identify any areas that need attention. The new application metric section to see what apps having the most activity. The new change automation section shows all the DevOps changes including the ones that are awaiting approval.
            -   Guided change automation experience
                -   Better in-product guidance is now provided on the various ways to leverage DevOps changes and how to easily adopt DevOps changes without complete disruption of your change process. A stepper guides you to automate DevOps change creation. You will see that the "DevOps Model Change Approval" and "DevOps Default Change Approval" flows are renamed as "DevOps Change Request Manual Approval" and "DevOps Change Request Advanced Automation Approval Flow" respectively and a new change approval flow "DevOps Change Request Minimal Automation Approval" is introduced. The UX clearly explains the intended outcome and behavior of each of the flows, and when to use which flow to achieve complete value incrementally.
            -   Connect to a Tool and App playbooks
                -   The tool playbook scope is reduced to support the tool owner role better. It now focuses on connecting to the tools having sufficient permissions and configuring webhooks to receive real-time data. The new Create application playbook guides the app owners to create a DevOps application, associate their plans, repositories, and pipelines, and importhistorical data.
            -   Tool connection and configuration status
                -   For Jenkins, GitHub, and Azure DevOps, the connection and configuration status indicators are updated. You can also easily test the tool connections.Overall Status of the tool is now updated as Connected, Disconnected, Needs Attention, based on the status of Connection Status, Tool Credentials, Permissions Check, Webhook Configuration Status.
            -   Automatically configure Jenkins
                -   The ServiceNow DevOps Jenkins plugin installed on the Jenkins tool can now be automatically configured directly from within DevOps Change Velocity application.
            -   Automated OAuth JWT setup to simplify GitHub OAuth JWT tool onboarding in playbook
                -   Several manual steps involved in onboarding GitHub tool using OAuth JWT credential are automated now in tool onboarding playbook, which makes the GitHub tool onboarding easier.
            -   Jenkins and GitHub test connection support
                -   Test GitHub webhook and Jenkins plugin configuration directly from DevOps Change Velocity. The Test connection button will provide an overall status of the tool.The Jenkins plugin can now be automatically configured from DevOps Change Velocity.
            -   Checkmarx support
                -   Connect Checkmarx that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results. This helps you determine how vulnerable your code is. Checkmarx scans that are configured on GitHub Actions, Jenkins, and Azure DevOps pipelines are supported in the base system. You can view the security scan results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance or in the Pipeline UI. You can use security results in defining change policies and conditions for change automation. Both Checkmarx One and Checkmarx SAST are supported.
    -   Fixed:
        -   Option to search for projects while configuring is added to Rally.
-   **Version 2.0.0 - August 2023**
    -   Changed:
        -   Workspace changes for onboarding and insights
        -   This includes validating the installation of ServiceNow DevOps extension in Azure DevOps before configuring webhooks, automatically importing pipeline steps when going through change automation setup, onboarding improvements, info icons for DevOps Insights widgets, and better visuals for flow and accelerate metric score widgets for DevOps Insights.
-   **Version 1.38.0 - May 2023**

    Changes to support capabilities added in DevOps Change Velocity 1.38.

-   **Version 1.37.0 - February 2023**
    -   Changed:
        -   DevOps Change Workspace changes
            -   Streamlined initial system setup for ServiceNow admins, which includes status of setup, improved identification of scope needed to complete, ability to set new passwords for account used for configurating credential alias, extra validation, and more.
            -   App Owner role expansion which includes the ability to modify pipeline steps to assign application services or to set up change automation. App owners can also click Discover for tools to associate any new objects needed for their DevOps application. Updated tool administration which includes the ability to easily update credentials for every tool and check permissions for the given credentials.
-   **Version 1.36.0 - November 2022**

    Fixed:

    -   Updated error messaging
        -   Improved error messages to help find the root cause of a problem while connecting to a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them. A new permission check when connecting a tool shows permissions available from the credentials instead of the required permissions.
    -   You can now specify a particular MID Server directly on the DevOps Change workspace page while connecting to a tool
    -   Pull Request \(PR\) pipeline executions support GitHub/Jenkins
        -   Track and support Pull Request pipeline executions for the Jenkins orchestration tool and PRs created in the GitHub coding tool. Integrate PR data like Pull Request ID, Commits, Origin branch, Destination branch, Raised by, Approver, Comments, PR raised time, PR approved time, and PR merged/closed time from the GitHub coding tool to the DevOps CHG created for the corresponding pipeline execution in the Jenkins orchestration tool. In addition, attach the PR-related data to the DevOps CHG to review who authorized, validated, verified, and approved the PR merge process.
    -   Import historical data for DevOps tools and CHG traceability - Gitlab
        -   Import historical data for Code and Orchestration capabilities by fetching data through the app-onboarding self-service catalog and periodic polling.
        -   The import framework helps to onboard teams by importing DevOps data into the instance without having to edit the pipeline or configure webhooks. The imported data provides insights into root causes for complete change traceability of Commits, Branches, Tags, and Pipelines \(both CI/CD\) from Gitlab.
    -   SonarQube - Support new code metrics
        -   Integrate New Code metrics provided by SonarQube scan results apart from the Overall code scan results, based on the New Code configuration in SonarQube. The following new code metrics are integrated in this release: New Vulnerabilities, New Maintainability Rating, New Reliability Rating, New Security Rating, New Bugs, New Code Smells, New Technical Debt, and New Lines of Code. This is supported for the Jenkins, Azure DevOps, and GitHub Actions orchestration tools.
    -   Split.io Feature Flag tool Integration with ServiceNow
        -   This integration extends ServiceNow to manage the CHG approval process for feature flags and segments of Split.io. ServiceNow DevOps can now manage updates to feature flags.
        -   Split.io feature flag tool integration support enables discovery of workspaces, environments, segments, and feature flags. You can set CHG request fields to enable Split.io for CHG control. Upon approval/rejection of a CHG request, the callback URL in split.io for the split or segment is invoked to resume implementation of the update to the split and segment
    -   You can now filter reports by Business Application on the DevOps insights dashboard.
    -   For the Jenkins integration, the minimum supported Jenkins version is now 2.289.1
    Changed:

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
    -   New:
        -   Improved error messages to help you find the root cause of a problem while connecting to a tool. Error messages identify relevant active problems, highlight specific issues, and explain how to mitigate them.
        -   You can now specify a particular MID Server directly on the DevOps Change workspace page while connecting to a tool.
-   **Version 1.35.0 - August 2022**
    -   DevOps Data Workspace is installed automatically as a dependency along with DevOps Insights when the new DevOps Change Velocity App is installed. Starting with release 1.31, whether you are upgrading an existing ServiceNow DevOps version or installing it new, install the DevOps Change Velocity app. DevOps Change Velocity simplifies and streamlines your DevOps install experience.
    -   Companies are turning to DevOps to speed up product delivery and innovation without compromising on quality. DevOps is integral to delivering differentiation, improving customer responsiveness, and building on your competitive advantage.
    -   ServiceNow DevOps is built on a powerful data model that connects your DevOps toolchain to the work and data already in the platform. One of several valuable outcomes is the ability to accelerate changes while ensuring effective and transparent risk management. This can make change management transparent to developers, improving their experience and helping to make them more productive by allowing them to stay in their preferred tools.
    -   This connected value stream supports the software factory in other ways like collecting, creating, and sharing insights through tailored dashboards. You have a complete chain from what is happening in production to the initial ideation or issue that caused a developer to start work. Code delivery becomes more reliable even with rapid iterations and, if incidents do arise, they can be resolved more quickly.

