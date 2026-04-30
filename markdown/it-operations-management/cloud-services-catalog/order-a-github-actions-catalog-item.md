---
title: Provision a GitHub Actions workflow using Cloud Services Catalog
description: Provision the GitHub Actions catalog by using the GitHub Actions catalog order form in the Cloud Services Catalog application.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 1
breadcrumb: [Integrating GitHub Actions with Cloud-Services-Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Provision a GitHub Actions workflow using Cloud Services Catalog

Provision the GitHub Actions catalog by using the GitHub Actions catalog order form in the Cloud Services Catalog application.

## Before you begin

Role required: cloud\_service\_user

## About this task

You can use the GitHub Actions workflow deployment form to call a GitHub Actions workflow and run it via a ServiceNow catalog item for deployment.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Cloud Services** &gt; **GitHub Actions**.

2.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |User Group|User group that is assigned to the user.|
    |Schedule Time Zone|Time zone used for resource scheduling.|
    |Aws Region|AWS region where cloud resources are provisioned.|
    |Bucket Name|Name of the S3 bucket to create \(must be lowercase, no spaces\).|
    |Choose Service Account|Service account specified in the workflow template for authentication and discovery.|
    |Choose Cloud Location|Region specified in the template used for resource discovery.|


## Result

Verify that a blueprint approval policy \(CSC Content Approval Policy GitHub Actions Integration\) is applied on the GitHub Actions catalog. This policy mandates that an approval must be obtained from the Change management group before any provisioning can take place.

**Parent Topic:**[Integrating GitHub Actions with Cloud-Services-Catalog](../concept/integrating-github-actions-with-cloud-service-catalog.md)

