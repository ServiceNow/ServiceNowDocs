---
title: Edit the record producer for an HR catalog item
description: Edit the record producer for an HR catalog item to define the required fields and how the item appears in the HR service catalog to employees.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR catalog item configuration, HR service catalog management, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Edit the record producer for an HR catalog item

Edit the record producer for an HR catalog item to define the required fields and how the item appears in the HR service catalog to employees.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Manage HR Catalog**.

2.  Hover over the HR catalog item and click **Edit catalog item**.

    ![Edit the record producer for an HR catalog item](../image/edit-hr-record-producer-for-hr-catalog-item.png)

3.  Fill in the fields on the form, as appropriate.

<table id="table_sdb_sy2_r2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record producer.

</td></tr><tr><td>

Table name

</td><td>

HR case table that the record producer is associated with.**Note:** Make sure that the HR case table for the record producer matches that of the associated HR service.

</td></tr><tr><td>

Application

</td><td>

This field is automatically set to `Human Resources: Core`.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record producer for use.

</td></tr><tr><td>

Preview link

</td><td>

Link to preview how the HR catalog item appears to users in the HR service catalog.

</td></tr><tr><td>

Expand help for all questions

</td><td>

 

</td></tr></tbody>
</table>4.  In the **What it will contain**, **Accessibility**, and **Generated Record Data** related lists, fill in the fields as appropriate.

    You can provide a short description and description, configure a script, add images, define a template, and more.

5.  In the **Variables** related list, configure the variables for the HR catalog item as appropriate.

    Variables collect information from the user, and are used to ask questions and map answers to fields. You can add as many variables as you need to the HR catalog item. Commonly used variables types include:

    -   Checkbox
    -   Multiple Choice
    -   Reference
    -   Select Box
    -   Single Line Text
    To learn more about the different types of variables and how to configure them, see Types of service catalog variables.

6.  In the **Available For** and **Not Available For** related lists, configure the user criteria to apply to the HR catalog item as appropriate.

    User criteria controls which employees can access and request the HR catalog item in the HR service catalog. To learn more about user criteria and how they are used to control access to HR catalog items, see Set security for items and categories.

    **Note:** User criteria applied to the HR catalog item is employee-facing only, and has no relation to the HR criteria that is used to control what HR services an HR agent can request for an employee from the **Create New Case** module. See [Configure an HR service](configure-hr-service.md) for more information.

7.  Click **Update**.


**Parent Topic:**[HR catalog item configuration](../concept/hr-catalog-item-configuration.md)

**Previous topic:**[Create an HR catalog item](create-hr-catalog-item.md)

**Next topic:**[Edit the HR case template for an HR catalog item](edit-hr-case-template-for-hr-catalog-item.md)

