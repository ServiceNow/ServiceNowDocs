---
title: Customized profile information
description: As part of designing the HR processes, you can customize the way HR profile information is processed. Keep in mind that some of the fields that appear are referenced from the User \[sys\_user\] table.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR Profile, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Customized profile information

As part of designing the HR processes, you can customize the way HR profile information is processed. Keep in mind that some of the fields that appear are referenced from the User \[sys\_user\] table.

If you have the sn\_hr\_core.admin role, you can customize HR profile information.

## Extend profile information

You can collect more profile information in a separate table. For example, you can create a Dependents table that extends the HR Profile \[hr\_profile\] table.

Because profile information is sensitive and confidential, the system administrator cannot view it. For more information, see [HR profile and HR case security](c_HRProfileSecurity.md).

## Associate profiles with user records

An HR profile record must be associated with the employee record in the User \[sys\_user\] table, to ensure that both employee records can be accessed conveniently. During the creation of an HR profile record, you can select the user record to associate with the profile.

Certain fields are displayed in both the user and HR profile records, but they are in only one of the tables, User \[sys\_user\] or HR Profile \[hr\_profile\]. The following fields are in the User \[sys\_user\] table.

-   Prefix \[introduction\]
-   First name \[first\_name\]
-   Middle name \[middle\_name\]
-   Last name \[last\_name\]
-   Manager \[manager\]
-   Department \[department\]
-   Location \[location\]
-   Employee number \[employee\_number\]

**Note:** Bot phone number sync is not supported.

The following table describes the other fields that are synchronized by the **Synchronize fields to hr\_profile** business rule.

<table id="table_ftq_klk_ss"><thead><tr><th>

HR profile \[hr\_profile\] field

</th><th>

User \[sys\_user\] field

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Position \[position\]

</td><td>

Title \[title\]

</td><td>

Position in the HR profile is a referenced field. The HR profile could not be updated message appears: -   When the title is updated in the User form
-   A position record with the same value does not exist

</td></tr><tr><td>

Home address \[address\]

</td><td>

Street \[street\]

</td><td>

 

</td></tr><tr><td>

Country \[country\]

</td><td>

Country code \[country\]

</td><td>

Although the field names are the same, these fields are of different types. In the HR profile, \[country\] is a reference field. In the user record, \[country\] is a choice list. The country code appears in the User form instead of the country name when the country selected in the HR profile is not in the choice list.

</td></tr><tr><td>

Work email \[work\_email\]

</td><td>

Email \[email\]

</td><td>

The HR profile contains both personal and work email fields, while the user record only contains the work email.

</td></tr></tbody>
</table>**Note:** The User form must be configured to show address, country, and email fields.

**Parent Topic:**[HR Profile](c_HRProfileRecords.md)

