---
title: Checkmarx integration with DevOps Change Velocity
description: Connect to your Checkmarx instance that is integrated with your CI/CD pipelines to retrieve security scan results. This helps you determine how vulnerable your code is.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Checkmarx integration with DevOps Change Velocity

Connect to your Checkmarx instance that is integrated with your CI/CD pipelines to retrieve security scan results. This helps you determine how vulnerable your code is.

## Checkmarx integration overview

Checkmarx scans that are configured on GitHub Actions, Jenkins, Azure DevOps, GitLab, and Harness pipelines are supported in DevOps Change Velocity.

Two Checkmarx tools can be integrated with DevOps Change Velocity, which are Checkmarx One and Checkmarx SAST. For more information, see [Checkmarx One](https://checkmarx.com/resource/documents/en/34965-68518-introduction.html) and [Checkmarx SAST](https://checkmarx.com/resource/documents/en/34965-46311-checkmarx-sast-overview.html) documentation.

Ensure that your Checkmarx SAST user has a role that has permissions to read **Project** and **Scan Results** to get summary details. For more information, see [Checkmarx documentation](https://checkmarx.atlassian.net/wiki/spaces/KC/pages/1178009601/CxSAST+CxOSA+Roles+and+Permissions+v9.0.0+and+up). Ensure that your Checkmarx One user has the **create-scan** and **manage-project** roles to access Scan summary details. For more information, see [Checkmarx documentation](https://checkmarx.com/resource/documents/en/34965-68603-managing-roles.html).

**Note:** If you are integrating with Checkmarx One, you can retrieve only Static Application Security Testing \(SAST\) scans but not Software Composition Analysis \(SCA\) scans.

You can configure Checkmarx scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity. If you’re using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always. If you’re using Jenkins, and your pipeline already has a Checkmarx One security scan \(checkmarxASTScanner\) step, you don’t have to add the custom action code in your pipeline. For Checkmarx SAST, the custom action code must be added in your pipeline even if it has the security scan step \(checkmarxASTScanner\).

If you want to configure Checkmarx for the GitLab tool, you can either use the generic Docker container image to add the Checkmarx security step or perform the steps specified in the [Integrate security tools with GitLab](../task/configure-security-tool-for-gitlab.md) topic.

For Harness pipelines, you can configure Checkmarx scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using generic Docker container image](servicenow-custom-actions-for-gitlab.md).

You can view the security scan results either in the related list of a Change Request, or the Task Execution of the pipeline, or in the Pipeline UI in your ServiceNow instance. You can also use security results in defining change policies and conditions for change automation.

## Get started

You must install the DevOps Vulnerability Integrations \(sn\_devops\_vul\_ints\) and Checkmarx One Vulnerability Integration \(x\_chec3\_chexone\) or Checkmarx CxSAST Vulnerability Integration \(x\_chec3\_cxsast\) plugins before connecting your Checkmarx instance to ServiceNow. For more information on activating a plugin, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.

For more information on the scan results captured in ServiceNow, see [Security scan results](../reference/security-tool-framework.md).

Use one of the following options to onboard Checkmarx. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Checkmarx to DevOps Change Velocity - Workspace](../task/onboard-checkmarx-to-devops-change-velocity-workspace.md)**  
Connect to your Checkmarx instance using the DevOps Change Workspace playbook.
-   **[Onboard Checkmarx to DevOps Change Velocity - Service Catalog](../task/onboard-checkmarx-to-devops-change-velocity-service-catalog.md)**  
Connect your Checkmarx instance using the ServiceNow Service Catalog.
-   **[Onboard Checkmarx to DevOps Change Velocity - Classic](../task/onboard-checkmarx-to-devops-change-velocity-classic.md)**  
Connect to your Checkmarx instance to retrieve scan results.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

