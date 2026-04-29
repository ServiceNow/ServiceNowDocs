---
title: Configure variables in a record producer for appointment booking
description: Create specific variables in a Service Catalog record producer to capture essential details such as location and contact information when users book appointments.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure variables in a record producer for appointment booking

Create specific variables in a Service Catalog record producer to capture essential details such as location and contact information when users book appointments.

## Before you begin

Role required: appointment\_booking\_admin

Ensure you have an existing Service Catalog record producer to configure.

## About this task

By configuring catalog item variables for appointment booking, you can:

-   Clearly prompt users to specify accurate details like location and contact, ensuring efficient scheduling.
-   Ensure appointment details are precise and complete, reducing errors or rescheduling.
-   Simplify the booking process by guiding users with clearly defined variables and questions.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Click the desired record producer.

3.  In the **Variable** related list, click **New**.

4.  On the form, fill in the fields.

5.  <table id="table_t54_b3k_lzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

\(Read-only\) Automatically populated based on the application scope.

</td></tr><tr><td>

Type

</td><td>

Choose a supported variable type.If you use unsupported variables, Service Catalog might not integrate the data in the right format.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item that uses the variable.

</td></tr><tr><td>

Order

</td><td>

Define the display order of variables. Lower values appear first.For example, a variable with an order value of 1 is placed ahead of other variables with higher-order values.

</td></tr><tr><td>

Active

</td><td>

This is a read only field and is enabled based on the Publish, Retire, or Edit actions.

</td></tr><tr><td>

Mandatory

</td><td>

Select if users must provide a response when requesting the service.

 **Note:** You can adjust this dynamically through client scripts or APIs.

</td></tr><tr><td>

Question

</td><td>

Question that you can ask users ordering the catalog item, to obtain related information. For example, "Enter appointment location".

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the Question field for all variable types except Break, Container Split, and Container End.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when users point to the variable. Enter a brief note to describe the purpose of the question.

</td></tr><tr><td>

Example Text

</td><td>

Question field hint that appears before a user enters a value. You can use a hint for the following variables:-   Email
-   URL
-   Single Line Text
-   Multi Line Text
-   Wide Single Line Text


</td></tr><tr><td>

Type Specification

</td><td>

Provide additional information or configuration specific to the selected variable type.

</td></tr></tbody>
</table>6.  Click **Submit**.

7.  Repeat steps 3 through 5 to create additional variables for the same catalog item record producer.


## Result

The service catalog record producer creates the new variable record in the selected table.

## What to do next

After creating your variables, link them to the Appointment Booking table so they appear correctly in the booking calendar interface. For more information, see [Create a business rule to automatically generate appointment records from catalog item variables](create-business-rules-to-automatically-create-appointment-record.md)

