---
title: Idea Category Configuration form
description: Learn about the fields of the idea category configuration form. Use this form to create or edit the details of an idea category configuration in Innovation Management.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Form field information for Innovation Management, Innovation Management reference, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Idea Category Configuration form

Learn about the fields of the idea category configuration form. Use this form to create or edit the details of an idea category configuration in Innovation Management.

<table id="table_jzp_4ry_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category table

</td><td>

The parent table to derive idea categories from.

 To use static idea categories, select the default Idea Category \[im\_category\] table.

 To use dynamic idea categories, select an existing table. For example, to use department names as idea categories, select the table that contains details of all the departments.

</td></tr><tr><td>

Category Field

</td><td>

Field from the category table from which to derive the idea category. The corresponding value of this field in the category table is listed in the **Category** field on the Idea Portal.For example, to list department names as category options, set the value of this field to **Name**. The system searches for and fetches the department names from the parent table and lists all the department names as category options.

</td></tr><tr><td>

Parent Field

</td><td>

If you are using nested idea categories, specify the field in the category table to be used to fetch the parent category.**Note:** Leave this field blank if you are not using nested idea categories.

 For example, to list Department 1 and 2 as subcategories of Department A, set the value of this field as **Parent**. The system searches for and fetches values from the parent table and lists Department 1 and 2 as subcategories of Department A.

</td></tr><tr><td>

Module

</td><td>

The Idea module to which this idea category belongs.

</td></tr></tbody>
</table>**Parent Topic:**[Form field information for Innovation Management](form-field-information-for-innovation-management.md)

**Related topics**  


[Configure idea categories](../task/category-configuration-existing-table.md)

