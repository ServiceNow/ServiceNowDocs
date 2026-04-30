---
title: Manage the Terraform template-based catalog items
description: Use an Infrastructure as Code \(IaC\) change task to create or update the Terraform template-based catalog items. The IaC change task helps ensure that the catalog items are aligned with the latest infrastructure specifications coded in the Terraform template.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Manage the Terraform template-based catalog items

Use an Infrastructure as Code \(IaC\) change task to create or update the Terraform template-based catalog items. The IaC change task helps ensure that the catalog items are aligned with the latest infrastructure specifications coded in the Terraform template.

## Before you begin

Role required: admin

## About this task

When the Cloud Services Catalog Terraform Connector app detects a change in the variables on the Terraform template \(.TF\) file or the metadata \(`metadata.snc`\) file, it creates change tasks. The change tasks are assigned to users who had created the catalog items \(user with \[sn.cmp.cloud\_service\_designer\] role\). Based on the change detected on the template variables or the metadata, the catalog item task prompts you take one of the following actions:

-   Create a catalog item from the modified template version.

    A new catalog item is created with the existing catalog item name appended by a number. For example, if the existing catalog item is called `Linux VM` the new catalog item will be created with the name `Linux VM1`

-   Update the existing catalog item per the updated template version.

    When you choose to update the existing catalog item per the updated template version, a new version of the template is created and activated while the existing template version is retired and rendered inactive.


**Note:** The name of the Terraform config provider should match between the environments, while exporting Terraform template based catalog items. For example, if the config provider is called TFE in dev environment, it should be named the same, TFE, in the target environment \(UAT, prod, etc.\) too.

Until you perform one of the above mentioned actions, the catalog item is deactivated. When the catalog item is in deactivated state, cloud users can’t access it.

The Cloud Services Catalog Terraform Connector creates an IaC change task for a Terraform template-based catalog item when any one of the following conditions is met:

-   One or more variables are added to the source Terraform template.
-   One or more variables are deleted from the source Terraform template.
-   One or more variables used in the source Terraform template undergo a data type change.
-   Default value of one or more variables changes.

**Note:** Deprovisioning the impacted stack triggers de-provisioning at the cloud provider's end.

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    The Cloud Admin Portal opens in a new browser tab.

2.  Navigate to **IaC** &gt; **Change Tasks**.

3.  Open the appropriate change task.

4.  Customize the new or updated variables detected in the Terraform template.

    1.  Select the **Customize Variables** related link.

    2.  Edit the default value of the new or updated Terraform variables from the Terraform Task Metadata related list.

        **Note:** The default value mentioned in the variable record of the Terraform Task Metadata related list overrides the default value mentioned in the Terraform template.

5.  Select the **changes** link on the recommendation message to view a difference comparison in the template content, as detected by IaC Discovery.

6.  On the form, fill in the fields.

    For more information, see [Cloud Services Catalog Terraform Connector Terraform Catalog Item Task form reference](../reference/cpg-terraform-connector-catalog-item-task-form.md).

7.  Select **Update**.


**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../concept/using-ccg-terraform-connector.md)

