---
title: Configure a record producer for an HR service
description: Make an existing HR service available for employee self-service by adding it to the HR service catalog.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure a record producer for an HR service

Make an existing HR service available for employee self-service by adding it to the HR service catalog.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

To avoid creating duplicate services, do not create a new HR catalog item. Instead, configure a record producer to link your existing HR service to the HR service catalog. For optimal performance, use one record producer per HR service.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Open the HR service.

3.  Open the record producer for that service.

    **Note:** To create a new record producer for the HR service, click the **Lookup** icon, and then click **New**.

    ![Open the record producer for the HR service.](../image/record-producer-for-hr-service.png)

4.  Fill in the fields on the form, as appropriate.

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
</table>5.  In the **What it will contain**, **Accessibility**, and **Generated Record Data** related lists, fill in the fields as appropriate.

    Since you are configuring the record producer from the HR service form, make sure to:

    1.  In the **What it will contain** related list, provide the following script:

        ```
        new sn_hr_core.hr_ServicesUtil(current, gs).createCaseFromProducer(producer, cat_item.sys_id);
        ```

    2.  In the **Accessibility** related list, set the **Catalogs** field to **Human Resources Catalog**.

6.  In the **Variables** related list, configure the variables for the HR catalog item as appropriate.

    Variables collect information from the user, and are used to ask questions and map answers to fields. You can add as many variables as you need to the HR catalog item. Commonly used variables types include:

    -   Checkbox
    -   Multiple Choice
    -   Reference
    -   Select Box
    -   Single Line Text
    To learn more about the different types of variables and how to configure them, see [Types of service catalog variables](https://www.servicenow.com/docs/access?context=r_VariableTypes&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

7.  In the **Available For** and **Not Available For** related lists, configure the user criteria to apply to the HR catalog item as appropriate.

    User criteria controls which employees can access and request the HR catalog item in the HR service catalog. To learn more about user criteria and how they are used to control access to HR catalog items, see [Set security for items and categories](https://www.servicenow.com/docs/access?context=c_ServiceCatalogAccessControls&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    **Note:** User criteria applied to the HR catalog item is employee-facing only, and has no relation to the HR criteria that is used to control what HR services an HR agent can request for an employee from the **Create New Case** module. See [Configure an HR service](configure-hr-service.md) for more information.

8.  Click **Submit** or **Update** on the record producer form.

9.  Click **Update** on the HR service form.


**Parent Topic:**[HR service configuration](../concept/hr-service-configuration.md)

**Previous topic:**[Configure an HR case template](configure-hr-case-template.md)

**Next topic:**[HR service catalog management](../concept/hr-service-catalog-management.md)

