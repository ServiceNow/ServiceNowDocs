---
title: Create a logical connection model
description: Create a logical connection model in the ServiceNow Telecommunications Network Inventory application to define the metadata for the different logical connections. In the logical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-logical-connection-models.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create a logical connection model

Create a logical connection model in the ServiceNow Telecommunications Network Inventory application to define the metadata for the different logical connections. In the logical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a logical connection model record, it creates a model in the Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory Models** &gt; **Logical Connection Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the common information for the logical connection model.

    The following table lists the fields that are unique to the logical connection form.

<table id="table_xxp_hq1_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the logical connection model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the logical connection model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(\[Omitted image "search.png"\] Alt text: Search icon.\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Manufacturer-assigned name of the logical connection model that is specified by the model manager.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the general section information for the logical connection model.

    **Note:** To learn more about the fields, see [Inventory Model form - General](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-model-form-general.md).

6.  On the **Details** tab, fill in the information section for the logical connection model.

    To learn more about the fields, see [Inventory Model form - Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-model-form-information.md).

7.  To add the compatible models, select **Add Compatible**.

    You can personalize the list of compatibles table by using the gear \(\[Omitted image "Personalize\_1.png"\] Alt text: Personalise icon.\) icon.

    **Note:** In the classic environment, this function is available only for administrators.

8.  To add the substitute logical connection models, select **Add Substitution**.

    You can track the network interface models that you use to substitute another network interface model with.

    **Note:** In the classic environment, this function is available only for administrators.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachment icon.\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/additional-tabs-of-inventory-models.md).

11. To delete a model, select the options icon \(\[Omitted image "options-icon.png"\] Alt text: Options icon.\) next to the **Save** button, and select **Delete**.


**Parent Topic:**[Create inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-inventory-models-tni.md)

