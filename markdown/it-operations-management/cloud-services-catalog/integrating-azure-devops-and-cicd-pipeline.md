---
title: Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline
description: You can process the release request from the Cloud Services Catalog workflow with Azure DevOps for end-to-end automation of the development process, including provisioning the resources, and deploying and monitoring the applications.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline

You can process the release request from the Cloud Services Catalog workflow with Azure DevOps for end-to-end automation of the development process, including provisioning the resources, and deploying and monitoring the applications.

The Azure DevOps and Continuous Integration-Continuous Deployment \(CI-CD tool\) pipeline integration is a release deployment process. You can use Cloud Services Catalog and the CI-CD tool to manage the deployed resources in Configuration Management Database \(CMDB\), directly through flows and actions.

## Benefits of Azure DevOps pipelines with Cloud Services Catalog

By using the Azure DevOps pipelines with Cloud Services Catalog, your organization gets the following benefits:

-   Ability to work with CI-CD pipelines regardless of the underlying languages that are used in the pipelines \(JavaScript, Java, Node.js, or Python\).
-   Support for all major version control systems such as GitHub, GitLab, Azure DevOps, Atlassian Bitbucket, or Team Foundation Version Control \(TFVC\).
-   Support for Amazon Web Services and Microsoft Azure Cloud services.
-   Ability to deploy the application anywhere \(on-cloud or on-premises, containers, or virtual machines\) or in any environment. For more information, see [ADO and Release and Life-cycle Management](../reference/ado-and-release-and-lifecycle-management.md).
-   Ability to deploy Kubernetes, Platform as a Service \(PaaS\), and so on, without any development change needs.
-   Automatic updates to CMDB through the required tags.
-   Approvals and governance steps that are built into the workflow.

Key steps in integrating Azure DevOps and CI-CD pipeline

1.  Use the release pipelines and Azure DevOps by Cloud Services Catalog.
2.  Set up the Microsoft Azure DevOps console.
3.  Run Discovery on Azure DevOps config provider.
4.  Order a Microsoft Azure DevOps catalog item.

-   **[Release pipelines and Azure DevOps by Cloud Services Catalog](release-pipelines-and-azure-devops-by-cloud-services-catalog.md)**  
Azure DevOps has release pipelines, such as the Continuous Integration-Continuous Deployment \(CI-CD\) pipelines, that offer a build, test, and deploy approach. You can use these fully automated processes to rapidly deploy build requests to the production environment.
-   **[Set up the Microsoft Azure DevOps console](../task/setting-up-azure-devops-console.md)**  
Set up the Microsoft Azure DevOps console as the first step before you run Discovery and order a catalog item in the Cloud Services Catalog application.
-   **[Run Discovery on Azure DevOps config provider](../task/running-discovery-on-ado-config-provider.md)**  
Add the Azure DevOps config provider and run Discovery to discover all projects, pipelines, and pipeline variables in an organization by using the Cloud Services Catalog application.
-   **[Order a Microsoft Azure DevOps catalog item](../task/azure-devops-pipeline-flow.md)**  
Provision the Microsoft Azure DevOps catalog by using the Microsoft Azure DevOps catalog order form in the Cloud Services Catalog application.

**Parent Topic:**[Configuring Cloud Services Catalog](configuring-csc.md)

