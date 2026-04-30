---
title: Customize and manage Journey Accelerator plan headers
description: Create customized plan headers for different plan types based on user roles.
locale: en-US
release: xanadu
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating and managing audience-specific Journey Accelerator templates, Install and configure Journey Accelerator, Journey Accelerator, HR Service Delivery, Employee Service Management]
---

# Customize and manage Journey Accelerator plan headers

Create customized plan headers for different plan types based on user roles.

## Before you begin

Role required: admin

## About this task

Journey Accelerator plans use three different roles:

-   Manager
-   Employee
-   Mentor

You can customize the plan header for each role. Customizations include role-based permission, customizing field labels, and setting role-based plan preferences. Plan header fields are available in the Journey Accelerator Plan \[sn\_ja\_plan\] table.

## Procedure

1.  Navigate to **All** &gt; **Journey Accelerator** &gt; **Manage Plan Header Configuration** and click **Default for employee**.

    The default header configuration for the employee role has these fields configured:

    -   **Plan created by**
    -   **mentor**
2.  Click **mentor**.

3.  In the **Custom label** field, enter `buddy` to replace mentor.

    **Note:** A custom field header can only be used for one mentor field. You can customize the mentor field for either **Mentor can view** or **Mentor can edit**.

4.  Click **Update** to save the changes to the mentor field.

5.  Click **Update** again to save the changes to the header configuration.

    The text **This person's mentor** is changed to **This person's buddy**. This change applies to only the header view of the employee role. Field labels are unique to each role.

    The changes are available to use in Journey Accelerator Plan Types.


**Related topics**  


[Create and manage Journey Accelerator plan types](create-manage-ja-plans.md)

