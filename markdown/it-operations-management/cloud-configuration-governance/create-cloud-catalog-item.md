---
title: Create a cloud catalog item
description: Create a cloud catalog item for provisioning, based on a template or an existing blueprint, and publish the catalog item to provide a service.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a cloud catalog item

Create a cloud catalog item for provisioning, based on a template or an existing blueprint, and publish the catalog item to provide a service.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

While creating a catalog item, you can associate the catalog item with a template either native to the cloud provider \( for example, CFT, ARM, GDM\) or a Terraform IaC template. After you generate a catalog item, the system automatically generates components such as variable sets, lifecycle operations, rules, and pre- and post-provision operations. You can manage all these components from the Create Catalog Item page.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog items**.

    All the catalog items that you've created are listed in a card layout view. You can click an inactive catalog item to provision it.

2.  Click **New**.

    The Cloud Catalog Items screen appears.

3.  On the form, fill in the fields.

<table id="table_fkz_wtp_2fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the catalog item.

</td></tr><tr><td>

Active

</td><td>

Option for making the catalog item available. This check box can be selected only after you've selected a blueprint.

</td></tr><tr><td>

Icon

</td><td>

Image to appear as an icon beside the item name in the catalog. You can upload a 16 x16 pixel image. If no image is uploaded, the default icon appears beside this item. The uploaded image overwrites the default image. The image you upload appears in the service catalog; not in the ServiceNow® Cloud Provisioning and Governance application.

</td></tr><tr><td>

Picture

</td><td>

Image for the catalog item. The image that you select is displayed for the catalog item in the Cloud User Portal \(after you click **Launch a Stack**\).

</td></tr><tr><td>

Catalogs

</td><td>

Names of catalogs.

</td></tr><tr><td>

Category

</td><td>

Category for the item appears by default. You can change the category. Catalog searches find only items that are assigned to a category. The categories appear in the service catalog. The catalog item can appear in multiple categories. To add categories, click the **Categories** tab and then click **New** or **Edit**.

</td></tr><tr><td>

Source

</td><td>

Source type \(Cloud Template or Custom\) to associate the catalog item with.

</td></tr><tr><td>

Template type

</td><td>

-   Select **Cloud Template**, then select the type of template \(**ARM Template** or **CloudFormation Template**, to import cloud-native templates\)

-   Select **Configuration Management Template** to use Config Management provider templates from Anisible or Terraform.


</td></tr><tr><td>

Blueprint

</td><td>

If you selected **Custom** in the **Source** field, then select a blueprint to associate with the catalog item.

</td></tr><tr><td>

Blueprint Operation

</td><td>

The value in this field is automatically populated after you generate the catalog item. This field appears only when you select a blueprint.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the catalog item. This description appears in the Cloud User Portal next to the catalog item.

</td></tr><tr><td>

Description

</td><td>

Full description of the catalog item. This description appears in the service catalog; not in the Cloud Provisioning and Governance application. You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The catalog item and all associated components such as variable sets, lifecycle operations, and rules are generated and appear as tabs in the Cloud Catalog Item page.

    **Note:** If you selected **Template** from the Source type list, you must create a template and associate the template with the catalog item.

    The related links are actions that you can perform on the catalog item.

    |Action|Description|
    |------|-----------|
    |Export Catalog Item|Exports all the components \(such as blueprints, resource blocks, rules\) of the catalog item from one environment to the other. See [Moving Cloud Provisioning and Governance content across environments](../concept/move-content-intro.md).|
    |Item Diagnostic|Identifies possible issues with the catalog item data and configuration. See [Item diagnostic report](https://www.servicenow.com/docs/access?context=c_ItemDiagnostic&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|
    |Manage Attributes|See [Manage operation attributes](manage-attributes.md).|
    |Reset Catalog Item|Resets \(to the last change you made\) any customizations that you've made to the catalog item.|


## What to do next

[Create a cloud template-based catalog item](create-cloud-template.md).

**Related topics**  


[Create a catalog item from a Terraform template](catalog-item-terraform-template.md)

