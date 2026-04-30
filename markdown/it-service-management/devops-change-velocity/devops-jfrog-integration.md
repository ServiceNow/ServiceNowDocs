---
title: JFrog integration with DevOps Change Velocity
description: Connect to your JFrog instance to track artifacts published to JFrog from pipeline executions in Jenkins, GitHub Actions, Azure DevOps, and GitLab.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# JFrog integration with DevOps Change Velocity

Connect to your JFrog instance to track artifacts published to JFrog from pipeline executions in Jenkins, GitHub Actions, Azure DevOps, and GitLab.

For Jenkins, you must activate the Jenkins Artifactory plugin in your Jenkins server to generate the artifacts as part of your pipeline run and publish them in the JFrog artifact repositories.

**Note:** Historical import of JFrog artifacts is not supported. You can import JFrog artifacts that are built by Jenkins using the Service Catalog import historical data process. For more information, see [Importing historical data for DevOps tools](import-historical-data-devops-catalog.md#). Discover and configure is also not supported for JFrog.

## Get started

Use one of the following options to onboard JFrog. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard JFrog to DevOps Change Velocity — Workspace](../task/devops-jfrog-connect-workspace.md)**  
Connect to your JFrog instance using the DevOps Change Workspace playbook to track artifact repositories published to JFrog.
-   **[Onboard JFrog to DevOps Change Velocity — Service Catalog](../task/sc-jfrog.md)**  
Connect your JFrog instance using the ServiceNow Service Catalog.
-   **[Onboard JFrog to DevOps Change Velocity — Classic](../task/devops-jfrog-create-tool.md)**  
Connect to an instance of the JFrog artifact tool to enable you to track artifacts published to JFrog.
-   **[Integration with JFrog AppTrust application](integration-with-jfrog-apptrust-application.md)**  
Integrate DevOps Change Velocity with JFrog AppTrust applications to automate change request creation, approval, and evidence collection as application versions are promoted through life-cycle stages.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

