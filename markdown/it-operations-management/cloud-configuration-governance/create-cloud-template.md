---
title: Create a cloud template-based catalog item
description: Create a cloud template and associate the template with a catalog item. Once you've created a template, you can reuse the template to create additional catalog items for the services you want to provision.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a cloud template-based catalog item

Create a cloud template and associate the template with a catalog item. Once you've created a template, you can reuse the template to create additional catalog items for the services you want to provision.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

You can create a template by uploading a generic template file, importing a template from a public URL, or by copying and pasting the contents of an existing template. AWS CloudFormation \(CFT\) templates support JSON and YAML. Azure Resource Manager \(ARM\) templates support JSON. The following public template URL content types are supported:

-   Text/Plain
-   Application/JSON
-   YAML MIME

**Note:** Catalog items that were based on templates in earlier releases are now treated as if they are based on blueprints.

You can update a template as often as needed. With each update, a new version of the template is created. A template can be in one of three states: **draft**, **active**, or **history**. When you create a template and do not activate it, the template is in a draft state. Once you activate the template, the state changes to active. If you create another template and activate it, the state of the previous active template turns into history. At any time, only one template is in the active state. Each time you activate a template, the previous active template becomes history.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items** and then create a catalog item or open an existing catalog item.

2.  Click **Cloud Templates** &gt; **New** and then enter a meaningful short description in the **Short description** field.

3.  Specify the **Ingestion method**.

<table id="choicetable_nck_fyq_cgb"><tbody><tr><td id="d281561e139">

**Import from URL**

</td><td>

Import a template by specifying a public URL where the template resides. Select this option and then click the lock icon \(![Lock image](../image/icon_lock.png)\) to unlock the **Cloud template URL** field. Enter the public URL in this field.**Note:** For the public URL, we support only HTTP and HTTPS protocols, and do not support FTP. Ensure that the size of the template does not exceed the default value of 3 MB. You can change the default value of the file size by changing the value in the **sn\_cmp.template\_content\_size\_supported\_inbytes** property in the sys\_properties table. Enter the file size in bytes. There's also a default time-out of five minutes for an HTTP request. You can change the time-out value in the **sn\_cmp.template\_url\_import\_http\_timeout** property in the sys\_properties table. Enter the new value in milliseconds.

</td></tr><tr><td id="d281561e166">

**Upload a file**

</td><td>

Upload a template from your local workstation.

</td></tr><tr><td id="d281561e175">

**Use template body**

</td><td>

Paste the contents of the template file in the **Body** field.

</td></tr></tbody>
</table>    After you specify the **Ingestion method**, the template is validated and the results appear in the **Validation status** and **Validation message** fields.

4.  Click **Submit**.

    The template is created and the Cloud Catalog Item page opens.

5.  If this is the first version of template, skip this step else on the **Cloud Templates** tab, open the template \(currently in Draft state\) to view the template version parameters.

    **Note:** The first version of a template that you create and publish has no conflict issues. If you update the template, a conflict can arise. If a parameter **Action Type** has the value **Update**, then specify a value for **Decision**.

    ![Template version parameters](../image/template-parameters.png)

6.  Open each parameter with a **Decision** value of **Pending**, select a value, and then click the check mark ![Check mark](../image/icon-check-mark.png).

<table id="choicetable_o1l_h5r_cgb"><tbody><tr><td id="d281561e266">

**Skip Update**

</td><td>

Discards the updates to the template.

</td></tr><tr><td id="d281561e275">

**Use template**

</td><td>

Applies the updates to the template.

</td></tr></tbody>
</table>7.  After you update each **Pending** decision, click **Activate**.

    The state of the template changes from **Draft** to **Active** and the system generates the catalog item.


