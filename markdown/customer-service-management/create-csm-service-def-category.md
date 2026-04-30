---
title: Create a service definition category
description: Create a service definition category record in the Customer Service Management \(CSM\) application. Then use the category to create logical groupings of service definitions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a service definition category

Create a service definition category record in the Customer Service Management \(CSM\) application. Then use the category to create logical groupings of service definitions.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

A category can have one or more associated service definitions and a service definition can belong to multiple categories.

When an agent is using the case type selector to create a case, they can select a category before selecting a service. The category acts as a filtering mechanism and reduces the number of available services.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definition Categories**.

2.  From the Service Definition Categories list, select **New**.

3.  In the **Name** field, enter a name for the category.

    The category name can be up to 60 characters in length.

4.  In the **Description** field, add a description of the category.

    The description can be up to 4000 characters in length.

5.  In the **Order** field, add an order number for the category.

    The order value determines the order in which the categories are displayed in the case type selector and case task type selector. The category with the lowest value is displayed first.

    The default value is 100. You do not have to set an order value for a category. If a category does not have a value, the system displays the category in the case type selector in alphabetical order.

6.  Enable the **Active** check box.

    This field is enabled by default.

7.  Select **Submit**.

    The category is added to the Service Definition Categories list.

    Upon save, the new category record includes the Service Definition Category Relationships related list, which shows the service definitions associated with the category.


## Result

After creating a service definition category, you can [associate service definitions with the category](service-def-category-associate-service.md). These associated service definitions are stored in the Service Definition Category Relationships related list.

