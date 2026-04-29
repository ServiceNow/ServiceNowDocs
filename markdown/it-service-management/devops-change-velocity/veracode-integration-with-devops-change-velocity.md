---
title: Veracode integration with DevOps Change Velocity
description: Connect to your Veracode instance that is integrated with your CI/CD pipelines to retrieve security scan results. This helps you determine how vulnerable your code is.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Veracode integration with DevOps Change Velocity

Connect to your Veracode instance that is integrated with your CI/CD pipelines to retrieve security scan results. This helps you determine how vulnerable your code is.

## Veracode integration overview

Veracode scans that are configured on GitHub Actions, Jenkins, Azure DevOps, GitLab, and Harness pipelines are supported in DevOps Change Velocity.

Ensure that your Veracode credentials have the following API roles.

-   Upload and Scan
-   Results

For more information, see [Veracode documentation](https://docs.veracode.com/r/c_API_roles_details).

You can configure Veracode scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity. If you’re using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always. If you’re using Jenkins, and your pipeline already has a Veracode security scan step, you don’t have to add the custom action code in your pipeline. Ensure that your Veracode security scan step has waitForScan: true. This is required for the system to retrieve the scan information.

If you want to configure Veracode for the GitLab tool, you can either use the generic Docker container image to add the Veracode security step or perform the steps specified in the [Integrate security tools with GitLab](../task/configure-security-tool-for-gitlab.md) topic.

For Harness pipelines, you can configure Veracode scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).

You can view the security scan results either in the related list of a Change Request, or the Task Execution of the pipeline, or in the Pipeline UI in your ServiceNow instance. You can also use security results in defining change policies and conditions for change automation.

## Get started

You must install the DevOps Vulnerability Integrations \(sn\_devops\_vul\_ints\) and Vulnerability Response Integration with Veracode \(sn\_vul\_veracode\) plugins before connecting your Veracode instance to ServiceNow. For more information on activating a plugin, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:**

-   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
-   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.

For more information on the scan results captured in ServiceNow, see [Security scan results](../reference/security-tool-framework.md).

Use one of the following options to onboard Veracode. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Veracode to DevOps Change Velocity - Workspace](../task/onboard-veracode-to-devops-change-velocity-workspace.md)**  
Connect to your Veracode instance using the DevOps Change Workspace playbook.
-   **[Onboard Veracode to DevOps Change Velocity - Service Catalog](../task/onboard-veracode-to-devops-change-velocity-service-catalog.md)**  
Connect your Veracode instance using the ServiceNow Service Catalog.
-   **[Onboard Veracode to DevOps Change Velocity - Classic](../task/onboard-veracode-to-devops-change-velocity-classic.md)**  
Connect to your Veracode instance to retrieve scan results.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

