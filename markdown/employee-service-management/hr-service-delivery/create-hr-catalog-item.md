---
title: Create an HR catalog item
description: Create an HR catalog item so that employees can request the HR service directly from the HR service catalog through a self-service portal such as the Employee Service Center. When you create a new HR catalog item, a corresponding HR service, record producer \(synonymous to HR catalog item\), and HR case template are automatically created.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HR catalog item configuration, HR service catalog management, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an HR catalog item

Create an HR catalog item so that employees can request the HR service directly from the HR service catalog through a self-service portal such as the Employee Service Center. When you create a new HR catalog item, a corresponding HR service, record producer \(synonymous to HR catalog item\), and HR case template are automatically created.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Manage HR Catalog**.

2.  Select a category.

3.  Click **New Catalog Item**.

    **Note:** The COEs available to you may differ depending on the HR package you have.

    -   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
    -   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](../concept/hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
    -   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
    -   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.
4.  Fill in the fields on the form.

<table id="table_kcl_v54_n2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR catalog item.

</td></tr><tr><td>

Short description

</td><td>

Short description of the HR catalog item.

</td></tr><tr><td>

Case type

</td><td>

Name of the HR Center of Excellence \(COE\) that the corresponding HR service and record producer are categorized under. **Note:** The COEs are organized around functional disciplines and are extensions of the HR Case \[sn\_hr\_core\_case\] table. To learn more, see [HR service categorization](../concept/hr-service-categorization.md).

</td></tr><tr><td>

Topic Category

</td><td>

Name of the HR topic category that the corresponding HR service and record producer are categorized under.**Note:** The HR topic category is the first-level of categorization for HR services. To learn more, see [HR service categorization](../concept/hr-service-categorization.md).

</td></tr><tr><td>

Topic Detail

</td><td>

Name of the HR topic detail that the corresponding HR service and record producer are categorized under.**Note:** The HR topic detail is the second-level of categorization for HR services. To learn more, see [HR service categorization](../concept/hr-service-categorization.md).

</td></tr><tr><td>

Assignment group

</td><td>

Default assignment group of the HR catalog item.

</td></tr><tr><td>

Priority

</td><td>

Default priority of the HR catalog item.

</td></tr></tbody>
</table>5.  Click **Submit**.

    **Note:** If you click **Publish**, the HR catalog item will be available for employees to request in the HR service catalog.


## What to do next

The creation of an HR catalog item automatically creates a corresponding HR service, record producer \(synonymous to HR catalog item\), and HR case template. Configure the record producer and HR case template before you publish the HR catalog item to the HR service catalog.

**Parent Topic:**[HR catalog item configuration](../concept/hr-catalog-item-configuration.md)

**Previous topic:**[HR catalog item configuration](../concept/hr-catalog-item-configuration.md)

**Next topic:**[Edit the record producer for an HR catalog item](edit-hr-record-producer-for-hr-catalog-item.md)

