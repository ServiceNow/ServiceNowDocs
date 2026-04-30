---
title: Add a workplace service item to a workplace service
description: Configure a workplace item that an employee can order along with a workplace service request or as part of the reservation. For example, while making a reservation, an employee can order a workplace service item such as catering, an additional chair, whiteboard, marker, and more.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Add a workplace service item to a workplace service

Configure a workplace item that an employee can order along with a workplace service request or as part of the reservation. For example, while making a reservation, an employee can order a workplace service item such as catering, an additional chair, whiteboard, marker, and more.

## Before you begin

Role required: sn\_wsd\_case.manager

## About this task

Add a workplace item to make it available for employees to order when they make a workplace service request. Specify the following details related to the workplace item:

-   Specify a name for the workplace item. The item is displayed to the employees with the specified name.
-   Select a template to prefill certain values when creating a workplace case or a workplace task.
-   The parent workplace service to which you’re adding the workplace item.
-   The subcategory to which the item belongs.
-   An image describing the workplace item. The image is displayed to the employees while they’re making a selection. The image is displayed to the customers while using the Reservation portal and Workplace Reservations for Microsoft Outlook Add-in.
-   A brief description about the workplace item. The description is displayed to the employees while they’re making a selection. You can add a normal text or an HTML text. The description can contain a text and a link. If you enter a long description, the text is displayed to the employees along with a **Show more** option. The description is displayed to the customers while using the Reservation portal and Workplace Reservations for Microsoft Outlook Add-in.

    **Note:** The Workplace Reservations for Microsoft Outlook Add-in doesn't inform about the services in lead time instead the services aren’t requested when the reservation gets submitted.

-   Cost of the workplace item. You can select the applicable currency based on your location.
-   Time duration required to prepare the item and clean up the item. You can specify the time in days and or hours.
-   Specify if you want to enable employees to specify their required quantity or capacity.
-   Configure the locations where the workplace service item shall be available.

Example: Workplace service items added with 'Request Furniture' workplace service:![Workplace service items added with 'Request Furniture' workplace service.](../image/wcasemgmt-workplceserviceservice-itemsl.png)

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service to which you want to add a workplace service item.

3.  On the form, scroll down to the Workplace Service items related list.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_pwz_4tl_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the workplace service item.

</td></tr><tr><td>

Item type

</td><td>

Type of workplace service activity that must be generated for this workplace service item when an employee makes an order. Choices are as follows:-   **Case**: Option to generate a child workplace case to fulfill this item.
-   **Task**: Option to generate a child workplace task to fulfill this item.
-   **Manual**: Option to generate a manual fulfillment workplace service to fulfill this item.


</td></tr><tr><td>

Workplace service

</td><td>

The workplace service that you want to set as a child case to fulfill the item. This field appears only if **Case** is selected from the **Item type** field.

</td></tr><tr><td>

Task table

</td><td>

The task table that must be used to create a child workplace task to fulfill the item. This field appears only if **Task** is selected from the **Item type** field.

</td></tr><tr><td>

Default template

</td><td>

The default task template to fulfill the task. For more information, refer to [Create a Workplace task template](wsd-task-template.md). This field appears only if **Task** is selected from the **Item type**.

</td></tr><tr><td>

Application

</td><td>

Application of the service item. This field is automatically set. -   If you’re adding the workplace service item for a workplace case-related service, select**Workplace Case Management**.
-   If you’re adding the workplace service item for a workplace service that is available for employees while making a reservation, then select **Workplace Reservation Management**.


</td></tr><tr><td>

Parent service

</td><td>

The workplace service to which you’re adding this activity. This field is automatically set.

</td></tr><tr><td>

Sub Category

</td><td>

Sub category to which the workplace item belongs. A list of subcategories is available from which you can select.

</td></tr><tr><td>

Active

</td><td>

Option to activate the workplace service item.

</td></tr><tr><td>

Image

</td><td>

Image describing the workplace service item. The image is displayed to employees while making a selection.

</td></tr><tr><td>

Description

</td><td>

Brief description about the workplace service item. The description can be in a normal text or an HTML text.The description is displayed to Workplace Reservation Management users while making a selection. The description can contain a text and a link. The description is displayed to the customers while using the Reservation portal and Workplace Reservations for Microsoft Outlook Add-in.

</td></tr><tr><td>

Quantity enabled

</td><td>

Option to enable users to specify their required quantity from **Default Configuration**.

</td></tr><tr><td>

Capacity enabled

</td><td>

Option to enable employees to specify a capacity from **Default Configuration**. The maximum capacity that is specified for the selected workplace location is used as the maximum capacity limit. To specify a maximum capacity, change the **Max capacity** field of the workplace service item location.**Note:** If the Workplace Service item isn't assigned to any location, there are no capacity restrictions.

</td></tr><tr><td>

Cost

</td><td>

Cost of the workplace item. To specify the currency of the cost, select the currency icon \(![Currency icon.](../image/currency-icon.png)\) from **Default Configuration**.

</td></tr><tr><td>

Preparation duration

</td><td>

Time required to prepare the item, if needed.

</td></tr><tr><td>

Cleanup duration

</td><td>

Time required to clean up the item, if needed.

</td></tr><tr><td>

Lead time for ordering

</td><td>

Time provided for the service team for preparing or arranging the service item. Configuring **Lead time for ordering** restricts in adding any extra service items to a reservation, when the service is within the lead time.This option is enabled at service item and service location level.

If a user changes the date of a reservation or a case and the new date is within the lead time, the system displays an error specifying the lead time of the service item. Service items that are within the lead time can't be modified while editing a reservation.

</td></tr><tr><td>

Restrict cancellation of requested services

</td><td>

Option to restrict employees to cancel the requested services.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

The workplace service item is added to the workplace service. An employee can order the workplace item while requesting the workplace service.

**Important:** While adding a service item to a reservation, if the item is within the lead time, then that service item doesn't appear in the items list.

A regular employee can’t remove any service items to an existing reservation in the following scenarios:

-   When a reservation is arranged
-   When the service items are within the **Lead time of ordering**
-   When the **Restrict cancellation of requested services** option is enabled

Employee can move a reservation to another date or time. While moving, if one or more services collide with the Lead time for ordering, then the employee is informed.

The employee shouldn't be able to remove any services that are being prepared or arranged.

The employee is informed if there are one or more services in the lead time while saving the reservation.

**Note:** Canceling a reservation cancels the requested service, even when the service item is restricted from cancellation.

## What to do next

Specify the workplace locations where the workplace service item is available for ordering. For more information, see [Make a workplace service item available to a workplace location](add-workplace-service-item-to-workplace-locs.md).

