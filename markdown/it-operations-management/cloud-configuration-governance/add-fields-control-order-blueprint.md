---
title: Add fields to a cloud catalog item order form
description: You can add fields to a cloud catalog form if you want the user to enter additional information beyond what a default blueprint provides.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-configuration-governance/add-fields-control-order-blueprint.html
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add fields to a cloud catalog item order form

You can add fields to a cloud catalog form if you want the user to enter additional information beyond what a default blueprint provides.

## Before you begin

-   You need a blueprint that you published to the catalog. The blueprint should be in the draft state. See [Build a Cloud Provisioning blueprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/create-blueprint-cmp.md) if you did not complete this prerequisite.
-   By default, cloud items appear in the Cloud Catalog, rather than the standard service catalog that comes with your instance. However, Blueprints utilize several features from the standard service catalog. It is suggested that you familiarize yourself with how the service catalog works. See  to get started.
-   Role required: sn\_cmp.cloud\_service\_designer

## About this task

Fields are represented as variables in blueprints. To add a field, you add a variable to an operation in the blueprint.

## Procedure

1.  Open a blueprint that you already created.

2.  Click the **Catalog** tab, and then click the operation, such as Provision, that you want to add the variable to.

    \[Omitted image "provision-operation-blueprint.png"\] Alt text: Provision operation

    The Cloud Catalog Item form opens.

3.  In the Variable Sets related list at the bottom, click the set in which you want the variable to belong.

    For example, click General Info, which is a default variable set for all blueprints, to have the field appear in the first tab on the catalog order form.

    The Variable Set form opens.

4.  In the Cloud Variables related list at the bottom, click **New**.

5.  Fill in the important form fields, such as:

    |Field|Description|
    |-----|-----------|
    |Type|Select the type of variable, such as **Single Line Text** for a text field, **CheckBox**, or **Date**, for example.|
    |Question tab|In **Question**, which is the value the user sees for the field on the catalog order form, enter a name. The **Name** field, which is the actual name of the variable, is automatically populated with the same value in lower case.|
    |Other tabs|Fill in other fields on the remaining tabs to control the field's visibility, form help text, default value, and access rights.|

    **Note:** This variable will not be available for orchestration. If you intend to use this variable for orchestration, please add it through Cloud Template or Blueprint instead.

    \[Omitted image "example-email-variable.png"\] Alt text: Example email variable

6.  Click **Submit**.

    The Variable Set form opens, showing the new variable in the Cloud Variables related list.

7.  To control the position of the field on the form, change the value in the **Order** column.

    **Note:** A lower order value moves the field higher up on the form, and vice versa.

    \[Omitted image "example-email-variable-order.png"\] Alt text: Example email variable order number

    In this example, the order is set to **1**, which means the Email address field appears after the Logical Datacenter field and before the Cloud Account field.

8.  On the form banner in the upper-left, click **Try It** to preview the order form as it would look to a user from the Cloud Catalog.

    The form appears with the new field that you created.

    \[Omitted image "example-email-address-field.png"\] Alt text: Email address field

9.  Click the back arrow on the upper-left of the form.

10. Toggle the catalog item to **Publish**.

    \[Omitted image "draft-published-slider.png"\] Alt text: Publish the blueprint


**Parent Topic:**[Form configuration with blueprints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/blueprint-form-configuration.md)

