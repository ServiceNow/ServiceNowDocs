---
title: Define release scope using product enhancements
description: Define the release scope of products and services by adding features, enhancements, and work items.​
locale: en-US
release: yokohama
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-04-25"
reading_time_minutes: 1
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Define release scope using product enhancements

Define the release scope of products and services by adding features, enhancements,and work items.​

## Before you begin

Role required: sn\_dpr\_model.product\_manager

## About this task

**Note:** When a Plan Version from the DevOps data model is mapped to a Software Model in DPR, any Work Items associated with that Plan Version get automatically listed in the Release scope page. If a work item is associated with a product enhancement, it shows as a child under that product enhancement in the list. You can track these work items on the Release scope page of the release.

This option is available when you have selected the **Auto-create product versions from plan versions** while associating the product with a plan from ServiceNow® Agile Development 2.0, Jira, or GitLab.

The mappings between plan versions and software models are stored in the Plan Version to Software Models \(sn\_devops\_m2m\_plan\_version\_software\_model\) table. The mappings between work items and plan versions are stored in the Work Item to Release Versions \(sn\_devops\_m2m\_work\_item\_plan\_version\) table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(![Products and services icon.](../image/dpr-icon-products.png)\).

3.  Select a product or service from the list to open.

4.  Add features andenhancements to the product.

    -   [Add a product feature to a product or service](dpr-create-product-feature.md)
    -   [Add an enhancement to a product or service](dpr-create-product-enhancement.md)
    -   [Add a product enhancement from an epic](dpr-add-product-enhancement-from-epic.md)

