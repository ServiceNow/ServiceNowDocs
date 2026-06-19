---
title: View and manage data from external tools
description: View and manage data coming from the DevOps application corresponding to your product that has been imported through external tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-manage-product-ext-tool.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# View and manage data from external tools

View and manage data coming from the DevOps application corresponding to your product that has been imported through external tools.

## Before you begin

Role required: sn\_dpr\_model.product\_manager

## About this task

This data coming from the external tools provide you with insights into the breakdown of product features into epics and their stories. This data also enables you to create and automate policies and determine whether the release meets the release exit criteria.

**Note:** The work item types that can be mapped to a product enhancement are controlled by the **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property. By default only epics are mapped; admins can extend this list to include other work item types. For more information, see [Digital Product Release properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/digital-product-release-properties.md).

The data also provides an overview of the software quality of your releases in the Release Quality dashboard. For more information, see [Release Quality dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-release-quality-dashboard.md).

This integration with external tools is accessible as part of the DevOps Change Velocity. For more information, see [DevOps Change Velocity integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-overview.md) and [Integrating DevOps Change Velocity with third party tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/integrating-devops-change-with-third-party-tools.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(\[Omitted image "dpr-icon-products.png"\] Alt text: Products and services icon.\).

3.  Select a product or service from the list to open.

4.  Select the **External tools** tab.

5.  Associate plans, repositories, and pipelines from the **Plans**, **Repositories**, and **Pipelines** tabs respectively.

    For more information, see [Associate tool objects to applications - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/apps-associate-objects-wkspc.md).

    **Note:** Only the **Plans** tab is available for services.

6.  To create product versions in DPR for each Release imported from ServiceNow® Agile Development 2.0, Fix Version imported from Jira, or Milestones imported from GitLab automatically, select the **Auto-create product versions from plan versions** option when associating plans from these planning tools.

    **Note:** This option is only available when you select only one record \(release, plan, or milestone\) for association. Make sure you have completed the mapping between the apps in DevOps and the products in DPR. For all new Releases created in Agile Development 2.0, Fix versions created in Jira, or Milestones created in GitLab for the associated plan, a product version and a corresponding release are automatically created in DPR.

7.  Select the **Artifact repositories** tab to associate an artifact repository to the product.

8.  Select the **Artifacts** tab to establish a relation between the artifacts and the product.

    When you create a release for the product, a relationship is established between the artifact version and the release so that policies can be run against the release.


**Parent Topic:**[Using Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-using-digital-product-release.md)

