---
title: GitHub Actions Workflows by Cloud Services Catalog
description: GitHub Actions workflows by Cloud Services Catalog uses automated Continuous Integration-Continuous Deployment \(CI/CD\) workflows to enable the rapid deployment of build requests to production environments.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Integrating GitHub Actions with Cloud-Services-Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# GitHub Actions Workflows by Cloud Services Catalog

GitHub Actions workflows by Cloud Services Catalog uses automated Continuous Integration-Continuous Deployment \(CI/CD\) workflows to enable the rapid deployment of build requests to production environments.

Cloud Services Catalog offers GitHub Actions release workflows as CI/CD tools that support the building, testing, and deployment of applications across various platforms and cloud providers throughout the development life cycle.

When used within Cloud Services Catalog, GitHub Actions offers expanded capabilities for version control management, work item tracking, project oversight, and reporting. Additionally, resource requests made through GitHub Actions workflows are subject to approval based on governance and confirmation procedures.

## Limitations

-   If a workflow includes a step that invokes another workflow, the process does not discover the inputs of the invoked workflow.
-   Step with approval: A workflow includes a step that waits for approval. Control over this step is not available.
-   The process does not discover repository secrets accessed by workflow steps.

**Parent Topic:**[Integrating GitHub Actions with Cloud-Services-Catalog](integrating-github-actions-with-cloud-service-catalog.md)

