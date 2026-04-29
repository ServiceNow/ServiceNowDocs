---
title: Create enterprise models
description: Create a model based on a top tier Enterprise Asset Management model category. Use models to manage and keep track of your assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise models, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create enterprise models

Create a model based on a top tier Enterprise Asset Management model category. Use models to manage and keep track of your assets.

## Before you begin

You can create a model based on any of the following Enterprise Asset Management model categories:

-   Construction
-   Medical
-   Transportation
-   Industrial
-   Facility
-   Retail
-   Tactical equipment
-   Wearable
-   Multimedia production equipment
-   Pallet

**Note:** Only consumables created from models in the Enterprise Asset Management application can be used if the **Asset strategy tracking** for the model is set to **create consumable asset**.

**Note:** The Enterprise Asset Management application supports only facilities models that fall under the Facility model \[sn\_ent\_facility\_model\] child class of the Enterprise good model \[sn\_ent\_model\] class. The application does not support facilities models that are listed in the Facility Models \[cmdb\_facility\_product\_model\] table.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterptrise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise model management**

2.  Select the tab for the model type that you want to create.

    -   Select the **All enterprise** tab for all available enterprise model types.
    -   Select the tab for a specific enterprise model type, such as **Facility**, **Industrial**, **Medical**, **Retail**, or **Transportation**.
    -   Select the **All models** tab for pallet models.
3.  Select **New**.

    If you are creating a pallet model, select **New pallet model**.

    If you select **New** on any tab other than the **All models** tab, a dialog box opens, prompting you to specify the type and category of the new model that you are creating. Proceed to [step 4](create-model-eam.md#dialog-box) to fill in the fields in the dialog box.

    If you select **New pallet model** on the **All models** tab, you are automatically redirected to the Create New Product Model page. Proceed to [step 6](create-model-eam.md#create-new-product-model-form) to fill in the fields on the page.

4.  In the dialog box, fill in the fields.

<table id="table_vt2_t5z_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type**Note:** This field appears only if you selected **New** on the **All enterprise** tab.

</td><td>

The type of model you want to create. Choose from the following options:-   Enterprise Good Model
-   Construction Model
-   Facilities Model
-   Industrial Model
-   Medical Model
-   Retail Model
-   Transportation Model
-   Tactical Equipment Model
-   Wearable Model


</td></tr><tr><td>

Model category

</td><td>

The category that the model belongs to.

</td></tr></tbody>
</table>5.  Select **Create**.

    The Create New Product Model page appears. The model is in **Build** status by default and the model category is a read-only field set to the category that you chose. You can change the status only after you have saved the model record.

6.  On the form, fill in the details.

    For a detailed description of the fields, see [Model fields for Enterprise Asset Management](../reference/eam-model-fields.md).

7.  Select **Save**.

    The model is created along with the related tabs such as **Model Components**, **Assets**, **Enterprise Model Lifecycles**, **Compatibles**,**Substitutes**, and **Vendor Catalog Items**. You can perform additional configuration on the model by entering details in the related tabs.

8.  Change the status of the model to **In Production** once you are done configuring the model.

9.  Select **Publish to Enterprise Asset Catalog** to publish your model to the Service Catalog.**Publish to Enterprise Asset Catalog** appears only when you change the status of the model to **In Production**.

    Enterprise models can be deleted only by the sn\_eam.enterprise\_admin role.

10. You may select **Update risk** if you updated the model's risk scores and want to propagate the updated scores to the associated assets too.

    After the **EAM - Update model risk values to asset** scheduled job is completed, the risk values for all the assets associated with this model is updated.


**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

