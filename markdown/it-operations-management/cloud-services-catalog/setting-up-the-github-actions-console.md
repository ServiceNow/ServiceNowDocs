---
title: Set up the GitHub Actions workflow
description: Set up the GitHub Actions workflow as the first step before you run Discovery and order a catalog item in the Cloud Services Catalog application.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Integrating GitHub Actions with Cloud-Services-Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up the GitHub Actions workflow

Set up the GitHub Actions workflow as the first step before you run Discovery and order a catalog item in the Cloud Services Catalog application.

## Before you begin

Add a deploymentID variable to GitHub Actions workflows in the organization.

Setup the workflow with deploymentID run name, and tag all provisioned resources using the deploymentID key to enable resource discovery after provisioning.

Define all workflows using YAML configuration scripts with .yml or .yaml extensions stored in the .github/workflows directory of the repository. These scripts specify the automated workflow process including triggers, jobs, and steps.

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  Set up the workflow in GitHub with deploymentID, run name, and tag all provisioned resources using the deploymentID to enable resource discovery after provisioning.

2.  Generate a GitHub Personal Access Token \(Classic\) and store it securely.

    For more, see [Creating a Personal Access Token \(Classic](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic)


**Parent Topic:**[Integrating GitHub Actions with Cloud-Services-Catalog](../concept/integrating-github-actions-with-cloud-service-catalog.md)

