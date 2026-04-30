---
title: Journey designer header configuration fields reference
description: Journey designer headers can be configured for different journeys so that the different users can have a unique view for their role in the journey.
locale: en-US
release: xanadu
product: Journey Designer
classification: journey-designer
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Journey designer reference, Journey designer, HR Service Delivery, Employee Service Management]
---

# Journey designer header configuration fields reference

Journey designer headers can be configured for different journeys so that the different users can have a unique view for their role in the journey.

## Heading Configuration

**Note:** The **Heading Configuration** must be created before heading fields can be added.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Configuration name**

</td><td>

The name of the header configuration.

</td></tr><tr><td>

**Persona**

</td><td>

Journeys have 3 personas. Each persona has its own header configuration.-   **Employee**: The person for whom the journey is created.
-   **Journey owner**: The person who creates the journey. Managers create and modify journeys for their employees.
-   **Mentor**: The person identified to help the employee complete a journey. A mentor's permission may include the ability to add other mentors and edit a journey.

</td></tr></tbody>
</table>## Heading Configuration Fields

Heading fields have default labels for the name of each field. Labels are displayed to users in the journey. Add custom labels to make user visible labels meaningful to the user.

For example:

|Custom label|Table name|Field name|
|------------|----------|----------|
|**Journey publish date**|Journey Accelerator Plan \[sn\_ja\_plan|**start\_on**|
|**Mentor**|Journey \[sn\_jny\_journey\]|**mentors**|

<table id="table_ypn_cqh_ytb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Custom label**

</td><td>

A custom label is visible to the users who are part of the journey.

</td></tr><tr><td>

**Display order**

</td><td>

A label's display order is used in the user interface to identify how the label is displayed.

</td></tr><tr><td>

**Field name**

</td><td>

The default name of a field that is given to the label identified in a table.

</td></tr><tr><td>

**Table name**

</td><td>

The name of the table that contains the field names and custom labels used in the user interface. The header fields for journeys are in these tables.-   Journey Accelerator Plan Header Field \[sn\_ja\_plan\]
-   Journey \[sn\_jny\_journey\]

 A journey header configuration can have labels identifies in multiple tables.

</td></tr></tbody>
</table>**Parent Topic:**[Journey designer reference](jny-dsnr-reference.md)

