---
title: Publish a blueprint as a cloud catalog item
description: You can create and publish a catalog item directly from a blueprint.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Publish a blueprint as a cloud catalog item

You can create and publish a catalog item directly from a blueprint.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

-   Starting with Orlando, Cloud Provisioning blueprints are available on instances upgraded from a previous release but you cannot create new blueprints. Resource profiles and custom-created blueprints will no longer be supported starting with the Australia release.
-   Use Cloud Provisioning cloud templates to create catalog items in place of blueprints. Cloud Provisioning [cloud templates](create-cloud-template.md) allow you to ingest Azure ARM, AWS CFT, Google Deployment Manager \(GDM\) and Terraform specification syntax in cloud catalog items to run your cloud deployment orchestration.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints**.

2.  Open a blueprint \(in draft mode\), click the **Catalog** tab, and then click **Create Catalog Item**.

    The Create Blueprint Catalog dialog box appears.

3.  Enter a name for the catalog item in the **Name** field and click **Save**.

    The catalog item is generated and appears in the **Catalog** tab.

4.  Click the catalog item to make any updates to the catalog item.

    The Cloud Catalog Item screen appears.

5.  Click **Update** to save the changes you made.


