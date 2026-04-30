---
title: Control visibility default values for Cloud catalog items
description: Through blueprints, you can control how form fields appear to users in the cloud catalog. For example, you can control where the fields appear to users on the catalog item form, and whether they are read only or mandatory.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Control visibility default values for Cloud catalog items

Through blueprints, you can control how form fields appear to users in the cloud catalog. For example, you can control where the fields appear to users on the catalog item form, and whether they are read only or mandatory.

## Before you begin

Role required: admin

## Procedure

1.  Open the blueprint to modify, and then toggle it from **Published** to **Draft**.

2.  Click the **Catalog** tab.

    The Request Operation sub-tab opens and displays the published catalog items for the Provision operation.

3.  Click the **Provision** tile for the catalog item.

    The settings in the Provision operation control the form that the user sees upon initial request of the item, before it is provisioned.

    ![Catalog item](../image/request-operation-catalog-item.png)

    The Cloud Catalog Item form opens.

4.  In the Variable Sets related list at the bottom, click the set in which you want the variable to belong.

    For example, click **General Info**, which is a default variable set for all blueprints, to have the field appear in the first tab on the catalog order form.

5.  In the Variable Set form, select the variable that you want to modify.

6.  In the Cloud Variable form, complete any of the following actions.

<table id="choicetable_fwb_rfm_bfb"><thead><tr><th align="left" id="d403697e112">

To

</th><th align="left" id="d403697e115">

Action

</th></tr></thead><tbody><tr><td id="d403697e121">

**Make the field mandatory**

</td><td>

Select the **Mandatory** check box. Clear the check box to make the field optional.

</td></tr><tr><td id="d403697e133">

**Make the field read-only**

</td><td>

Click the **Availability** tab, and then select the **Read Only** check box. Clear the check box to make the field editable.Use this option to automatically populate a value in the field that the user cannot change.

</td></tr><tr><td id="d403697e151">

**Show or hide the field**

</td><td>

Click the **Availability** tab, and then select or clear the **Visible** check box.

</td></tr><tr><td id="d403697e166">

**Move the field to another tab**

</td><td>

Select a different **Variable set**. **General Info** and **Provision** are provided in the base system, and you can configure additional form UI groups. To add a new tab for organizing fields in the catalog item, see [Create a variable set for Cloud Provisioning and Governance](configure-ui-group.md).

</td></tr><tr><td id="d403697e193">

**Set a default value**

</td><td>

Click the **Default Value** tab and enter the value in **Default value**. If the field is not read-only, users can change the value on the cloud catalog form.Reference fields must use the Sys ID of the record that represents the default value.

</td></tr><tr><td id="d403697e211">

**Add help for the user**

</td><td>

Do any of the following: -   Click the **Question** tab, and add a value in the **Tooltip** field to show a bubble with the text when the user hovers the cursor over the field.
-   Click the **Annotation** tab, select **Show** help, and then enter values in the **Help text** or **Instructions** fields to display additional text to the user above the field.


</td></tr></tbody>
</table>7.  Click **Update**.

8.  Toggle the catalog item to **Publish**.

    ![Publish the blueprint](../image/draft-published-slider.png)


## Example

In this example, the Business Service field:

-   Is populated with the Email business service record from the cmdb\_ci\_service table based on the Sys ID of the record.
-   Is read-only so users cannot change it.
-   Is mandatory because it is considered necessary before the system can provision the virtual resource.
-   Contains help text to tell the user that the default selection is Email.

On the catalog order form, the field appears like this graphic: ![The Business Service field](../image/blueprint-example-business-service-catalog.png)

**Parent Topic:**[Form configuration with blueprints](../concept/blueprint-form-configuration.md)

