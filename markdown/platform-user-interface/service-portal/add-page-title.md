---
title: Add dynamic titles to a page
description: Create variables to generate descriptive titles depending on the content loaded into a page.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add dynamic titles to a page

Create variables to generate descriptive titles depending on the content loaded into a page.

## Before you begin

Role required: admin

## About this task

**Note:** The dynamic titles don’t apply to the knowledge article view page in the Knowledge Management Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  Open a page.

3.  Add one or more variables to the **Dynamic page title** field.

    Depending on the available URL parameters and the dynamic title you would like to define, you can add the following types of values:

    |Value types|Description|Example value|
    |-----------|-----------|-------------|
    |One URL parameter variable|Generates a page title using the associated record of one URL parameter.|`%first_name`|
    |More than one URL parameter variable|Generates a page title using the associated records of multiple URL parameters.|`%first_name %last_name`|
    |Static value and a URL parameter variable|Generates a page title using a static value and the associated record of a URL parameter.|`Employee: %first_name`|

    Enter the variables in the intended syntax of the title. For example, to have an employee's name and title separated by a hyphen, you would enter `%first_name - %title`. In the page title, this syntax would render as something like "Beth - System Administrator".

4.  Click the **Dynamic page variables** related list tab.

5.  Click **New** to create a new variable.

6.  On the form, fill in the fields.

    Associate a field with a URL query parameter. When the value of the query parameter is used to display content, a field from the same record is used to generate the title. You can define the field to generate the title through the **Table field** field.

<table id="table_acv_cff_51b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Variable to store the value. Must begin with **%** and cannot contain spaces. This value must match one of the variables defined in the **Dynamic page title** field.

</td></tr><tr><td>

Application

</td><td>

Application scope of the page. This value is read-only.

</td></tr><tr><td>

Page

</td><td>

Page to apply the dynamic variable to.

</td></tr><tr><td>

URL query parameter

</td><td>

URL parameter to indicate the record that is being displayed. You can enter any string.**Tip:** To create a URL parameter that is meaningful and easily identifiable, use a field name from the record. For example, to refer to a knowledge article, you can enter `number` to reference the article by its number.

</td></tr><tr><td>

Relevant table column

</td><td>

Table field to match the URL query parameter. For example, if you entered `number` to reference a knowledge article by its number, select **Number**. If left blank, the system uses the record sys\_id.

</td></tr><tr><td>

Table

</td><td>

The source table of the URL query parameter record.

</td></tr><tr><td>

Table field

</td><td>

Field from the table defined in the **Table** field. This field is used to generate the dynamic page title.

</td></tr></tbody>
</table>    If more than one dynamic page variables match a variable defined in the **Dynamic page title** field, the record with the latest Updated date is used.

    Variables with same name aren't supported and won't be created multiple times. Each variable should be unique.

    ![A completed dynamic page title variables form that populates the page title with a user's title.](../image/dynamic-var.png)

    In this example, the value of the Title field in the User \[sys\_user\] table populates the page title. The `%title` variable must also be defined in the **Dynamic page title** field in the page record.

7.  Click **Submit**.


## Result

When the page loads, the record defined in the URL query parameter displays. The field defined in **Table field** determines the title of the page.

**Parent Topic:**[Improving search engine optimization for portals](../concept/seo-sp.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](t_ConfigureAPage.md#)

