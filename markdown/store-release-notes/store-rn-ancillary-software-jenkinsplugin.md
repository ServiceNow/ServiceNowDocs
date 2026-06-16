---
title: Jenkins plugin for ServiceNow DevOps release notes
description: Version history for the Jenkins plugin for ServiceNow DevOps in ancillary software on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ancillary-software-jenkinsplugin.html
release: store
topic_type: reference
last_updated: "2024-05-09"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Ancillary software release notes, ServiceNow Store release notes]
---

# Jenkins plugin for ServiceNow DevOps release notes

Version history for the Jenkins plugin for ServiceNow DevOps in ancillary software on the ServiceNow Store.

**Note:** Starting with version 1.33, the Jenkins plugin for ServiceNow DevOps will be released on the Jenkins marketplace. See the [Jenkins marketplace](https://plugins.jenkins.io/servicenow-devops/) for more information.

## Version history

-   **Version 4.0.0 - May 2024**
    -   New:
        -   Multiple ServiceNow DevOps configurations in the same Jenkins instance.
        -   Configure multiple ServiceNow DevOps connections in one Jenkins Server.
    -   Changed:
        -   Improved onboarding error handling and guardrails.
        -   View improved error messages which helps you find the root cause of a problem while onboarding \(connection, discover, configure, or import\) a tool.
        -   Change request creation with errors in DevOps data retrieval.
        -   Enable change request creation even if there is an error in retrieving the DevOps data in a pipeline.
-   **Version 3.1.0 - February 2024**
    -   New: Improved error logging and handling with ServiceNow DevOps extensions:
        -   ServiceNow DevOps extensions published for the Jenkins plugin now have improved error logging and handling for easier troubleshooting.
        -   Changes to artifacts and packages:
            -   The overall experience with adoption, implementation, and error handling for artifacts and packages has been improved. The artifact and package registration API, for Jenkins, provides clear messaging in the response regarding the status. Users can see if the artifact version is already present, staged, or created and can also see the reason in case of a rejection. A clear message is available on the console along with a link to navigate to the artifact page. The DevOpsDPRHelper API now takes pipeline executions as input to get data on vulnerabilities, test results, and code coverage. The troubleshooting experience has been improved by the addition of a description column that explains why an artifact version or package is pending.
            -   LogRecorder has been changed to be compatible with the latest versions of Jenkins.
    -   Fixed:
        -   Security events are stuck in a waiting state for Jenkins pipelines which run inside a folder.
        -   Security fix.
-   **Version 3.0.1 - November 2023**
    -   New:
        -   Automatic update of close code based on overall pipeline execution status:
            -   The Change created from a pipeline is now automatically closed and updated with the closure notes, and actual start/end time based on the overall pipeline completion status. This is controlled by a configuration flag which can be passed in as the attribute in the CHG creation step or via the configuration in the pipeline level in DevOps Change Velocity.
        -   Tool connection and configuration status:
            -   For Jenkins, the connection and configuration status indicators are updated. You can also easily test the tool connections.Overall Status of the tool is now updated as Connected, Disconnected, Needs Attention, based on the status of Connection Status, Tool Credentials, Permissions Check, Webhook Configuration Status.
        -   Checkmarx support:
            -   Connect Checkmarx that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results. This helps you determine how vulnerable your code is. Checkmarx scans that are configured on Jenkins pipelines are supported in the base system. You can view the security scan results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance or in the Pipeline UI. You can use security results in defining change policies and conditions for change automation. Both Checkmarx One and Checkmarx SAST are supported.
        -   Automatically setup Jenkins configuration from ServiceNow
    -   Fixed: Window Server had a compatibility issue with Jenkins
    -   Changed:
        -   Refactor: snDevOpsConfigGetSnapshots - Add an option for changeset that returns the latest deployable snapshots, if no deployables are impacted.
        -   Refactor: snDevOpsConfig - Handles multiple data formats.
        -   Refactor: snDevOpsConfigUpload - Add auto delete option
-   **Version 2.0.0 - August 2023**

    Changed:

    Secure token authentication support.

    Fixed:

    Security fix.

-   **Version 1.38.0 - May 2023**

    Changes:

    -   Logging change status while pipeline is pending decision to resume execution
        -   Change information such as, Change Number, State, Assignment Group, Approvers, Planned Start/End date is displayed in the console logs of Jenkins and GitHub Actions, while the pipeline/workflow is pending for change approval. The ServiceNow DevOps application is polled at regular intervals and if there is any difference in the change information, it is logged directly in the console logs, thereby minimizing the hops to ServiceNow instance.
-   **Version 1.37.0 - February 2023**

    Changes:

    -   Get and update DevOps Change Request details
        -   Get and update change request details associated with a Jenkins pipeline by running the snDevOpsGetChangeNumber and snDevOpsUpdateChangeInfo scripts respectively in the Jenkins pipeline.
    Fixed:

    -   Jenkins Discover fails with large number of pipelines/jobs.
-   **Version 1.35.2 - September 2022**

    Multi-branch pipeline support when registering a changeset or snapshot to a pipeline execution \(requires DevOps Config\).

-   **Version 1.35.0 - August 2022**

    Jenkins snippet generator: Jenkins plugin for ServiceNow DevOps supports the generation of DevOps scripted pipeline steps. This helps developers to adopt ServiceNow DevOps features quickly and modify the pipelines easily.

-   **Version 1.32 - November 2021**
    -   Changed: Support for parallel stages: ServiceNow DevOps will now track stages that run in parallel/nested in Jenkins pipelines. The parallel stages will be rendered accurately in the Pipeline User Interface, and automated Change Requests will only get created once parallel stages preceding it are complete
    -   Fixed:
        -   Multibranch pipelines with BitBucket configuration has task execution value as empty
        -   Pipeline executions are created even though Track is NOT enabled for multibranch pipeline and nested pipeline
        -   After recreating Jenkins tool, inbound events are created even though pipelines are not discovered or tracked
-   **Version 1.31 - October 2021**

    Changed: Automatic Change Control enablement for Jenkins: When DevOps Change Control has been enabled in a Jenkins pipeline, the corresponding step in ServiceNow will automatically have Change Control enabled. This improvement works with the Self-service Onboarding feature to simplify and streamline the onboarding process.

-   **Version 1.30 - September 2021**
    -   Fixed:
        -   Security fixes related to Jenkins plugin dependencies
        -   Notification stuck in the waiting state for multibranch pipelines that has branch name with special characters \(e.g. scratch/dev!@@&amp;mybranch\)
-   **Version 1.28.0 - July 2021**
    -   Fixed:
        -   Improved security, you can now use API keys to create to Jenkins tool in ServiceNow DevOps
        -   The change request rejected/cancelled reason is sent back to the respective Jenkins pipeline so that you will know why the change was rejected/cancelled.
-   **Version 1.27.0 - June 2021**

    Fixed: SonarQube support: Out-Of-the-Box support for Jenkins. Whenever there is a scan triggered from the pipeline, the scan results are captured in ServiceNow DevOps that is needed to determine change risk

-   **Version 1.24.0 - March 2021**
    -   Fixed:
        -   Change request pipeline API changes:
            -   Set additional change request attributes when creating the change request from Jenkins and Azure DevOps pipelines Set flag from pipeline so ServiceNow DevOps will not close the change request
-   **Version 1.23.0 - February 2021**
    -   Fixed:
        -   Jenkins pipeline under DevOps change resumes automatically after restart of Jenkins server.
        -   Jenkins global tool configuration username/password are stored as plain texts in config.xml.
        -   Jenkins pipeline fails if pipeline has not been discovered.
-   **Version 1.20.2 - January 2021**
    -   Fixed:
        -   Security fix
        -   If Pipeline has not been discovered, the Jenkins plugin behavior can fail
-   **Version 1.20.1 - December 2020**

    Fixed: This includes a fix for Jenkins unable to communicate to ServiceNow Instance will not proceed the snDevOpsChange function stage. And can be overridden with Ignore Error property.

-   **Version 1.20.0 - November 2020**

    New: Jenkins test result processing - This feature makes it possible for DevOps to store and process test results as part of the standard job notification rather than requiring an explicit call for that purpose. It also adds flexibility for handling test results of varying formats.

-   **Version 1.19.0 - October 2020**

    Fixed: ServiceNow automatically tracks Jenkins step events so snDevOpsStep function is no longer required when configuring the pipeline.

-   **Version 1.15.0 - June 2020**
    -   Fixed: Jenkins proxy server settings are now honored in outbound calls.
    -   NOTE: The new DevOps Integrations App must be installed to use the ServiceNow DevOps Jenkins integration: https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/ca1a857cc72600108c2c02b827c260df
-   **Version 1.12.0 - April 2020**
    -   New: Steps to set up in the SAP system:
        -   The new DevOps Integrations App must be installed to use the ServiceNow DevOps Jenkins integration
        -   Refer to https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/ca1a857cc72600108c2c02b827c260df

