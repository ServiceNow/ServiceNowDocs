---
title: Define release scope using product enhancements
description: Define the release scope of products and services by adding features, enhancements, and work items.​
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-product-release/dpr-manage-digital-product.html
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Define release scope using product enhancements

Define the release scope of products and services by adding features, enhancements,and work items.​

## Before you begin

Role required: sn\_dpr\_model.product\_manager

## About this task

Watch the following video to learn how release planning in Digital Product Release helps you define the scope of a release.

Release planning in Digital Product Release.  

**Note:** When a Plan Version from the DevOps data model is mapped to a Software Model in DPR, any Work Items associated with that Plan Version get automatically listed in the Release scope page. If a work item is associated with a product enhancement, it shows as a child under that product enhancement in the list. You can track these work items on the Release scope page of the release.

This option is available when you have selected the **Auto-create product versions from plan versions** while associating the product with a plan from ServiceNow® Agile Development 2.0, Jira, or GitLab.

The mappings between plan versions and software models are stored in the Plan Version to Software Models \(sn\_devops\_m2m\_plan\_version\_software\_model\) table. The mappings between work items and plan versions are stored in the Work Item to Release Versions \(sn\_devops\_m2m\_work\_item\_plan\_version\) table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(\[Omitted image "dpr-icon-products.png"\] Alt text: Products and services icon.\).

3.  Select a product or service from the list to open.

4.  Add features andenhancements to the product.

    -   [Add a product feature to a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-product-release/dpr-create-product-feature.md)
    -   [Add an enhancement to a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-product-release/dpr-create-product-enhancement.md)
    -   [Add a product enhancement from an epic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-product-release/dpr-add-product-enhancement-from-epic.md)

