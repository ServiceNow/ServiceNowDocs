---
title: Extend user criteria
description: Extend the user criteria table when the available user criteria fields are not sufficient. User criteria references various user fields \(fields from the User \[sys\_user\] table\), such as department, company, and groups. You can extend user criteria with a custom field to include any other user reference field \(field from the User \[sys\_user\] table\) of interest.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set security for items and categories, Service Catalog security, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Extend user criteria

Extend the user criteria table when the available user criteria fields are not sufficient. User criteria references various user fields \(fields from the User \[sys\_user\] table\), such as department, company, and groups. You can extend user criteria with a custom field to include any other user reference field \(field from the User \[sys\_user\] table\) of interest.

## Before you begin

Role required: admin

## About this task

For example, you can extend user criteria to include the user's cost center, and then restrict certain catalog items only to members of that cost center.

Meet the following rules to extend the user criteria table.

-   The field to add must be a reference field in the user record.
-   The field added to the user criteria table must be **List** type.
-   The fields must have matching names. For example, **cost\_center** \[sys\_user\] and **u\_cost\_center** \("u" prefix is added to custom fields in a table\) are considered to be matching.

This example demonstrates how to extend the current user criteria record to include **Cost center** as an option.

![User criteria record that you want to add cost center to](../image/user-criteria-b4-extended.png "User criteria record before extending Cost center")

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the **User Criteria** record.

3.  In the **Table Columns** related list, click **New**.

4.  Set the type to **List**, and then enter `Cost center` as the column label.

    The **Column name** field populates with **u\_cost\_center**.

5.  In the Reference Specification form section, select **Cost Center** for the reference field.

6.  Add any conditions or additional information to the dictionary entry as desired.

7.  Click **Submit**.

8.  Navigate to **Service Catalog &gt; Catalog Definition &gt; User Criteria**.

9.  Select or create a user criteria record, and see that you can now use the new field.


## What to do next

Test the user criteria record by navigating to **Service Catalog** &gt; **Catalog Definition** &gt; **User Criteria**, and opening any record. Verify that the extended field is available.

![The Cost center field is in the user criteria record](../image/user-criteria-extended.png "User criteria with cost center")

You can extend the User \[sys\_user\] table if there are fields in other tables that you want considered in user criteria. After extending the User table, follow the steps in this procedure to extend it to user criteria.

**Parent Topic:**[Set security for items and categories](../concept/c_ServiceCatalogAccessControls.md)

