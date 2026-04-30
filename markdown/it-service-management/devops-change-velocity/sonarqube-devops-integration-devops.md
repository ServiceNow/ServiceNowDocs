---
title: SonarQube integration with DevOps Change Velocity
description: Connect to your SonarQube instance that is integrated with your CI/CD pipelines to retrieve code quality and code security results.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# SonarQube integration with DevOps Change Velocity

Connect to your SonarQube instance that is integrated with your CI/CD pipelines to retrieve code quality and code security results.

## SonarQube integration overview

Sonar scans that are configured on GitHub Actions, Jenkins, and Azure DevOps pipelines are supported in DevOps Change Velocity. Both SonarCloud and SonarQube \(on-premises\) are supported.

You can view the code quality and code security summary results either in the related list of a Change Request or the Task Execution of the pipeline in your ServiceNow instance. You can also use code quality and code security results in defining change policies and conditions for change automation.

DevOps Change Velocity captures both overall and new code metrics.

## Get started

You can onboard your Sonar instance using an admin or a non-admin Sonar PAT. To enable a non-admin user for onboarding, perform the following steps.

1.  Navigate to **All** &gt; **DevOps** &gt; **Administration** &gt; **Properties**.
2.  Enable the **DevOps Non-Admin Software Quality Summary Flag** property by selecting the **Yes** option.

On the SonarQube side, the following permissions are required.

-   **Admin PAT**

    Project-level access to your SonarQube instance to configure scans for all your projects.

-   **Non-admin PAT**
    -   Browse permission for GitHub, GitLab, and Azure DevOps pipelines, and Execute Analysis permission for Jenkins for the projects \(both private and public\) on which the scan is run.
    -   A branch must be created in SonarQube before a non-admin user retrieves data into ServiceNow. For more information, see [Branch Analysis](https://docs.sonarqube.org/latest/analyzing-source-code/branches/branch-analysis/).

        **Note:** You can set up branch analysis to enable SonarCloud to analyze branches in your projects apart from the main branch. You can’t set up or perform branch analysis on SonarQube community edition licenses. Upgrade to SonarQube Developer or Enterprise editions to set up branch analysis on SonarQube on-premises implementations.


Sonar custom action and extension are available in the GitHub and Azure DevOps marketplace respectively. For Jenkins, the Sonar scan results are retrieved using ServiceNow Jenkins plugin.

For more information on the scan results captured in ServiceNow, see [Software Quality Results](dev-ops-software-quality-results.md#).

Use one of the following options to onboard SonarQube. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard SonarQube to DevOps Change Velocity — Workspace](../task/sonar-connect-workspace.md)**  
Connect to your Sonar instance using the DevOps Change Workspace playbook.
-   **[Onboard SonarQube to DevOps Change Velocity — Service Catalog](../task/sc-sonar.md)**  
Connect your Sonar instance using the ServiceNow Service Catalog.
-   **[Onboard SonarQube to DevOps Change Velocity — Classic](../task/create-sonar-tool-devops.md)**  
Connect to your Sonar instance to retrieve scan results.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

